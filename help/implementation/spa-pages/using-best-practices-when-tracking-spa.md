---
title: Utilisation des bonnes pratiques lors du suivi des applications monopages (SPA) dans Adobe Analytics
description: Dans ce document, nous décrirons plusieurs bonnes pratiques que vous devez suivre et connaître lorsque vous utilisez Adobe Analytics pour effectuer le suivi des applications monopages (SPA). Ce document se concentre sur l’utilisation d’Experience Platform Launch, qui est la méthode d’implémentation recommandée.
feature: Implementation Basics
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: Developer, Data Engineer
level: Intermediate
exl-id: 8fe63dd1-9629-437f-ae07-fe1c5a05fa42
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 100%

---

# Utilisation des bonnes pratiques lors du suivi des applications monopages (SPA) dans Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

Dans ce document, nous décrirons plusieurs bonnes pratiques que vous devez suivre et connaître lorsque vous utilisez Adobe Analytics pour effectuer le suivi des applications monopages (SPA). Ce document se concentre sur l’utilisation d’Adobe [!DNL Experience Platform Launch], qui est la méthode d’implémentation recommandée.

NOTES INITIALES :

* Les éléments ci-dessous supposent que vous utilisez [!DNL Experience Platform Launch] pour l’implémentation sur votre site. Les considérations persistent si vous n’utilisez pas [!DNL Experience Platform Launch], mais vous devez les adapter à votre méthode d’implémentation.
* Toutes les SPA sont différentes. Vous devrez peut-être donc ajuster certains des éléments suivants pour répondre au mieux à vos besoins, mais nous avons voulu partager certaines bonnes pratiques avec vous. Il s’agit d’éléments auxquels vous devez réfléchir lorsque vous implémentez Adobe Analytics sur des pages SPA.

## Schéma simple de l’utilisation des SPA dans [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![spa pour analytics dans launch](assets/spa_for_analyticsinlaunch.png)

**REMARQUE :** comme indiqué, il s’agit d’un schéma simplifié de la façon dont les pages SPA sont traitées dans une implémentation d’Adobe Analytics à l’aide d’[!DNL Experience Platform Launch]. Dans les sections suivantes de cette page, nous discuterons des étapes et des problèmes que vous devez soigneusement étudier ou traiter.

## Définition de la couche de données {#setting-the-data-layer}

Lorsque du nouveau contenu est chargé sur une page SPA ou lorsqu’une action a lieu sur une page SPA, l’une des premières choses à faire est de mettre à jour la couche de données. Cela doit se produire AVANT que l’événement personnalisé ne se déclenche et ne déclenche des règles dans [!DNL Experience Platform Launch], de sorte qu’[!DNL Experience Platform Launch] puisse sélectionner les nouvelles valeurs de la couche de données et les transmettre dans Adobe Analytics.

Vous trouverez ci-dessous un exemple de couche de données, dont les éléments peuvent être modifiés lors d’une modification d’affichage ou d’une action sur votre application monopage. Par exemple, lors d’une modification en plein écran/en majorité, il serait courant de modifier un élément « [!DNL pageName] », de sorte que le nouvel élément puisse être capturé dans [!DNL Experience Platform Launch] et envoyé dans Adobe Analytics.

```JavaScript
<script>
    digitalData = {
        pageInstanceID: "Launch Demo Site",
        page:{
            pageInfo:{
                pageID: '2745374',
                pageName: 'acs demo - product listing page'
            },
            attributes:{
                project: "Experience Platform Launch Project"
            }
        },
        user : [ {
          "profile" : [ {
            "attributes" : {
              "gender" : "male",
              "age" : "35"
            }
          } ]
        }],
        libraries : {
          adobe : {
            launch : {
              state : 0, // 0 = not loaded , 1 = loaded
              domain : "assets.adobedtm.com"
            }
          }
        }

     };
    </script>
```

## Définition des événements personnalisés et de l’écoute dans [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Lorsque du nouveau contenu est chargé sur la page ou lorsqu’une action se produit sur le site, vous souhaitez informer [!DNL Experience Platform Launch] afin qu’il puisse exécuter une règle et envoyer des données à [!DNL Analytics]. Il existe plusieurs façons de procéder : les [!UICONTROL règles] d’[!UICONTROL appel direct] ou les événements personnalisés.

* [!UICONTROL Règles] d’[!UICONTROL appel direct] : dans [!DNL Experience Platform Launch], vous pouvez configurer une [!UICONTROL règle] d’[!UICONTROL appel direct] qui s’exécute lorsqu’elle est appelée directement à partir de la page. Si le chargement de votre page ou l’action effectuée sur votre site est très simple ou s’il est unique et peut exécuter un ensemble spécifique d’instructions à chaque fois (définissez [!DNL eVar4] sur X et déclenchez [!DNL event2] à chaque fois), vous pouvez alors utiliser une [!UICONTROL règle] d’[!UICONTROL appel direct]. Consultez la documentation d’[!DNL Experience Platform Launch] concernant la création de [!UICONTROL règles] d’[!UICONTROL appel direct].
* Événements personnalisés : pour plus de fonctionnalités et pour la possibilité de joindre dynamiquement une payload avec différentes valeurs, vous devez définir des événements JavaScript personnalisés et les écouter dans [!DNL Experience Platform Launch], où vous pouvez utiliser la payload pour définir des variables et envoyer les données dans Adobe Analytics. Il est plus probable que vous ayez besoin de cette fonctionnalité. Cette option est donc considérée comme la bonne pratique. Cependant, chaque fonction de votre site peut déterminer la méthode la plus appropriée. Nous avancerons dans ce document en supposant que vous devez utiliser cette méthode d’événements personnalisés.

**Exemples :** dans [CE](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html?lang=fr) document d’aide, il existe des liens vers des exemples de sites SPA qui ont implémenté [!DNL Analytics] (et d’autres solutions Experience Cloud), ainsi que des documents décrivant ce qui a été implémenté. Dans ces exemples de SPA, les événements personnalisés suivants ont été utilisés :

* [!DNL event-view-start] : cet événement doit se déclencher au démarrage d’affichage/d’état en cours de chargement.
* [!DNL event-view-end] : cet événement doit être déclenché même lorsqu’une modification d’affichage/d’état s’est produite et que tous les composants SPA de la page ont terminé leur chargement. Il s’agit de l’événement qui déclenche généralement un appel dans Adobe Analytics.
* [!DNL event-action-trigger] : cet événement doit se déclencher lorsqu’un événement se produit sur la page, à l’exception du chargement d’affichage/d’état. Il peut s’agir d’un événement de clic ou d’une modification de contenu plus petite sans changement d’affichage.

Pour plus d’informations sur les modes et les moments de déclenchement, consultez les pages/documents référencés ci-dessus. Vous n’avez pas à utiliser ces mêmes noms d’événement, mais les fonctionnalités répertoriées ici sont les bonnes pratiques recommandées. La vidéo suivante montre un exemple de site et indique où, dans [!DNL Experience Platform Launch], écouter les événements personnalisés.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Exécution de s.t() ou s.tl() dans la [!UICONTROL règle] d’[!DNL Experience Platform Launch] {#running-s-t-or-s-tl-in-the-launch-rule}

L’une des choses les plus importantes à comprendre pour [!DNL Analytics] lors de l’utilisation d’une application monopage est la différence entre `s.t()` et `s.tl()`. Vous déclencherez l’une de ces méthodes dans [!DNL Experience Platform Launch] pour envoyer des données dans [!DNL Analytics], mais vous devez savoir quand envoyer chacune d’elles.

* **s.t()** : « t » signifie « track » et correspond à une page vue normale. Même si l’URL ne change pas, la vue change-t-elle suffisamment pour que vous la *considériez* comme une nouvelle « page » ? Si tel est le cas, définissez la variable s.[!DNL pageName] et utilisez `s.t()` pour envoyer l’appel dans [!DNL Analytics].

* **s.tl()** : « tl » signifie « track link » et est généralement utilisé pour le suivi des clics ou des petites modifications de contenu sur la page, par opposition à un changement en plein écran. Si la modification de votre page est légère, de sorte que vous ne la considériez pas comme une nouvelle « page » complète, utilisez `s.tl()` et ne vous souciez pas de définir la variable s.pageName, car [!DNL Analytics] l’ignorera.

**CONSEIL :** certaines personnes appliquent une directive générale selon laquelle si l’écran change de plus de 50 %, il doit être considéré comme une page vue et utiliser `s.t()`. Si la modification de l’écran est inférieure à 50 %, utilisez `s.tl()`. Cependant, c’est à vous de décider ce que vous considérez être une nouvelle « page » et comment vous souhaitez effectuer le suivi de votre site dans Adobe Analytics.

La vidéo suivante montre où/comment déclencher `s.t()` ou `s.tl()` dans Experience Platform Launch.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Effacement des variables {#clearing-variables}

Lors du suivi de votre site avec Adobe Analytics, vous ne souhaitez bien sûr envoyer que les données appropriées dans [!DNL Analytics] au bon moment. Dans un environnement SPA, une valeur suivie dans une variable [!DNL Analytics] peut persister et être renvoyée dans [!DNL Analytics], potentiellement lorsque nous ne le voulons plus. C’est pourquoi l’extension [!DNL Analytics] [!DNL Launch] contient une fonction permettant d’effacer les variables. Ainsi, vous repartez sur une nouvelle base lorsque vous exécutez la demande d’image suivante et envoyez les données dans [!DNL Analytics].

Dans le diagramme ci-dessus, cette opération est répertoriée à la fin du processus, effaçant les variables *après* l’envoi de l’accès. En réalité, vous pouvez le faire avant OU après l’envoi de l’accès. Toutefois, cela doit être cohérent dans vos règles [!DNL Experience Platform Launch], afin que l’effacement se fasse toujours avant ou après la définition de variables et leur envoi. Souvenez-vous que si vous devez effacer les variables *avant* d’exécuter `s.t()`, assurez-vous d’abord d’effacer les variables, puis de définir les nouvelles variables, et enfin d’envoyer les nouvelles données dans [!DNL Analytics].

**REMARQUE :** l’effacement des variables n’est pas toujours nécessaire lors de l’exécution de `s.tl()`, car `s.tl()` nécessite l’utilisation parallèle de la variable [!DNL linkTrackVars] à chaque fois pour indiquer à [!DNL Analytics] quelles variables vont être définies (automatiquement ajoutées en arrière-plan dans [!DNL Experience Platform Launch]). Cela signifie que les variables errantes n’apparaissent généralement pas lors de l’utilisation de `s.tl()`, mais cette opération est vivement recommandée lorsque vous utilisez `s.t()` dans un environnement SPA. Cela dit, en guise de bonne pratique, je recommande vivement d’utiliser la fonction Effacer les variables pour `s.t()` et `s.tl()` dans un environnement SPA, afin d’assurer une collecte de données de qualité.

La vidéo suivante montre où/comment effacer les variables dans [!DNL Launch].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Autres points à prendre en compte {#additional-considerations}

### Fenêtres de code personnalisé dans [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

Dans l’extension [!DNL Launch] [!DNL Analytics], vous pouvez insérer du code personnalisé à deux endroits : la section [!UICONTROL Gestion de bibliothèque] et la section « [!UICONTROL Configurer le dispositif de suivi à l’aide du code personnalisé] » supplémentaire.

![Fenêtres de code personnalisé de Launch Analytics](assets/launch_analyticscustomcodewindows.png)

Il est important de savoir que l’un de ces emplacements n’exécute le code qu’une seule fois, lorsque le chargement initial de la page se produit sur votre page SPA. Si vous avez besoin que le code s’exécute sur une modification d’affichage ou sur une action de votre site, vous devez ajouter une action supplémentaire à la **[!UICONTROL règle]** appropriée (par exemple, dans la [!UICONTROL règle] « chargement de page : fin-d’affichage-d’événement »), de sorte que le code s’exécute chaque fois que la [!UICONTROL règle] s’exécute. Lors de la création de cette action dans la [!UICONTROL règle], définissez *Extension = Core* et *Type d’action = Code personnalisé*.

### Sites SPA/standard « hybrides » {#hybrid-spa-regular-sites}

Certains sites consistent en une combinaison de pages « normales » et de pages SPA. Dans ce cas, vous devez utiliser une stratégie qui fonctionne pour les deux types de page. Lors de la configuration de vos événements personnalisés sur le site et du déclenchement des règles dans [!DNL Experience Platform Launch], veillez à ce qu’il n’y ait pas de double accès allant dans [!DNL Analytics] à partir de la page, en fonction des modifications de hachage, etc. (si c’est ainsi que vous avez choisi de déclencher la règle [!DNL Experience Platform Launch]). Dans ce cas, vous devez supprimer l’une des pages vues afin qu’elle ne vous fournisse pas les données incorrectes dans Adobe Analytics.

Si vous décidez de diviser la fonctionnalité en [!UICONTROL règles] distinctes afin d’avoir plus de contrôle sur celle-ci, veillez à vous rappeler/documenter que vous avez fait cela, de sorte que toute modification d’une [!UICONTROL règle] puisse être apportée à l’autre [!UICONTROL règle], protégeant ainsi l’intégrité de vos données [!DNL Analytics].

### Intégration à [!DNL Target] via A4T {#integration-with-target-via-a4t}

Voici juste un petit rappel. Si vous effectuez une intégration à [!DNL Target] à l’aide d’A4T, assurez-vous que la requête [!DNL Target] et la requête [!DNL Analytics] sur la même modification d’affichage ont le même SDID. Vous aurez ainsi la garantie que vos données se synchronisent correctement sur les solutions.

Pour afficher les accès, utilisez un débogueur ou un programme de renifleur de paquets. Vous pouvez également utiliser Experience Cloud Debugger, une extension Chrome qui peut être téléchargée [ICI](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). [!DNL Target] doit être déclenché en premier sur la page. Vous pouvez donc également vérifier cela dans la console JavaScript ou dans le débogueur.

## Ressources supplémentaires {#additional-resources}

* [Discussion sur les SPA sur les forums Adobe](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-platform-launch/best-practices-for-single-page-apps/m-p/267940?profile.language=fr)
* [Sites d’architecture de référence pour montrer comment implémenter une application monopage dans Experience Platform Launch](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)
