---
title: 'Utilisation des bonnes pratiques lors du suivi des applications d’une seule page (ZPS) en Adobe Analytics '
description: Dans ce document, nous décrirons plusieurs bonnes pratiques que vous devez suivre et dont vous devez tenir compte lorsque vous utilisez Adobe Analytics pour effectuer le suivi des applications d’une seule page. Ce document se concentrera sur l’utilisation de l’Experience Platform Launch, qui est la méthode d’implémentation recommandée.
feature: implementation basics
topics: spa
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
translation-type: tm+mt
source-git-commit: 548ac75589383dfd4da4ae02412de91a0a3b28d6
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 0%

---


# Utilisation des bonnes pratiques lors du suivi des applications d’une seule page (ZPS) en Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

Dans ce document, nous décrirons plusieurs bonnes pratiques que vous devez suivre et dont vous devez tenir compte lorsque vous utilisez Adobe Analytics pour effectuer le suivi des applications d’une seule page. Ce document se concentrera sur l’utilisation de l’Adobe [!DNL Experience Platform Launch], qui est la méthode d’implémentation recommandée.

NOTES INITIALES :

* Les éléments ci-dessous partent du principe que vous utilisez [!DNL Experience Platform Launch] pour la mise en oeuvre sur votre site. Si vous n’utilisez pas [!DNL Experience Platform Launch]les éléments à prendre en compte, vous devrez les adapter à votre méthode d’implémentation.
* Tous les SPA sont différents. Il est donc possible que vous deviez modifier certains des éléments suivants pour répondre le mieux à vos besoins, mais nous voulions partager avec vous certaines bonnes pratiques ; ce à quoi vous devez réfléchir pendant que vous implémentez Adobe Analytics sur des pages d’application d’une seule page.

## Diagramme simple d’utilisation des applications monopages dans [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![spa for analytics au lancement](assets/spa_for_analyticsinlaunch.png)

**REMARQUE :** Comme indiqué, il s’agit d’un diagramme simplifié de la manière dont les pages d’une application d’une seule page sont gérées dans une mise en oeuvre Adobe Analytics utilisant [!DNL Experience Platform Launch]. Dans les sections suivantes de cette page, nous discuterons des étapes et de tout problème que vous devriez examiner attentivement ou sur lequel vous devriez agir.

## Définition de la couche de données {#setting-the-data-layer}

Lorsque du nouveau contenu est chargé sur une page d’application d’une seule page ou lorsqu’une action a lieu sur une page d’application d’une seule page, l’une des premières choses à faire est de mettre à jour la couche de données. Ceci doit se produire AVANT que le événement personnalisé ne déclenche et ne déclenche des règles dans [!DNL Experience Platform Launch], afin que [!DNL Experience Platform Launch] les nouvelles valeurs de la couche de données puissent être récupérées et poussées dans Adobe Analytics.

Vous trouverez ci-dessous un exemple de couche de données dont les éléments peuvent être modifiés lors d’un changement de vue ou d’une action sur votre application d’une seule page. Par exemple, lors d’un changement en mode Plein écran ou Majorité, il serait courant de modifier un élément &quot;[!DNL pageName]&quot;, de sorte que le nouveau élément puisse être capturé dans [!DNL Experience Platform Launch] Adobe Analytics et envoyé dans.

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

## Définition des Événements personnalisés et de l’écoute dans [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Lorsque du nouveau contenu est chargé sur la page ou lorsqu’une action se produit sur le site, vous devez en informer [!DNL Experience Platform Launch] afin qu’il puisse exécuter une règle et envoyer des données à [!DNL Analytics]. Il existe plusieurs façons de procéder :  Règles [!UICONTROL d’appel] direct ou Événements personnalisés.

*  Règles [!UICONTROL d&#39;appel]direct : dans [!DNL Experience Platform Launch], vous pouvez configurer une [!UICONTROL règle] d’appel  direct qui s’exécute lorsqu’elle est appelée directement à partir de la page. Si le chargement de votre page ou votre action sur votre site est très simple, ou s’il est unique et peut exécuter un ensemble spécifique d’instructions à chaque fois (défini [!DNL eVar4] sur X et déclenché [!DNL event2] à chaque fois), vous pouvez alors utiliser une [!UICONTROL règle] d’appel direct. Voir [!DNL Experience Platform Launch] la documentation relative à la création de [!UICONTROL règles] d’appel direct.
* Événements personnalisés : Pour plus de fonctionnalités et pour la possibilité de joindre dynamiquement une charge utile avec des valeurs différentes, vous devez définir des événements JavaScript personnalisés et les écouter dans [!DNL Experience Platform Launch], où vous pouvez utiliser la charge utile pour définir des variables et envoyer les données dans Adobe Analytics. Il est plus probable que vous ayez besoin de cette fonctionnalité et cette option est donc considérée comme la meilleure pratique. Cependant, chaque fonction de votre site peut déterminer la méthode la plus appropriée. Nous avancerons dans ce document en supposant que vous devrez utiliser cette méthode de événements personnalisés.

**Exemples :** Dans [CE](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) document d’aide, il existe des liens vers des exemples de sites d’application d’une seule page qui ont mis en oeuvre [!DNL Analytics] (et d’autres solutions Experience Cloud), ainsi que des documents décrivant ce qui a été mis en oeuvre. Dans ces exemples d’application d’une seule page, les événements personnalisés suivants ont été utilisés :

* [!DNL event-view-start]: Ce événement doit se déclencher sur le début de vue de la vue/de l’état en cours de chargement.
* [!DNL event-view-end]: Ce événement doit être déclenché même lorsqu’une modification de vue/état s’est produite et que tous les composants SPA de la page ont terminé de se charger. Il s’agit du événement qui déclenche généralement un appel à Adobe Analytics.
* [!DNL event-action-trigger]: Ce événement doit se déclencher lorsqu’un événement se produit sur la page, à l’exception du chargement de vue/état. Il peut s’agir d’un événement de clics ou d’une modification de contenu plus petite sans modification de vue.

Pour plus d&#39;informations sur le mode de déclenchement/la date de déclenchement, consultez les pages/documents mentionnés ci-dessus. Il n’est pas nécessaire d’utiliser ces mêmes noms de événement, mais les fonctionnalités répertoriées ici sont les meilleures pratiques recommandées. La vidéo suivante montre un exemple de site et où [!DNL Experience Platform Launch] écouter les événements personnalisés.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Exécution de s.t() ou s.tl() dans la [!DNL Experience Platform Launch][!UICONTROL règle] {#running-s-t-or-s-tl-in-the-launch-rule}

L&#39;une des choses les plus importantes à comprendre pour [!DNL Analytics] travailler avec un SPA est la différence entre `s.t()` et `s.tl()`. Vous déclencherez l&#39;une de ces méthodes pour [!DNL Experience Platform Launch] envoyer des données à [!DNL Analytics], mais vous devez savoir quand les envoyer.

* **s.t()** - &quot;t&quot; signifie &quot;track&quot; et est une vue de page normale. Même si l’URL ne change pas, la vue change-t-elle suffisamment pour que vous la *considériez* comme une nouvelle &quot;page&quot; ? Si tel est le cas, définissez la variable s.[!DNL pageName] et à utiliser `s.t()` pour envoyer l’appel à [!DNL Analytics]

* **s.tl()** - &quot;tl&quot; signifie &quot;lien de suivi&quot; et est normalement utilisé pour le suivi des clics ou des modifications de contenu mineures sur la page, par opposition à un changement en plein écran. Si la modification apportée à votre page est petite, de sorte que vous ne la considériez pas comme une nouvelle &quot;page&quot; complète, utilisez `s.tl()` et ne vous souciez pas de la définition de la variable s.pageName, car [!DNL Analytics] elle sera ignorée.

**CONSEIL :** Certaines personnes utilisent une directive générale selon laquelle si l’écran change de plus de 50 %, il doit être considéré comme une vue de page et utilisé `s.t()`. S’il s’agit d’une modification de moins de 50 % de l’écran, utilisez `s.tl()`. Cependant, c&#39;est entièrement à vous et à ce que vous considérez comme une nouvelle &quot;page&quot; et comment vous souhaitez suivre votre site en Adobe Analytics.

La vidéo suivante montre où/comment se déclencher `s.t()` ou `s.tl()` en Launch by Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Effacement des variables {#clearing-variables}

Lorsque vous effectuez le suivi de votre site avec Adobe Analytics, vous ne souhaitez bien sûr qu’envoyer les données appropriées [!DNL Analytics] au bon moment. Dans un environnement d’application d’une seule page, une valeur suivie dans une [!DNL Analytics] variable peut persister et être renvoyée dans [!DNL Analytics]une autre page, éventuellement lorsque nous ne le voulons plus. C&#39;est pourquoi il existe une fonction dans l&#39; [!DNL Analytics] extension [!DNL Launch] pour effacer les variables, de sorte que vous disposez d&#39;une nouvelle ardoise lorsque vous exécutez la demande d&#39;image suivante et envoyez des données dans [!DNL Analytics].

Dans le diagramme ci-dessus, il est répertorié à la fin du processus, en supprimant les variables *après* l’envoi de l’accès. En réalité, il peut être effectué avant OU après l’envoi de l’accès, mais il doit être cohérent dans vos [!DNL Experience Platform Launch] règles, de sorte que vous puissiez toujours effacer avant ou après la définition des variables et leur envoi. N&#39;oubliez pas que si vous devez effacer les variables *avant* de les exécuter `s.t()`, veillez à effacer d&#39;abord les variables, puis définissez les nouvelles variables, puis envoyez enfin les nouvelles données dans [!DNL Analytics]le.

**REMARQUE :** Il n’est pas toujours nécessaire d’effacer les variables lors de l’exécution `s.tl()`, car `s.tl()` il faut utiliser la [!DNL linkTrackVars] variable à côté de celle-ci à chaque fois pour indiquer [!DNL Analytics] quelles variables vont être définies (automatiquement ajoutées en arrière-plan dans [!DNL Experience Platform Launch]). Cela signifie que les variables errantes ne sont généralement pas incluses lors de l’utilisation `s.tl()`, mais elles sont très recommandées lors `s.t()` de l’utilisation dans un environnement d’application d’une seule page. Ceci étant dit, je voudrais recommander comme meilleure pratique d&#39;utiliser la fonction Clear Variables à la fois pour `s.t()` et `s.tl()` dans un environnement d&#39;application d&#39;une seule page, juste pour assurer la qualité de la collecte de données.

La vidéo suivante montre où/comment effacer les variables dans [!DNL Launch].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Autres points à prendre en compte {#additional-considerations}

### Fenêtres de code personnalisé dans [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

Dans l’ [!DNL Launch] extension [!DNL Analytics] , vous pouvez insérer du code personnalisé à deux endroits : La section de gestion [!UICONTROL des] bibliothèques et la section supplémentaire &quot;[!UICONTROL Configurer le suivi à l’aide du code]personnalisé&quot;.

![Lancement des fenêtres de code personnalisé d’Analytics](assets/launch_analyticscustomcodewindows.png)

Il est important de savoir que l’un ou l’autre de ces emplacements n’exécutera le code qu’une seule fois, lorsque la page initiale sera chargée sur votre page d’application d’une seule page. Si vous avez besoin que le code s’exécute sur une modification de vue ou sur une action de votre site, vous devez ajouter une action supplémentaire à la **[!UICONTROL règle]** appropriée (par exemple, dans &quot;chargement de page : &quot; [!UICONTROL règle]événement-vue-end&quot;), de sorte que le code s’exécute chaque fois que cette [!UICONTROL règle] s’exécute. Lors de la création de cette action dans la [!UICONTROL règle], définissez *Extension = Core* et *Action Type = Custom Code*.

### SPA &quot;hybride&quot;/Sites réguliers {#hybrid-spa-regular-sites}

Certains sites sont une combinaison de pages &quot;régulières&quot; et de pages d’application d’une seule page. Dans ce cas, vous devez utiliser une stratégie qui fonctionne pour les deux types de page. Lors de la configuration de vos événements personnalisés sur le site et du déclenchement des règles dans [!DNL Experience Platform Launch], veillez à ce qu’aucun accès au doublon ne soit effectué [!DNL Analytics] à partir de la page, en fonction des modifications de hachage, etc. (si c&#39;est ainsi que vous avez choisi de déclencher la [!DNL Experience Platform Launch] règle). Dans ce cas, vous devrez supprimer l’une des vues de page afin qu’elle ne vous donne pas de données erronées dans Adobe Analytics.

Si vous décidez de diviser la fonctionnalité en [!UICONTROL règles] distinctes afin que vous puissiez mieux la contrôler, n’oubliez pas/document que vous avez fait cela, de sorte que toute modification d’une [!UICONTROL règle] puisse être apportée à l’autre [!UICONTROL règle] , protégeant ainsi l’intégrité de vos [!DNL Analytics] données.

### Intégration à [!DNL Target] via A4T {#integration-with-target-via-a4t}

Juste un rapide rappel ici. Si vous effectuez une intégration avec [!DNL Target] A4T, assurez-vous que la [!DNL Target] demande et la [!DNL Analytics] demande sur la même vue ont le même SDID. Ainsi, vos données seront correctement synchronisées sur les solutions.

Pour afficher les accès, utilisez un débogueur ou un programme renifleur de paquets. Vous pouvez également utiliser l’Experience Cloud Debugger, une extension Chrome qui peut être téléchargée [ICI](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). [!DNL Target] doit se déclencher en premier sur la page, de sorte que vous puissiez également vérifier cela dans la console JavaScript ou le débogueur.

## Ressources supplémentaires {#additional-resources}

* [Discussion de l&#39;APS sur les forums d&#39;Adobe](https://forums.adobe.com/thread/2451022)
* [Sites d’architecture de référence pour montrer comment implémenter l’application d’une seule page dans l’Experience Platform Launch](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)