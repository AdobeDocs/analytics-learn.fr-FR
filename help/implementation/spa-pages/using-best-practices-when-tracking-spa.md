---
title: 'Utilisation des bonnes pratiques lors du suivi des applications d’une seule page (SPA) dans Adobe Analytics '
description: Dans ce document, nous décrirons plusieurs bonnes pratiques que vous devez suivre et connaître lorsque vous utilisez Adobe Analytics pour effectuer le suivi des applications d’une seule page (SPA). Ce document se concentre sur l’utilisation d’Experience Platform Launch, qui est la méthode de mise en oeuvre recommandée.
feature: Concepts de base de la mise en œuvre
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
source-wordcount: '1672'
ht-degree: 0%

---

# Utilisation des bonnes pratiques lors du suivi des applications d’une seule page (SPA) dans Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

Dans ce document, nous décrirons plusieurs bonnes pratiques que vous devez suivre et connaître lorsque vous utilisez Adobe Analytics pour effectuer le suivi des applications d’une seule page (SPA). Ce document se concentre sur l’utilisation de l’Adobe [!DNL Experience Platform Launch], qui est la méthode de mise en oeuvre recommandée.

NOTES INITIALES :

* Les éléments ci-dessous supposent que vous utilisez [!DNL Experience Platform Launch] pour implémenter sur votre site. Les considérations persistent si vous n’utilisez pas [!DNL Experience Platform Launch], mais vous devez les adapter à votre méthode de mise en oeuvre.
* Tous les SPA sont différents. Vous devrez peut-être donc ajuster certains des éléments suivants pour répondre le mieux à vos besoins, mais nous avons voulu partager certaines bonnes pratiques avec vous. éléments auxquels vous devez réfléchir pendant la mise en oeuvre d’Adobe Analytics sur SPA pages.

## Schéma simple de l’utilisation de SPA dans [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![spa pour analytics dans launch](assets/spa_for_analyticsinlaunch.png)

**REMARQUE :** Comme indiqué, il s’agit d’un diagramme simplifié de la manière dont SPA pages sont traitées dans une mise en oeuvre Adobe Analytics à l’aide de  [!DNL Experience Platform Launch]. Dans les sections suivantes de cette page, nous discuterons des étapes et des problèmes que vous devez soigneusement étudier ou traiter.

## Définition de la couche de données {#setting-the-data-layer}

Lorsque du nouveau contenu est chargé sur une page SPA ou lorsqu’une action a lieu sur une page SPA, l’une des premières choses à faire est de mettre à jour la couche de données. Cela doit se produire AVANT que l’événement personnalisé ne déclenche et ne déclenche des règles dans [!DNL Experience Platform Launch], de sorte que [!DNL Experience Platform Launch] puisse sélectionner les nouvelles valeurs de la couche de données et les transmettre dans Adobe Analytics.

Vous trouverez ci-dessous un exemple de couche de données, dont les éléments peuvent être modifiés lors du changement d’affichage ou de l’action sur votre SPA. Par exemple, lors d’une modification en plein écran/en majorité, il serait courant de modifier un élément &quot;[!DNL pageName]&quot;, de sorte que le nouvel élément puisse être capturé dans [!DNL Experience Platform Launch] et envoyé dans Adobe Analytics.

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

Lorsque du nouveau contenu se charge sur la page ou lorsqu’une action se produit sur le site, vous souhaitez informer [!DNL Experience Platform Launch] afin qu’il puisse exécuter une règle et envoyer des données à [!DNL Analytics]. Il existe plusieurs façons de procéder : [!UICONTROL Appel direct] [!UICONTROL règles] ou événements personnalisés.

* [!UICONTROL Règles ] [!UICONTROL d’appel direct] : dans  [!DNL Experience Platform Launch], vous pouvez configurer un  [!UICONTROL appel ]  direct qui s’exécute lorsqu’il est appelé directement à partir de la page. Si le chargement de votre page ou l’action effectuée sur votre site est très simple, ou s’il est unique et qu’il peut exécuter un ensemble spécifique d’instructions à chaque fois (définissez [!DNL eVar4] sur X et déclenchez [!DNL event2] à chaque fois), vous pouvez utiliser un [!UICONTROL appel direct] [!UICONTROL règle]. Voir [!DNL Experience Platform Launch] documentation concernant la création de [!UICONTROL règles ] [!UICONTROL d’appel direct].
* Événements personnalisés : Pour plus de fonctionnalités et pour la possibilité de joindre dynamiquement une payload avec différentes valeurs, vous devez définir des événements JavaScript personnalisés et les écouter dans [!DNL Experience Platform Launch], où vous pouvez utiliser la payload pour définir des variables et envoyer les données dans Adobe Analytics. Il est plus probable que vous ayez besoin de cette fonctionnalité. Cette option est donc considérée comme la bonne pratique. Cependant, chaque fonction de votre site peut déterminer la méthode la plus appropriée. Nous avancerons dans ce document en supposant que vous devrez utiliser cette méthode d’événements personnalisée.

**Exemples :** dans  [](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) CE document d’aide, il existe des liens vers des exemples de sites SPA qui ont mis en oeuvre  [!DNL Analytics] (et d’autres solutions Experience Cloud), ainsi que des documents décrivant ce qui a été mis en oeuvre. Dans ces SPA exemples, les événements personnalisés suivants ont été utilisés :

* [!DNL event-view-start]: Cet événement doit se déclencher au démarrage de la vue/de l’état en cours de chargement.
* [!DNL event-view-end]: Cet événement doit être déclenché même lorsqu’un changement d’affichage/d’état s’est produit et que tous les composants SPA de la page ont terminé de se charger. Il s’agit de l’événement qui déclenche généralement un appel dans Adobe Analytics.
* [!DNL event-action-trigger]: Cet événement doit se déclencher lorsqu’un événement se produit sur la page, à l’exception du chargement d’affichage/d’état. Il peut s’agir d’un événement de clic ou d’une modification de contenu plus petite sans changement d’affichage.

Pour plus d’informations sur le mode de déclenchement ou le moment où ils sont déclenchés, consultez les pages/documents référencés ci-dessus. Vous n’avez pas à utiliser ces mêmes noms d’événement, mais les fonctionnalités répertoriées ici sont les bonnes pratiques recommandées. La vidéo suivante montre un exemple de site et où dans [!DNL Experience Platform Launch] écouter les événements personnalisés.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Exécution de s.t() ou s.tl() dans la [!DNL Experience Platform Launch] [!UICONTROL règle] {#running-s-t-or-s-tl-in-the-launch-rule}

L’une des choses les plus importantes à comprendre pour [!DNL Analytics] lors de l’utilisation d’un SPA est la différence entre `s.t()` et `s.tl()`. Vous déclencherez l’une de ces méthodes dans [!DNL Experience Platform Launch] pour envoyer des données dans [!DNL Analytics], mais vous devez savoir quand envoyer chacune d’elles.

* **s.t()**  - &quot;t&quot; signifie &quot;track&quot; et correspond à une page vue normale. Même si l’URL ne change pas, la vue change-t-elle suffisamment pour que vous considériez *qu’il s’agit d’une nouvelle &quot;page&quot; ?* Si tel est le cas, définissez la variable s.[!DNL pageName] et utilisez `s.t()` pour envoyer l’appel dans [!DNL Analytics].

* **s.tl()**  : &quot;tl&quot; signifie &quot;lien de suivi&quot; et est généralement utilisé pour le suivi des clics ou des petites modifications de contenu sur la page, par opposition à un changement en plein écran. Si la modification de votre page est faible, de sorte que vous ne la considériez pas comme une nouvelle &quot;page&quot; complète, utilisez `s.tl()` et ne vous souciez pas de définir la variable s.pageName, car [!DNL Analytics] l’ignorera.

**CONSEIL :** Certaines personnes utilisent une directive générale selon laquelle si l’écran change de plus de 50 %, il doit être considéré comme une page vue et utilisé  `s.t()`. Si la modification de l’écran est inférieure à 50 %, utilisez `s.tl()`. Cependant, c’est entièrement à vous et à ce que vous considérez comme une nouvelle &quot;page&quot; et comment vous souhaitez effectuer le suivi de votre site dans Adobe Analytics.

La vidéo suivante montre où/comment déclencher `s.t()` ou `s.tl()` en Launch by Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Effacement des variables {#clearing-variables}

Lors du suivi de votre site avec Adobe Analytics, vous ne souhaitez bien sûr envoyer les données appropriées dans [!DNL Analytics] qu’au bon moment. Dans un environnement SPA, une valeur trackée dans une variable [!DNL Analytics] peut persister et être renvoyée dans [!DNL Analytics], potentiellement lorsque nous ne le voulons plus. C’est pourquoi il existe une fonction dans l’extension [!DNL Analytics] [!DNL Launch] pour effacer les variables, de sorte que vous obteniez une nouvelle page lorsque vous exécutez la demande d’image suivante et envoyez les données dans [!DNL Analytics].

Dans le diagramme ci-dessus, il est répertorié à la fin du processus, effaçant les variables *après* que vous envoyez dans l’accès. En réalité, cela peut être fait avant OU après l’envoi de l’accès, mais doit être cohérent dans vos règles [!DNL Experience Platform Launch], de sorte que vous effacez toujours avant ou après la définition de variables et leur envoi. Souvenez-vous que si vous allez effacer les variables *avant* d’exécuter `s.t()`, assurez-vous d’abord d’effacer les variables, puis définissez les nouvelles variables, puis envoyez enfin les nouvelles données dans [!DNL Analytics].

**REMARQUE :** L’effacement des variables n’est pas toujours nécessaire lors de l’exécution  `s.tl()`, car  `s.tl()` nécessite l’utilisation de la  [!DNL linkTrackVars] variable à côté de celle-ci à chaque fois pour indiquer  [!DNL Analytics] quelles variables vont être définies (automatiquement ajoutées en arrière-plan dans  [!DNL Experience Platform Launch]). Cela signifie que les variables errantes ne sont généralement pas présentes lors de l’utilisation de `s.tl()`, mais il est vivement recommandé d’utiliser `s.t()` dans un environnement SPA. Cela dit, je recommande vivement d’utiliser la fonction Effacer les variables pour `s.t()` et `s.tl()` dans un environnement SPA, afin d’assurer la collecte de données de qualité.

La vidéo suivante montre où/comment effacer les variables dans [!DNL Launch].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Autres points à prendre en compte {#additional-considerations}

### Fenêtres de code personnalisé dans [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

Dans l’extension [!DNL Launch] [!DNL Analytics], vous pouvez insérer du code personnalisé à deux endroits : La section [!UICONTROL Gestion de bibliothèque] et la section &quot;[!UICONTROL Configurer le dispositif de suivi à l’aide du code personnalisé]&quot; supplémentaire.

![Lancement des fenêtres de code personnalisé Analytics](assets/launch_analyticscustomcodewindows.png)

Il est important de savoir que l’un de ces emplacements n’exécute le code qu’une seule fois, lorsque le chargement initial de la page se produit sur votre page SPA. Si vous avez besoin que le code s’exécute sur un changement d’affichage ou sur une action de votre site, vous devez ajouter une action supplémentaire à la **[!UICONTROL règle]** appropriée (par exemple, dans le &quot;chargement de page : event-view-end&quot; [!UICONTROL règle]), de sorte que le code s’exécute chaque fois que la [!UICONTROL règle] s’exécute. Lors de la création de cette action dans la [!UICONTROL règle], définissez *Extension = Core* et *Type d’action = Code personnalisé*.

### &quot;Hybride&quot; SPA/sites standard {#hybrid-spa-regular-sites}

Certains sites sont une combinaison de pages &quot;normales&quot; et de pages SPA. Dans ce cas, vous devrez utiliser une stratégie qui fonctionne pour les deux types de page. Lors de la configuration de vos événements personnalisés sur le site et du déclenchement des règles dans [!DNL Experience Platform Launch], veillez à ce qu’il n’y ait pas de double accès allant dans [!DNL Analytics] à partir de la page, en fonction des modifications de hachage, etc. (si c’est ainsi que vous avez choisi de déclencher la règle [!DNL Experience Platform Launch]). Dans ce cas, vous devrez supprimer l’une des pages vues afin qu’elle ne vous fournisse pas les données incorrectes dans Adobe Analytics.

Si vous décidez de diviser la fonctionnalité en [!UICONTROL règles] distinctes afin que vous ayez plus de contrôle sur celle-ci, veillez à vous rappeler/documenter que vous avez fait cela, de sorte que toute modification d’une [!UICONTROL règle] puisse être apportée à l’autre [!UICONTROL règle], protégeant ainsi l’intégrité de vos données [!DNL Analytics].

### Intégration à [!DNL Target] via A4T {#integration-with-target-via-a4t}

Juste un petit rappel ici. Si vous effectuez une intégration avec [!DNL Target] à l’aide d’A4T, assurez-vous que la requête [!DNL Target] et la requête [!DNL Analytics] sur la même modification de vue ont le même SDID. Vous aurez ainsi la garantie que vos données se synchronisent correctement sur les solutions.

Pour afficher les accès, utilisez un débogueur ou un programme de renifleur de paquets. Vous pouvez également utiliser l’Experience Cloud Debugger, une extension Chrome qui peut être téléchargée [HERE](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). [!DNL Target] doit être déclenché en premier sur la page. Vous pouvez donc également vérifier cela dans la console JavaScript ou dans le débogueur.

## Ressources supplémentaires {#additional-resources}

* [SPA discussion sur les forums de l&#39;Adobe](https://forums.adobe.com/thread/2451022)
* [Sites d’architecture de référence pour montrer comment mettre en oeuvre SPA dans Experience Platform Launch](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)
