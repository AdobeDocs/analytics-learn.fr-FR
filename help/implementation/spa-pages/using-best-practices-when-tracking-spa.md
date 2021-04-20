---
title: 'Utilisation des bonnes pratiques lors du suivi des applications d’une seule page (SPA) dans Adobe Analytics '
description: Dans ce document, nous décrirons plusieurs bonnes pratiques que vous devez suivre et connaître lorsque vous utilisez Adobe Analytics pour effectuer le suivi des applications d’une seule page (SPA). Ce document se concentrera sur l’utilisation de l’Experience Platform Launch, qui est la méthode d’implémentation recommandée.
feature: Implementation Basics
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: "Developer, Data Engineer"
level: Intermediate
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '1676'
ht-degree: 0%

---


# Utilisation des bonnes pratiques lors du suivi des applications d’une seule page (SPA) dans Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

Dans ce document, nous décrirons plusieurs bonnes pratiques que vous devez suivre et connaître lorsque vous utilisez Adobe Analytics pour effectuer le suivi des applications d’une seule page (SPA). Ce document porte sur l&#39;utilisation de l&#39;Adobe [!DNL Experience Platform Launch], qui est la méthode d&#39;implémentation recommandée.

NOTES INITIALES :

* Les éléments ci-dessous vont supposer que vous utilisez [!DNL Experience Platform Launch] pour implémenter votre site. Les considérations persistent si vous n’utilisez pas [!DNL Experience Platform Launch], mais vous devez les adapter à votre méthode d’implémentation.
* Tous les SPA sont différents, vous devrez peut-être modifier certains des éléments suivants pour mieux répondre à vos besoins, mais nous voulions partager avec vous certaines pratiques exemplaires ; à quoi vous devez réfléchir pendant que vous implémentez Adobe Analytics sur SPA pages.

## Diagramme simple de l&#39;utilisation des SPA dans [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![spa for analytics au lancement](assets/spa_for_analyticsinlaunch.png)

**REMARQUE :** Comme nous l&#39;avons indiqué, il s&#39;agit d&#39;un diagramme simplifié de la façon dont SPA pages sont traitées dans une implémentation Adobe Analytics utilisant  [!DNL Experience Platform Launch]. Dans les sections suivantes de cette page, nous discuterons des étapes et de tout problème que vous devriez examiner attentivement ou sur lequel vous devriez agir.

## Définition de la couche de données {#setting-the-data-layer}

Lorsque du nouveau contenu est chargé sur une page SPA ou lorsqu’une action se produit sur une page SPA, l’une des premières choses à faire est de mettre à jour la couche de données. Ceci doit se produire AVANT que le événement personnalisé déclenche et déclenche des règles dans [!DNL Experience Platform Launch], de sorte que [!DNL Experience Platform Launch] puisse sélectionner les nouvelles valeurs de la couche de données et les pousser dans Adobe Analytics.

Vous trouverez ci-dessous un exemple de couche de données dont les éléments peuvent être modifiés lors d’un changement de vue ou d’une action sur votre SPA. Par exemple, dans le cas d’un changement d’écran complet/majoritaire, il serait courant de modifier un élément &quot;[!DNL pageName]&quot;, de sorte que le nouveau élément puisse être capturé dans [!DNL Experience Platform Launch] et envoyé en Adobe Analytics.

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

Lorsque du nouveau contenu est chargé sur la page ou lorsqu’une action se produit sur le site, vous devez en informer [!DNL Experience Platform Launch] afin qu’il puisse exécuter une règle et envoyer des données à [!DNL Analytics]. Il existe plusieurs façons de procéder : [!UICONTROL Appels directs] [!UICONTROL règles] ou Événements personnalisés.

* [!UICONTROL Règles] d&#39;appel direct : dans  [!DNL Experience Platform Launch], vous pouvez configurer un appel    direct qui s’exécute lorsqu’il est appelé directement à partir de la page. Si le chargement de votre page ou votre action sur votre site est très simple, ou s&#39;il est unique et peut exécuter un ensemble spécifique d&#39;instructions à chaque fois (définissez [!DNL eVar4] sur X et déclenchez [!DNL event2] à chaque fois), vous pouvez utiliser un [!UICONTROL appel direct] [!UICONTROL règle]. Voir la documentation [!DNL Experience Platform Launch] concernant la création de [!UICONTROL règles ] [!UICONTROL d&#39;appel direct].
* Événements personnalisés : Pour plus de fonctionnalités et la possibilité de joindre dynamiquement une charge utile avec des valeurs différentes, vous devez définir des événements JavaScript personnalisés et les écouter dans [!DNL Experience Platform Launch], où vous pouvez utiliser la charge utile pour définir des variables et envoyer les données dans Adobe Analytics. Il est plus probable que vous ayez besoin de cette fonctionnalité et cette option est donc considérée comme la meilleure pratique. Cependant, chaque fonction de votre site peut déterminer la méthode la plus appropriée. Nous avancerons dans ce document en supposant que vous devrez utiliser cette méthode de événements personnalisés.

**Exemples :** Dans  [](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) CEhelp document, il existe des liens vers des exemples de sites SPA qui ont mis en oeuvre  [!DNL Analytics] (et d’autres solutions Experience Cloud), ainsi que des documents décrivant ce qui a été mis en oeuvre. Dans ces SPA exemples, les événements personnalisés suivants ont été utilisés :

* [!DNL event-view-start]: Ce événement doit se déclencher sur le début de vue de la vue/de l’état en cours de chargement.
* [!DNL event-view-end]: Ce événement doit être déclenché même lorsqu’une modification de vue/état s’est produite et que tous les composants SPA de la page ont terminé de se charger. Il s’agit du événement qui déclenche généralement un appel à Adobe Analytics.
* [!DNL event-action-trigger]: Ce événement doit se déclencher lorsqu’un événement se produit sur la page, à l’exception du chargement de vue/état. Il peut s’agir d’un événement de clics ou d’une modification de contenu plus petite sans modification de vue.

Pour plus d&#39;informations sur le mode de déclenchement/la date de déclenchement, consultez les pages/documents mentionnés ci-dessus. Il n’est pas nécessaire d’utiliser ces mêmes noms de événement, mais les fonctionnalités répertoriées ici sont les meilleures pratiques recommandées. La vidéo suivante montre un exemple de site et où dans [!DNL Experience Platform Launch] pour écouter les événements personnalisés.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Exécution de s.t() ou s.tl() dans la [!DNL Experience Platform Launch] [!UICONTROL règle] {#running-s-t-or-s-tl-in-the-launch-rule}

L&#39;une des choses les plus importantes à comprendre pour [!DNL Analytics] lorsque vous travaillez avec un SPA est la différence entre `s.t()` et `s.tl()`. Vous déclencherez l&#39;une de ces méthodes dans [!DNL Experience Platform Launch] pour envoyer des données dans [!DNL Analytics], mais vous devez savoir quand les envoyer.

* **s.t()** - &quot;t&quot; signifie &quot;track&quot; et est une vue de page normale. Même si l’URL ne change pas, la vue change-t-elle suffisamment pour que vous *considériez* qu’il s’agit d’une nouvelle &quot;page&quot; ? Si tel est le cas, définissez la variable s.[!DNL pageName] et utilisez `s.t()` pour envoyer l’appel dans [!DNL Analytics].

* **s.tl()** - &quot;tl&quot; signifie &quot;lien de suivi&quot; et est généralement utilisé pour le suivi des clics ou des modifications de contenu mineures sur la page, par opposition à un changement en plein écran. Si la modification apportée à votre page est petite, de sorte que vous ne la considériez pas comme une nouvelle &quot;page&quot; complète, utilisez `s.tl()` et ne vous souciez pas de la définition de la variable s.pageName, car [!DNL Analytics] l’ignorera.

**CONSEIL :** Certaines personnes utilisent une ligne directrice générale selon laquelle si l’écran change de plus de 50 %, il doit être considéré comme une vue de page et une utilisation  `s.t()`. Si l&#39;écran est modifié à moins de 50 %, utilisez `s.tl()`. Cependant, c&#39;est entièrement à vous et à ce que vous considérez comme une nouvelle &quot;page&quot; et comment vous souhaitez suivre votre site en Adobe Analytics.

La vidéo suivante montre où/comment déclencher `s.t()` ou `s.tl()` en Launch by Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Effacement des variables {#clearing-variables}

Lorsque vous effectuez le suivi de votre site avec Adobe Analytics, vous souhaitez bien sûr uniquement envoyer les données appropriées dans [!DNL Analytics] au bon moment. Dans un environnement SPA, une valeur suivie dans une variable [!DNL Analytics] peut persister et être renvoyée dans [!DNL Analytics], potentiellement lorsque nous ne le voulons plus. Pour cette raison, il existe une fonction dans l&#39;extension [!DNL Analytics] [!DNL Launch] pour effacer les variables, de sorte que vous disposez d&#39;une nouvelle ardoise lorsque vous exécutez la demande d&#39;image suivante et envoyez des données dans [!DNL Analytics].

Dans le diagramme ci-dessus, il est répertorié à la fin du processus, en effaçant les variables *après* l’envoi de l’accès. En réalité, il peut être effectué avant OU après l’envoi de l’accès, mais il doit être cohérent dans vos règles [!DNL Experience Platform Launch], de sorte que vous puissiez toujours effacer avant ou après la définition des variables et leur envoi. N&#39;oubliez pas que si vous devez effacer les variables *avant* d&#39;exécuter `s.t()`, assurez-vous d&#39;abord d&#39;effacer les variables, puis définissez les nouvelles variables, puis envoyez enfin les nouvelles données dans [!DNL Analytics].

**REMARQUE :** L&#39;effacement des variables n&#39;est pas toujours nécessaire lors de l&#39;exécution  `s.tl()`car  `s.tl()` nécessite l&#39;utilisation de la  [!DNL linkTrackVars] variable à côté pour indiquer à chaque fois  [!DNL Analytics] quelles variables vont être définies (automatiquement ajoutées en arrière-plan dans  [!DNL Experience Platform Launch]). Cela signifie que les variables errantes ne sont généralement pas incluses lors de l’utilisation de `s.tl()`, mais il est vivement recommandé lors de l’utilisation de `s.t()` dans un environnement SPA. Cela étant dit, je voudrais recommander que la fonction Clear Variables soit utilisée comme meilleure pratique pour `s.t()` et `s.tl()` dans un environnement SPA, juste pour assurer la qualité de la collecte des données.

La vidéo suivante montre où/comment effacer les variables dans [!DNL Launch].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Autres points à prendre en compte {#additional-considerations}

### Fenêtres de code personnalisé dans [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

Dans l&#39;extension [!DNL Launch] [!DNL Analytics], vous pouvez insérer du code personnalisé à deux endroits : La section [!UICONTROL gestion de bibliothèque] et la section &quot;[!UICONTROL Configurer le suivi à l&#39;aide du code personnalisé]&quot; supplémentaires.

![Lancement des fenêtres de code personnalisé d’Analytics](assets/launch_analyticscustomcodewindows.png)

Il est important de savoir que l’un ou l’autre de ces emplacements n’exécutera le code qu’une seule fois, lorsque le chargement initial de la page se produira sur votre page SPA. Si vous avez besoin que le code s&#39;exécute sur une modification de vue ou sur une action de votre site, vous devez ajouter une action supplémentaire à la **[!UICONTROL règle]** appropriée (par exemple dans le &quot;chargement de page : événement-vue-end&quot; [!UICONTROL règle]), de sorte que le code s’exécute chaque fois que [!UICONTROL règle] s’exécute. Lors de la création de cette action dans la [!UICONTROL règle], définissez *Extension = Core* et *Type d&#39;action = Code personnalisé*.

### SPA &quot;hybride&quot;/Sites réguliers {#hybrid-spa-regular-sites}

Certains sites sont une combinaison de pages &quot;régulières&quot; et de pages SPA. Dans ce cas, vous devez utiliser une stratégie qui fonctionne pour les deux types de page. Lors de la configuration de vos événements personnalisés sur le site et du déclenchement des règles dans [!DNL Experience Platform Launch], veillez à ce qu’aucun accès au doublon ne soit entré dans [!DNL Analytics] à partir de la page, en fonction des modifications de hachage, etc. (si c&#39;est ainsi que vous avez choisi de déclencher la règle [!DNL Experience Platform Launch]). Dans ce cas, vous devrez supprimer l’une des vues de page afin qu’elle ne vous donne pas de données erronées dans Adobe Analytics.

Si vous décidez de séparer la fonctionnalité en [!UICONTROL règles] distinctes afin que vous en ayez plus de contrôle, veillez à vous souvenir/document que vous avez fait cela, de sorte que toute modification d&#39;une [!UICONTROL règle] puisse être apportée à l&#39;autre [!UICONTROL règle], tout en protégeant votre intégrité des données [!DNL Analytics].

### Intégration à [!DNL Target] via A4T {#integration-with-target-via-a4t}

Juste un rapide rappel ici. Si vous effectuez une intégration avec [!DNL Target] en utilisant A4T, assurez-vous que la requête [!DNL Target] et la requête [!DNL Analytics] sur la même modification de vue ont le même SDID. Ainsi, vos données seront correctement synchronisées sur les solutions.

Pour afficher les accès, utilisez un débogueur ou un programme renifleur de paquets. Vous pouvez également utiliser l’Experience Cloud Debugger, une extension Chrome qui peut être téléchargée [ICI](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). [!DNL Target] doit se déclencher en premier sur la page, de sorte que vous puissiez également vérifier cela dans la console JavaScript ou le débogueur.

## Ressources supplémentaires {#additional-resources}

* [SPA débat sur les forums Adobes](https://forums.adobe.com/thread/2451022)
* [Sites d’architecture de référence pour montrer comment implémenter des SPA dans l’Experience Platform Launch](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)