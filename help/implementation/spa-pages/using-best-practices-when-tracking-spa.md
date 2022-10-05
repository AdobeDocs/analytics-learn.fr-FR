---
title: Bonnes pratiques d’implémentation pour les applications d’une seule page (SPA)
description: Découvrez quelques bonnes pratiques pour implémenter Adobe Analytics sur des applications d’une seule page (SPA). Cela inclut l’utilisation de balises Experience Platform, la méthode de mise en oeuvre recommandée.
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
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 3%

---

# Bonnes pratiques d’implémentation pour les applications d’une seule page (SPA) {#implementation-best-practices-for-single-page-appliations}

Découvrez les bonnes pratiques de mise en oeuvre de [!DNL Adobe Analytics] sur les applications d’une seule page (SPA). Cela inclut l’utilisation de [!DNL Experience Platform Tags], méthode de mise en oeuvre recommandée.

NOTES INITIALES :

* Le contenu ci-dessous fait référence à l’utilisation de [!DNL Experience Platform Tags] pour mettre en oeuvre Adobe Analytics sur votre site. Ces considérations s’appliquent si : [!DNL Experience Platform Tags] n’est pas utilisée, vous devez donc les adapter à votre méthode de mise en oeuvre.
* Il existe des différences dans SPA. Par conséquent, vous devez ajuster votre approche en fonction de vos besoins.

## Schéma simple de l’utilisation des SPA dans [!DNL Experience Platform Tags] {#simple-diagram-of-working-with-spas-in-tags}

![SPA pour les analyses dans les balises](assets/spa_for_analyticsinlaunch.png)

**REMARQUE :** Il s’agit d’un diagramme simplifié de la manière dont SPA pages sont traitées dans une mise en oeuvre Adobe Analytics à l’aide de [!DNL Experience Platform Tags]. Les sections suivantes décrivent les étapes et les problèmes à prendre en compte.

## Définition de la couche de données {#set-the-data-layer}

Lors du chargement d’un nouveau contenu ou d’une action sur une page SPA, *mettre à jour la couche de données en premier*. Cela doit se produire. **before** un événement personnalisé qui déclenche l’exécution d’une règle dans [!DNL Experience Platform Tags]. Cela permet de s’assurer que les valeurs correctes de la couche de données sont transmises dans Balises, puis dans Adobe Analytics.

Voici un exemple de couche de données. L’un de ces éléments peut changer en fonction de la vue initiale ou de la modification ultérieure de la vue, compte tenu d’une action effectuée sur votre page SPA. Par exemple, lors d’un changement de vue complet ou majoritaire, il est courant de transmettre un &quot;[!DNL pageName]&quot; pour différencier les vues dans les rapports Adobe Analytics.

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

## Définissez des événements personnalisés et écoutez ces événements dans [!DNL Experience Platform Tags] {#setting-custom-events-and-listening-in-tags}

Lors du chargement d’un nouveau contenu ou d’une action sur la page SPA, les balises Experience Platform doivent être informées afin d’exécuter une règle qui envoie des données à [!DNL Analytics]. Il existe plusieurs approches pour cela : [!UICONTROL Règles d’appel direct] ou Événements personnalisés.

* [!UICONTROL Règles d’appel direct]: Configurez une [!UICONTROL règle d’appel direct] qui s’exécute lorsqu’il est appelé directement à partir de la page. Si le chargement ou l’action de la page est simple ou unique et peut exécuter un ensemble spécifique d’instructions à chaque fois (par exemple, défini [!DNL eVar4] à X et déclenchez [!DNL event2] à chaque fois), cette approche est adaptée. Voir [!DNL Experience Platform Tags] documentation pour plus d’informations sur la création [!UICONTROL règles d’appel direct].
* Événements personnalisés : Si vous devez joindre de manière dynamique une payload avec des valeurs uniques pour les événements qui se produisent sur SPA pages, utilisez des événements JavaScript personnalisés et écoutez-les dans [!DNL Experience Platform Tags]. Utilisez la payload pour définir les éléments de données et les variables Analytics dans les balises. Cette méthode est considérée comme la bonne pratique, car ce besoin est généralement répandu pour SPA. Les exemples ci-dessous utilisent la méthode d’événements personnalisés.

**Exemples :** [Dans ce](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html) document d’aide, il existe des liens vers des exemples de sites SPA qui implémentent [!DNL Analytics] et d’autres solutions Experience Cloud. Dans ces exemples, les événements personnalisés suivants sont utilisés :

* **[!DNL Event-view-start]**: Exécutez au début de la vue de l’affichage/de l’état qui charge.
* **[!DNL Event-view-end]**: S’exécute lorsqu’un changement d’affichage/d’état se produit et que tous les composants SPA de la page se terminent par leur chargement. Il s’agit de l’événement qui envoie généralement des données à Adobe Analytics.
* **[!DNL Event-action-trigger]**: Exécutez lorsque un événement se produit sur la page, à l’exception du chargement d’affichage/d’état. Par exemple, un événement de clic ou un changement de contenu plus petit sans changement d’affichage.

Pour plus d’informations sur la manière et le moment de déclenchement de ces événements, reportez-vous aux pages et documents référencés ci-dessus. Vous n’avez pas besoin d’utiliser les mêmes noms d’événement dans votre mise en oeuvre. Le cas d’utilisation fonctionnel de la méthode utilisée est essentiel pour comprendre comme la bonne pratique recommandée pour chacune d’elles. La vidéo suivante présente un exemple SPA page et un exemple de code dans [!DNL Experience Platform Tags] qui écoute les événements personnalisés.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Exécutez s.t() ou s.tl() dans la variable [!DNL Experience Platform Tags] {#running-s-t-or-s-tl-in-the-launch-rule}

Un concept important à comprendre pour [!DNL Analytics] lorsque vous utilisez un SPA, la différence entre `s.t()` et `s.tl()`. Votre code déclenche l’une ou l’autre de ces méthodes dans [!DNL Experience Platform Tags] pour envoyer des données dans [!DNL Analytics].

* **s.t()** - &quot;t&quot; signifie &quot;track&quot;, et cela représente une page vue. Si l’affichage change suffisamment, vous pouvez  *considération* Il s’agit d’une nouvelle &quot;page&quot;, utilisez cet appel. Définissez une valeur unique sur la variable [!DNL s.pageName] et utiliser `s.t()` pour envoyer les données dans [!DNL Analytics].

* **s.tl()** - &quot;tl&quot; signifie &quot;suivre le lien&quot;, ce qui représente un clic sur les liens ou un petit changement de contenu. Si le changement d’affichage est minimal, utilisez `s.tl()` pour transmettre une valeur unique à propos de l’interaction à [!DNL Analytics]. Cette variable transmise n’est pas [!DNL s.pageName], car cela est ignoré dans Analytics lorsque `s.tl()` les appels sont reçus.

**CONSEIL :** En règle générale, si l’écran change de plus de 50 %, utilisez la variable `s.t()` appel de page vue. Sinon, utilisez `s.tl()`. Toutefois, faites preuve de jugement lorsque vous envisagez des actions qui constituent une nouvelle &quot;page&quot; et la manière dont elles doivent être présentées dans les rapports Adobe Analytics.

La vidéo suivante montre où et comment déclencher `s.t()` ou `s.tl()` dans Balises.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Effacer des variables {#clear-variables}

Envoyez les données appropriées dans [!DNL Analytics] au bon moment. Dans un environnement SPA, une valeur stockée dans un [!DNL Analytics] persiste et renvoie dans [!DNL Analytics], éventuellement lorsque vous ne le souhaitez plus. Une fonction existe dans la fonction [!DNL Analytics] [!DNL Tags] extension pour effacer les variables afin de garantir que l’appel suivant n’envoie pas de données de manière erronée dans [!DNL Analytics].

Le diagramme ci-dessus montre les variables effacées *after* vous envoyez des données. En réalité, cela peut se produire avant OU après l’appel, mais soyez cohérent dans votre [!DNL Experience Platform Tags] règles pour une mise en oeuvre plus propre. Si vous effacez des variables *before* vous exécutez `s.t()`, définissez les nouvelles variables immédiatement après l’appel , puis procédez à l’envoi des nouvelles données dans [!DNL Analytics].

**REMARQUE :** L’effacement des variables n’est pas toujours nécessaire lors de l’exécution `s.tl()`. Cet appel nécessite l’utilisation de la fonction [!DNL linkTrackVars] à indiquer [!DNL Analytics] les variables à définir. Cela se produit automatiquement. [!DNL Experience Platform Tags] via la configuration . Cela empêche les variables erronées de définir en contraste avec le comportement de `s.t()` appelle dans un environnement SPA. Pour garantir une mise en oeuvre la plus propre et la plus fiable, il est probablement plus facile d’utiliser la fonction clear variables pour les deux appels dans un environnement SPA.

La vidéo suivante montre où et comment effacer des variables dans [!DNL Tags].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Remarques complémentaires {#additional-considerations}

### Fenêtres Custom Code (Code personnalisé) dans [!DNL Experience Platform Tags] {#custom-code-windows-in-tags}

Dans le [!DNL Tags] [!DNL Analytics] , le code personnalisé peut être inséré à deux endroits : Le &quot;[!UICONTROL gestion des bibliothèques]&quot; et &quot;[!UICONTROL Configuration du dispositif de suivi à l’aide du code personnalisé]&quot;.

![Balises Fenêtres de code personnalisé Analytics](assets/launch_analyticscustomcodewindows.png)

L’un de ces emplacements exécute le code contenu une fois pour que la page initiale charge votre page SPA. Si le code doit s’exécuter sur une vue ou une modification d’action, implémentez-le dans le **[!UICONTROL règle]** (par exemple, &quot;chargement de page : event-view-end&quot;), pour vous assurer que le code s’exécute chaque fois que la variable [!UICONTROL règle] s’exécute. Lors de la création de l’action dans le [!UICONTROL règle], définit *Extension = Core* et *Type d’action = Code personnalisé*.

### SPA &quot;hybride&quot; et sites traditionnels {#hybrid-spa-and-traditional-sites}

Certains sites sont constitués d’une combinaison de pages traditionnelles et de pages SPA. Dans ce cas, utilisez une stratégie qui fonctionne pour les deux types de page. Lors de la configuration d’événements personnalisés sur le site et du déclenchement de règles dans [!DNL Experience Platform Tags], assurez-vous que les accès doubles ne sont pas envoyés dans [!DNL Analytics] en fonction des modifications de hachage, etc. Dans ce cas, supprimez l’une des pages vues pour empêcher la transmission de données en double dans Adobe Analytics.

Si vous décidez de séparer la fonctionnalité en une [!UICONTROL rules] pour plus de contrôle, pensez à documenter que vous avez fait cela. Si vous en modifiez un [!UICONTROL règle], apporter la même modification à l’autre [!UICONTROL règle].

### Intégration avec [!DNL Target] Utilisation d’A4T {#integration-with-target-using-a4t}

Lors de l’intégration à [!DNL Target] à l’aide d’A4T, vérifiez que la variable [!DNL Target] et [!DNL Analytics] les requêtes envoyées sur la même vue ou action transmettent la même valeur de paramètre SDID. Cela garantit que vos données se synchronisent correctement dans le serveur principal.

Pour afficher ces accès, utilisez un débogueur ou un outil de surveillance des paquets. Adobe fournit un débogueur Experience Platform à cet effet. Il s’agit d’une extension Chrome qui peut être [téléchargé ici](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob?hl=fr). [!DNL Target] doit s’exécuter en premier sur la page. Cela peut également être vérifié dans le débogueur.

## Ressources supplémentaires {#additional-resources}

* [Discussion sur les SPA sur les forums Adobe](https://experienceleaguecommunities.adobe.com:443/t5/adobe-experience-platform-launch/best-practices-for-single-page-apps/m-p/267940)
* [Sites d’architecture de référence pour montrer comment implémenter une application monopage dans Experience Platform Launch](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)
