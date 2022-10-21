---
title: Bonnes pratiques d’implémentation pour les applications monopages (SPA)
description: Découvrez quelques bonnes pratiques pour implémenter Adobe Analytics sur des applications monopages (SPA). Cela inclut l’utilisation de balises Experience Platform, la méthode d’implémentation recommandée.
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
workflow-type: ht
source-wordcount: '1313'
ht-degree: 100%

---

# Bonnes pratiques d’implémentation pour les applications monopages (SPA) {#implementation-best-practices-for-single-page-appliations}

Découvrez quelques bonnes pratiques pour implémenter [!DNL Adobe Analytics] sur des applications monopages (SPA). Cela inclut l’utilisation des [!DNL Experience Platform Tags], la méthode d’implémentation recommandée.

REMARQUES INITIALES :

* Le contenu ci-dessous fait référence à l’utilisation des [!DNL Experience Platform Tags] pour implémenter Adobe Analytics sur votre site. Ces considérations s’appliquent si les [!DNL Experience Platform Tags] ne sont pas utilisées. Dans ce cas, vous devrez les adapter à votre méthode d’implémentation.
* Il existe des différences entre les SPA. Vous devez donc ajuster votre approche en fonction de vos besoins.

## Schéma simple de l’utilisation des SPA dans les [!DNL Experience Platform Tags] {#simple-diagram-of-working-with-spas-in-tags}

![SPA pour Analytics dans les balises](assets/spa_for_analyticsinlaunch.png)

**REMARQUE :** il s’agit d’un schéma simplifié de la façon dont les pages SPA sont traitées dans une implémentation d’Adobe Analytics à l’aide des [!DNL Experience Platform Tags]. Les sections suivantes décrivent les étapes et les problèmes à prendre en compte.

## Définir la couche de données {#set-the-data-layer}

Lors du chargement d’un nouveau contenu ou d’une action sur une page SPA, *mettez à jour la couche de données en premier*. Cela doit se produire **avant** qu’un événement personnalisé qui déclenche l’exécution d’une règle ne s’exécute dans les [!DNL Experience Platform Tags]. Cela permet de s’assurer que les valeurs correctes de la couche de données sont transmises dans les balises, puis dans Adobe Analytics.

Voici un exemple de couche de données. L’un de ces éléments peut changer en fonction de l’affichage initial ou de sa modification ultérieure, compte tenu d’une action effectuée sur votre page SPA. Par exemple, lors d’un changement d’affichage complet ou majoritaire, il est courant de transmettre une valeur « [!DNL pageName] » unique pour différencier les affichages dans les rapports Adobe Analytics.

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

## Définir des événements personnalisés et les écouter dans les [!DNL Experience Platform Tags] {#setting-custom-events-and-listening-in-tags}

Lors du chargement d’un nouveau contenu ou d’une action sur la page SPA, les balises Experience Platform doivent être informées afin d’exécuter une règle qui envoie des données à [!DNL Analytics]. Il existe deux approches pour cela : [!UICONTROL Règles d’appel direct] ou Événements personnalisés.

* [!UICONTROL Règles d’appel direct] : configurez une [!UICONTROL règle d’appel direct] qui s’exécute lorsqu’elle est appelée directement à partir de la page. Si le chargement ou l’action de la page est simple ou unique et peut exécuter un ensemble spécifique d’instructions à chaque fois (par exemple, définir [!DNL eVar4] sur X et déclencher [!DNL event2] à chaque fois), cette approche sera adaptée. Pour plus d’informations sur la création de [!UICONTROL règles d’appel direct], voir la documentation des [!DNL Experience Platform Tags].
* Événements personnalisés : si vous devez joindre dynamiquement une payload avec des valeurs uniques pour les événements qui se produisent sur les pages SPA, utilisez des événements JavaScript personnalisés et écoutez-les dans les [!DNL Experience Platform Tags]. Utilisez la payload pour définir les éléments de données et les variables Analytics dans les balises. Cette méthode est considérée comme la bonne pratique, car ce besoin est généralement courant pour les SPA. Les exemples ci-dessous utilisent la méthode d’événements personnalisés.

**Exemples :** [ce document d’aide](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=fr) comporte des liens vers des exemples de sites SPA qui implémentent [!DNL Analytics] et d’autres solutions Experience Cloud. Dans ces exemples, les événements personnalisés suivants ont été utilisés :

* **[!DNL Event-view-start]** : s’exécute au démarrage d’affichage/d’état en cours de chargement.
* **[!DNL Event-view-end]** : s’exécute lorsqu’une modification d’affichage/d’état se produit et que tous les composants SPA de la page terminent leur chargement. Il s’agit de l’événement qui envoie généralement des données à Adobe Analytics.
* **[!DNL Event-action-trigger]** : s’exécute lorsqu’un événement se produit sur la page, à l’exception du chargement d’affichage/d’état. Il peut s’agir, par exemple, d’un événement de clic ou d’une modification de contenu plus petite sans changement d’affichage.

Pour plus d’informations sur comment et quand ces événements se déclenchent, reportez-vous aux pages et documents susmentionnés. Vous n’avez pas besoin d’utiliser les mêmes noms d’événement dans votre implémentation. Il est essentiel de comprendre le cas d’utilisation fonctionnel de la méthode utilisée, car il s’agit de la bonne pratique recommandée pour chacune. La vidéo suivante présente un exemple de page SPA et un exemple de code dans les [!DNL Experience Platform Tags] qui écoute les événements personnalisés.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Exécuter s.t() ou s.tl() dans les [!DNL Experience Platform Tags] {#running-s-t-or-s-tl-in-the-launch-rule}

Un concept important à comprendre pour [!DNL Analytics], lorsque vous utilisez une SPA, est la différence entre `s.t()` et `s.tl()`. Votre code déclenche l’une ou l’autre de ces méthodes dans les [!DNL Experience Platform Tags] pour envoyer des données dans [!DNL Analytics].

* **s.t()** : « t » signifie « track » (suivi) et correspond à une page vue. Si l’affichage change au point que vous le *considérez* comme une nouvelle « page », utilisez cet appel. Définissez une valeur unique sur la variable [!DNL s.pageName] et utilisez `s.t()` pour envoyer les données dans [!DNL Analytics].

* **s.tl()** : « tl » signifie « track link » (lien de suivi) et représente un clic sur les liens ou un petit changement de contenu. Si le changement d’affichage est minimal, utilisez `s.tl()` pour transmettre une valeur unique sur l’interaction à [!DNL Analytics]. Cette variable transmise n’est pas [!DNL s.pageName], car elle est ignorée dans Analytics lorsque des appels `s.tl()` sont reçus.

**CONSEIL :** en règle générale, si l’écran change de plus de 50 %, utilisez l’appel de page vue `s.t()`. Sinon, utilisez `s.tl()`. Toutefois, faites preuve de jugement lorsque vous envisagez des actions qui constituent une nouvelle « page » et la manière dont elles doivent être présentées dans les rapports Adobe Analytics.

La vidéo suivante montre où et comment déclencher `s.t()` ou `s.tl()` dans les balises.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Effacer des variables {#clear-variables}

Envoyez les données appropriées dans [!DNL Analytics] au bon moment. Dans un environnement SPA, une valeur stockée dans une variable [!DNL Analytics] peut persister et être renvoyée dans [!DNL Analytics], potentiellement lorsque vous ne le voulez plus. Une fonction existe dans l’extension [!DNL Analytics] [!DNL Tags] pour effacer les variables, de façon à s’assurer que l’appel suivant n’envoie pas par erreur des données dans [!DNL Analytics].

Le diagramme ci-dessus montre les variables effacées *après* avoir envoyé des données. En réalité, cela peut se produire avant OU après l’appel. Toutefois, restez cohérent dans la définition de vos règles [!DNL Experience Platform Tags] pour une implémentation plus épurée. Si vous effacez des variables *avant* d’exécuter `s.t()`, définissez les nouvelles variables immédiatement après l’appel, puis procédez à l’envoi des nouvelles données dans [!DNL Analytics].

**REMARQUE :** l’effacement des variables n’est pas toujours nécessaire lors de l’exécution de `s.tl()`. Cet appel nécessite l’utilisation de la variable [!DNL linkTrackVars] pour indiquer à [!DNL Analytics] les variables à définir. Cela se produit automatiquement sur [!DNL Experience Platform Tags] via la configuration. Cela empêche les variables errantes de définir en contraste avec le comportement avec les appels `s.t()` dans un environnement SPA. Pour garantir l’implémentation la plus épurée et la plus fiable, il est probablement plus facile d’utiliser la fonction d’effacement des variables pour les deux appels dans un environnement SPA.

La vidéo suivante montre où et comment effacer les variables dans les [!DNL Tags].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Remarques complémentaires {#additional-considerations}

### Fenêtres de code personnalisé dans les [!DNL Experience Platform Tags] {#custom-code-windows-in-tags}

L’extension [!DNL Tags] [!DNL Analytics] vous permet d’insérer du code personnalisé à deux endroits : les sections « [!UICONTROL Gestion des bibliothèques] » et « [!UICONTROL Configurer le dispositif de suivi à l’aide du code personnalisé] ».

![Fenêtres de code personnalisé des balises Analytics](assets/launch_analyticscustomcodewindows.png)

L’un de ces emplacements exécute le code contenu une fois pour que la page initiale charge votre page SPA. Si le code doit s’exécuter sur une modification d’action ou d’affichage, implémentez-le dans la **[!UICONTROL règle]** appropriée (par exemple, la règle « page load: event-view-end »), pour vous assurer que le code s’exécute chaque fois que la [!UICONTROL règle] s’exécute. Lors de la création de cette action dans la [!UICONTROL règle], définissez *Extension = Core* et *Type d’action = Code personnalisé*.

### Sites « hybrides » traditionnels et SPA {#hybrid-spa-and-traditional-sites}

Certains sites sont constitués d’une combinaison de pages traditionnelles et de pages SPA. Dans ce cas, utilisez une stratégie qui fonctionne pour les deux types de page. Lors de la configuration d’événements personnalisés sur le site et du déclenchement de règles dans les [!DNL Experience Platform Tags], assurez-vous que les accès doubles ne sont pas envoyés dans [!DNL Analytics] en fonction des modifications de hachage, etc. Dans ce cas, supprimez l’une des pages vues pour empêcher la transmission de données en double dans Adobe Analytics.

Si vous décidez de séparer la fonctionnalité en des [!UICONTROL règles] uniques pour plus de contrôle, pensez à documenter cette action. Si vous modifiez une [!UICONTROL règle], apportez la même modification à l’autre [!UICONTROL règle].

### Intégration à [!DNL Target] via A4T {#integration-with-target-using-a4t}

Lors de l’intégration à [!DNL Target] à l’aide d’A4T, vérifiez que les requêtes [!DNL Target] et [!DNL Analytics] envoyées sur le même affichage ou la même action transmettent la même valeur de paramètre SDID. Cela garantit que vos données se synchronisent correctement dans le serveur principal.

Pour afficher ces accès, utilisez un débogueur ou un outil de surveillance des paquets. Adobe fournit un débogueur Experience Platform à cet effet. Il s’agit d’une extension Chrome qui peut être [téléchargée ici](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob?hl=fr). [!DNL Target] doit s’exécuter en premier sur la page. Cela peut également être vérifié dans le débogueur.

## Ressources supplémentaires {#additional-resources}

* [Discussion sur les SPA sur les forums Adobe](https://experienceleaguecommunities.adobe.com:443/t5/adobe-experience-platform-launch/best-practices-for-single-page-apps/m-p/267940?profile.language=fr)
* [Sites d’architecture de référence pour montrer comment implémenter une application monopage dans Experience Platform Launch](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=fr)
