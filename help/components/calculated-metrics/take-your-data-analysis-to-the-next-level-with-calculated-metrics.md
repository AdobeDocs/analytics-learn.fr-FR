---
title: Atteindre le niveau suivant de votre analyse de données avec des mesures calculées
description: Découvrez comment un expert pair utilise les mesures calculées pour créer de nouvelles mesures sans modifier leur mise en oeuvre et en utilisant les données déjà collectées pour répondre à des questions complexes.
feature: Calculated Metrics
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13266
thumbnail: KT-13266.jpeg
source-git-commit: c64f2fde1b91edd9f3d6c0f87aa889ed2c613d9b
workflow-type: tm+mt
source-wordcount: '1566'
ht-degree: 1%

---


# Atteindre le niveau suivant de votre analyse de données avec des mesures calculées

La plupart des nouveaux utilisateurs d’Adobe Analytics connaissent bien les segments comme moyen de découper et de découper leurs données. Aujourd’hui, je veux vous présenter les mesures calculées, le meilleur outil de votre boîte à outils d’analyse.

En tant que fonctionnalité avancée d’Adobe Analytics, les mesures calculées vous permettent de créer de nouvelles mesures sans modifier votre mise en oeuvre à l’aide des données que vous avez déjà collectées. Le créateur de mesures calculées peut utiliser de nombreuses fonctions mathématiques et statistiques différentes. Vous pouvez ainsi créer des mesures qui répondent aux questions les plus complexes de l’entreprise.

## Prise en main des mesures calculées

Pour commencer à utiliser les mesures calculées, prenons un exemple simple. Imaginez que vous souhaitiez déterminer si les utilisateurs en libre-service en ligne ont une valeur de commande moyenne (AOV) plus élevée que les utilisateurs assistés par des appels. Pour créer une mesure calculée afin de répondre à cette question, procédez comme suit :

Pour ouvrir le créateur de mesures calculées, utilisez le volet de navigation supérieur pour cliquer sur → **Composants** → **Mesures calculées** → **+ Ajouter.** Vous pouvez également cliquer sur le bouton **signe +** above **Mesures** dans le panneau Composants.


![Calc 01](assets/calc01.png) ![Calc 02](assets/calc03.png) ![Calc 03](assets/calc02.png)

![Calc 04](assets/calc04.png)

*Descriptions ci-dessous des éléments de l’interface utilisateur*

Une fois le créateur de mesures calculées ouvert, ajoutez et/ou procédez comme suit :

**A.** Nom de la mesure calculée. Ce nom s’affiche dans la liste des composants des mesures. Dès lors, rendez-le clair pour vous-même et pour les autres, comme *Centre d’appels AOV*.

**B.** Description de la mesure calculée. Cette description s’affiche lorsque les utilisateurs cliquent sur le signe **i**&quot; en regard de la mesure dans la liste des composants, veillez donc à ce qu’elle soit informative. Par exemple, pour la valeur de commande moyenne du centre d’appels, nous pouvons ajouter *Calcule la valeur de commande moyenne (AOV) pour les commandes assistées du centre d’appels*.

**C.** Format de mesure : Sélectionnez décimal, heure, pourcentage ou devise, puis ajoutez des décimales et de la polarité. Ici, nous choisirons *Devise pour le format, 0 pour le nombre de décimales et* ⬆ *Bon (vert) pour la polarité.*

**D**. Si vous utilisez des balises qui vous permettent d’appliquer des rubriques et de localiser rapidement des mesures calculées, ajoutez les balises qui s’appliquent ici. Nous avons ajouté *AOV* et *Centre d’appels* balises.

**E.** Cette section est destinée à l’affichage : lorsque vous créez la mesure calculée dans la section F, la formule s’affiche ici.

**F.** Vous allez ici faire glisser et déposer des dimensions (H), des mesures (I) ou des segments (J) pour créer votre mesure calculée ainsi que les opérateurs de la formule. Pour chaque mesure, si vous cliquez sur la roulette de rouage, vous pouvez modifier le type de mesure (standard/total) et le modèle d’attribution. *Nous allons glisser et déposer les recettes du centre d’appels, puis, en dessous, nous allons*÷ ￼*. Nous accepterons le type de mesure par défaut et le modèle d’attribution.*

**G**. Utilisez cette **+Ajouter** pour ajouter des conditions ou des nombres statiques supplémentaires, ce dont nous n’avons pas besoin ici.

**K.** Et enfin, quand vous construisez votre calcul, vous pouvez prévisualiser les données des 90 derniers jours ici.

Maintenant que nous avons créé la valeur de commande moyenne du centre d’appels, nous avons également besoin d’une mesure calculée pour la valeur de commande moyenne en ligne. Nous le ferions en suivant les mêmes étapes que celles décrites ci-dessus.

Ensuite, nous pouvons créer une troisième mesure calculée, à l’aide du créateur de mesures calculées ou à la volée dans le tableau à structure libre, pour comparer le centre d’appels et la valeur de commande moyenne en ligne afin de obtenir quelque chose comme ceci :

![Calc 05](assets/calc05.png)

Dans notre exemple, nous observons un effet élévateur significatif lorsque les acheteurs utilisent le centre d’appel pour les aider à effectuer un achat. Ces données peuvent ensuite informer nos décisions sur la manière d’aider les clients à obtenir de l’aide sur leurs achats, par exemple au moyen d’offres contextuelles ou d’autres expériences guidées.

## Utilisation de segments dans les mesures calculées

Examinons maintenant comment utiliser les segments dans les mesures calculées pour mieux comprendre le comportement, les préférences et les motivations des clients. Grâce aux segments et aux mesures calculées, nous pouvons en apprendre suffisamment sur les clients pour améliorer leur expérience, augmenter leurs recettes et améliorer la satisfaction et la fidélité de leurs clients.

Nous savons déjà d&#39;après les exemples ci-dessus que les achats assistés par le centre d&#39;appels ont généralement une valeur de commande moyenne supérieure. Cependant, d’autres mesures indiquent que la plupart des utilisateurs n’utilisent pas le centre d’appels pour les achats.

Par conséquent, quelles catégories de vente au détail - et chemins d’accès des utilisateurs dans ces catégories - génèrent la valeur de commande moyenne la plus élevée ?  Nous pouvons le découvrir en combinant des segments à des mesures calculées.

Pour ce faire, nous devons d’abord créer un niveau de visite *include* et *exclude* segments pour chaque catégorie de produits. L’inclusion ou l’exclusion est déterminée en cliquant sur le bouton **Options** dans le coin droit du conteneur. La valeur par défaut est Inclure.

![Calc 06](assets/calc06.png) ![Calc 07](assets/calc07.png)

Une fois ces segments créés, nous pouvons créer une mesure calculée afin de vous donner la réponse à votre question. Nous ouvrons le créateur de mesures calculées et procédez comme suit :

1. Recherchez les segments que vous venez de créer, puis faites glisser ceux que vous souhaitez utiliser dans la zone grise en haut de la page **Définition** de la boîte. Par exemple, si nous voulons créer une valeur de commande moyenne (AOV) pour les utilisateurs qui ont visité les catégories Femmes et Hommes, mais pas Enfants, nous pouvons faire glisser ces trois segments vers cette zone : *Inclure les femmes*, *Inclure les hommes*, et *Exclure les enfants*. Nous appelons cela *empilement de segments*.

   ![Calc 09](assets/calc09.png) ![Calc 08](assets/calc08.png)

1. Ensuite, faites glisser et déposez le **Recettes en ligne** dans le même conteneur, puis **Commandes en ligne**. Puisque les conteneurs fonctionnent comme des expressions mathématiques pour déterminer l’ordre des opérations, les éléments des conteneurs sont traités avant les processus suivants, bien qu’il n’y ait pas plusieurs conteneurs ou processus dans ce calcul.
1. Nous changeons l’opérateur entre les deux mesures en division (÷).
1. We Select **Devise** comme format, **0** décimales, et **UP** pour la polarité.
1. Nommez la mesure calculée et décrivez-la.
1. Enregistrer.

Lorsque nous avons terminé, la mesure calculée ressemble à ceci :

![Calc 10](assets/calc10.png)

Après avoir créé des mesures calculées à l’aide de segments empilés pour chaque combinaison du parcours de catégorie du visiteur et jeté un oeil aux données, découvrez ce que nous apprenons ! Les utilisateurs qui visitent les catégories Femmes et Hommes au cours de leur visite ont la valeur de commande moyenne la plus élevée et, par rapport aux visiteurs d’une seule catégorie, l’effet élévateur est significatif :

![Calc 11](assets/calc11.png) ![Calc 12](assets/calc12.png)

Sachant cela, nous pouvons optimiser la mise en page, les emplacements de produits et les messages promotionnels afin d’attirer plus de personnes dans ces catégories avant de les extraire.

## Valeur mais non disponible partout

**Ainsi, les mesures calculées, simples et complexes, sont très utiles aux analystes !**

Toutefois, ces mesures ne sont pas disponibles dans toutes les zones d’Adobe Analytics. Vous ne pouvez pas utiliser de mesures calculées dans :

- Abandons dans Analysis Workspace
- Analyse de cohortes dans Analysis Workspace
- Data Warehouse
- Rapports en temps réel
- Rapports Données actives
- Analytics for Target
- Report Builder

## Bonnes pratiques relatives aux mesures calculées

Maintenant que vous savez à quel point les mesures calculées peuvent être utiles, examinons quelques bonnes pratiques pour les créer.

1. **Vérifiez la syntaxe de votre formule.** Assurez-vous que la syntaxe de la formule est correcte et suit la syntaxe Adobe Analytics pour vous assurer que vous obtenez des informations significatives.
1. **Vérifiez l’ordre des opérations.** Assurez-vous d&#39;utiliser les conteneurs avec précaution et de mettre les objets dans l&#39;ordre mathématique approprié des opérations.
1. **Ne pas comptabiliser deux fois les données**. Vous pouvez éviter le double comptage des données en vous assurant que la formule utilisée dans la mesure calculée ne comptabilise pas les mêmes données plusieurs fois. Cela est souvent réalisé en combinant des *Inclure* et *Exclure* conditions dans la mesure calculée ou via l’utilisation de segments.
1. **Vérifiez la granularité temporelle.** Assurez-vous que la mesure calculée a la même granularité temporelle que les mesures source utilisées dans la formule.
1. **Utilisez des données précises :** Vous obtiendrez des résultats précieux uniquement si vous utilisez des données précises et fiables dans le calcul.

## Bonnes pratiques relatives aux segments personnalisés

Lors de la création de segments dans Adobe Analytics, tenez compte des bonnes pratiques suivantes :

1. **Restez simple.** Évitez de compliquer le segment de manière excessive. Soyez aussi simple que possible et utilisez uniquement les conditions nécessaires pour garantir la précision.
1. **Utilisation des types de conteneur appropriés**. Veillez à utiliser le type de conteneur correct (visiteur, visite ou accès) dans la définition de segment pour éviter d’obtenir des résultats incorrects.
1. **Ne pas comptabiliser deux fois les données**. Comme pour les mesures calculées, assurez-vous que le segment ne comptabilise pas plusieurs fois les mêmes données. Les conteneurs Inclure et Exclure peuvent vous aider.
   1. Lorsqu’un conteneur d’inclusion est utilisé, il *inclut* *tout le contenu de la visite* si un accès correspond à la condition dans la visite.
   1. Lorsqu’un conteneur d’exclusion est utilisé, il *exclut tout le contenu de la visite ;* si un accès correspond à la condition dans la visite.
1. **Imbriquer correctement les conteneurs**. Déterminez les données qui sont incluses à l’aide du conteneur le plus éloigné, puis appliquez des règles imbriquées aux données restantes. À mesure que les règles imbriquées sont appliquées, le flux de segments agit comme un entonnoir et les règles suivantes ne s’appliquent à aucun accès que la première règle a exclu.
1. **Assurez-vous que vos données sont à jour.** Veillez à utiliser des données exactes et à jour dans la définition de segment pour obtenir des résultats précis.
1. **Testez le segment.** Testez toujours le segment pour vous assurer qu’il fonctionne comme prévu avant de le publier sur d’autres segments.
1. **Tenez compte des performances.** Les segments peuvent ralentir le traitement des rapports. Tenez donc compte de cet impact lors de leur création.

## Points clés

La combinaison de segments et de mesures calculées dans Adobe Analytics peut conduire à une analyse des données plus robuste et plus efficace. En découpant et en divisant vos données et en créant des calculs à des fins de comparaison, vous pouvez obtenir des informations plus approfondies sur le comportement des clients, que vous pouvez utiliser pour optimiser vos campagnes marketing et créer des tableaux de bord et des rapports personnalisés. Toutefois, n’oubliez pas que les mesures calculées ne sont pas disponibles dans toutes les zones d’Adobe Analytics et veillez à suivre les bonnes pratiques pour vous assurer que vous obtenez des données précises et utiles.


## Auteur

Ce document a été rédigé par :

![Debbie Kern](assets/calc13.jpeg)

**Debbie Kern**, responsable Adobe Analytics senior chez Adobe

![Adswerve](assets/calc14.png)
