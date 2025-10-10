---
title: Faites passer un cap à votre analyse des données grâce aux Mesures calculées
description: Découvrez comment des personnes chevronnées utilisent les Mesures calculées pour créer des mesures sans modifier leur implémentation et utiliser des données déjà collectées pour répondre à des questions commerciales complexes.
feature: Calculated Metrics
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13266
thumbnail: KT-13266.jpeg
exl-id: 74793149-9967-4765-832c-c65e578ee34b
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1582'
ht-degree: 3%

---

# Faites passer un cap à votre analyse des données grâce aux Mesures calculées

La plupart des nouveaux utilisateurs d’Adobe Analytics connaissent les segments comme moyen de découper leurs données en tranches. Aujourd’hui, je souhaite vous présenter les mesures calculées, le prochain meilleur outil de votre boîte à outils d’analystes.

Les mesures calculées constituent une fonctionnalité avancée d’Adobe Analytics. Elles vous permettent de créer des mesures sans modifier votre implémentation à l’aide des données que vous avez déjà collectées. Le créateur de mesures calculées peut utiliser de nombreuses fonctions mathématiques et statistiques différentes afin que vous puissiez créer des mesures qui répondent même aux questions commerciales les plus complexes.

## Prise en main des mesures calculées

Pour commencer à utiliser des mesures calculées, prenons un exemple simple. Imaginez que vous souhaitiez comprendre si les utilisateurs en libre-service en ligne ont une valeur de commande moyenne (AOV) plus élevée que les utilisateurs assistés par appel. Pour créer une mesure calculée afin de répondre à cette question, procédez comme suit :

Pour ouvrir le créateur de mesures calculées, utilisez le volet de navigation supérieur pour cliquer sur → **Composants** → **Mesures calculées** → **+ Ajouter.** Ou, vous pouvez cliquer sur le signe **+**-dessus **Mesures** dans le panneau Composants.


![Calc 01](assets/calc01.png) ![Calc 02](assets/calc03.png) ![Calc 03](assets/calc02.png)

![Calc 04](assets/calc04.png)

*Descriptions ci-dessous des éléments de l’interface utilisateur*

Une fois que le créateur de mesures calculées s’ouvre, ajoutez et/ou procédez comme suit :

**A.** Nom de la mesure calculée. Ce nom s’affiche dans la liste des composants de mesures. Faites en sorte qu’il soit clair pour vous-même et pour les autres, comme *AOV du centre d’appels*.

**B.** Description de la mesure calculée. Cette description s’affiche lorsque les utilisateurs cliquent sur le bouton « **i** » en regard de la mesure dans la liste des composants. Assurez-vous donc qu’elle est informative. Par exemple, pour l’AOV du centre d’appels, nous pouvons ajouter *Calcule l’AOV pour les commandes assistées du centre d’appels*.

**C.** Format de la mesure : choisissez une décimale, une heure, un pourcentage ou une devise, puis ajoutez des décimales et une polarité. Ici, nous choisirons *Devise pour le Format, 0 pour le nombre de décimales, et* ⬆ *Bon (Vert) pour la polarité.*

**D**. Si vous utilisez des balises qui vous permettent d’appliquer des rubriques et de localiser rapidement des mesures calculées, ajoutez la ou les balises qui s’appliquent ici. Nous avons ajouté les balises *AOV* et *Call Center*.

**E.** Cette section est à afficher : lorsque vous créez votre mesure calculée dans la section F, la formule s’affiche ici.

**F.** Ici, vous allez faire glisser et déposer des dimensions (H), des mesures (I) ou des segments (J) pour créer votre mesure calculée, ainsi que les opérateurs pour la formule. Pour chaque mesure, si vous cliquez sur la roue dentée, vous pouvez modifier le Type de mesure (Standard/Total) et le Modèle d’attribution. *Nous ferons glisser et déposerons Revenu du centre d’appels, puis, en dessous, nous*÷￼*. Nous accepterons le type de mesure et le modèle d’attribution par défaut.*

****. Utilisez cette option **+Ajouter** pour ajouter des conditions supplémentaires ou des nombres statiques, dont nous n’avons pas besoin ici.

**K.** Enfin, lorsque vous créez votre calcul, vous pouvez prévisualiser les données des 90 derniers jours ici.

Maintenant que nous avons créé le centre d’appels AOV, nous avons également besoin d’une mesure calculée pour le centre d’appels AOV en ligne. Nous procéderions de la même manière que décrit ci-dessus.

Ensuite, nous pouvons créer une troisième mesure calculée, à l’aide du créateur de mesures calculées ou à la volée à partir du tableau à structure libre, pour comparer le centre d’appels et l’AOV en ligne afin d’obtenir un résultat similaire à celui-ci :

![Calc 05](assets/calc05.png)

Dans notre exemple, nous constatons un effet élévateur significatif lorsque les acheteurs utilisent le centre d’appel pour les aider à effectuer un achat. Ces données peuvent ensuite éclairer nos décisions sur la manière d&#39;aider les clients à obtenir de l&#39;aide concernant leurs achats, par exemple au moyen d&#39;offres contextuelles ou d&#39;autres expériences guidées.

## Utilisation de segments dans les mesures calculées

Maintenant, voyons comment nous pouvons utiliser les segments dans les mesures calculées pour obtenir plus d’informations d’insight sur le comportement, les préférences et les motivations des clients. Grâce aux segments et aux mesures calculées, nous pouvons en apprendre suffisamment sur les clients pour améliorer leur expérience, augmenter les revenus et améliorer la satisfaction et la fidélité de la clientèle.

Nous savons déjà, grâce aux exemples ci-dessus, que les achats assistés par centre d’appels ont généralement un AOV plus élevé. Cependant, d’autres mesures nous indiquent que la plupart des utilisateurs n’utilisent pas le centre d’appel pour les achats.

Alors, quelles catégories de vente au détail (et quels chemins d&#39;accès utilisateur à travers ces catégories), produisent le plus haut niveau de valeur ajoutée (AOV) ?  Nous pouvons le savoir en combinant des segments avec des mesures calculées.

Pour ce faire, nous devons d’abord créer des segments *inclure* et *exclure* au niveau des visites pour chaque catégorie de produits. L’option Inclure ou exclure est déterminée en cliquant sur l’engrenage **Options** dans le coin droit du conteneur. La valeur par défaut est Inclure.

![Calc 06](assets/calc06.png) ![Calc 07](assets/calc07.png)

Une fois ces segments créés, nous pouvons créer une mesure calculée pour vous donner la réponse à votre question. Nous ouvrons le créateur de mesures calculées et procédons comme suit :

1. Recherchez les segments que vous venez de créer, puis faites glisser et déposez ceux que vous souhaitez utiliser dans la zone grise située en haut de la zone **Définition**. Par exemple, si nous voulons créer un AOV pour les utilisateurs qui ont visité à la fois les catégories pour femmes et pour hommes, mais pas celle pour enfants, nous pouvons faire glisser ces trois segments vers cette zone : *Inclure les femmes*, *Inclure les hommes* et *Exclure les enfants*. Nous appelons cela *empilement de segments*.

   ![Calc 09](assets/calc09.png) ![Calc 08](assets/calc08.png)

1. Ensuite, nous effectuons un glisser-déposer de la mesure **Chiffre d’affaires en ligne** dans le même conteneur, puis **Commandes en ligne**. Les conteneurs fonctionnent comme des expressions mathématiques pour déterminer l’ordre des opérations. Par conséquent, les éléments qu’ils contiennent sont traités avant les processus suivants, bien que ce calcul ne contienne pas de conteneurs ou de processus multiples.
1. Nous modifions l’opérateur entre les deux mesures en division (÷).
1. Nous sélectionnons **Devise** comme format, **0** décimales et **UP** pour la polarité.
1. Nommez la mesure calculée et fournissez une description.
1. Enregistrez.

Lorsque nous avons terminé, notre mesure calculée ressemble à ceci :

![Calc 10](assets/calc10.png)

Après avoir créé des mesures calculées à l’aide de segments empilés pour chaque combinaison de parcours de catégorie de visiteurs et jeté un coup d’œil aux données, regardez ce que nous apprenons ! Les utilisateurs qui visitent à la fois les catégories pour femmes et pour hommes au cours de leur visite ont le plus haut niveau d’AOV et, par rapport aux visiteurs d’une seule catégorie, l’ascenseur est important :

![Calc 11](assets/calc11.png) ![Calc 12](assets/calc12.png)

Sachant cela, nous pouvons optimiser la mise en page, les emplacements de produits et les messages promotionnels pour attirer plus de personnes dans ces catégories avant de passer à la caisse.

## Précieux, mais pas disponible partout

**Ainsi, les mesures calculées, à la fois simples et complexes, sont extrêmement précieuses pour les analystes !**

Toutefois, ces mesures ne sont pas disponibles dans toutes les zones d’Adobe Analytics. Vous ne pouvez pas utiliser de mesures calculées dans :

- Abandons dans Analysis Workspace
- Analyse de cohortes dans Analysis Workspace
- Data Warehouse
- Rapports en temps réel
- Rapports Données actives
- Analytics for Target
- Report Builder

## Bonnes pratiques relatives aux mesures calculées

Maintenant que vous savez à quel point les mesures calculées peuvent être utiles, examinons quelques bonnes pratiques pour les créer.

1. **Vérifiez la syntaxe de la formule.** Assurez-vous que la syntaxe de la formule est correcte et suit la syntaxe Adobe Analytics pour vous assurer d’obtenir des informations significatives.
1. **Vérifier l’ordre des opérations.** Assurez-vous d&#39;utiliser les conteneurs avec précaution et de placer les choses dans l&#39;ordre mathématique approprié des opérations.
1. **Ne comptez pas deux fois les données**. Vous pouvez éviter de compter deux fois les données en vous assurant que la formule utilisée dans la mesure calculée ne compte pas les mêmes données plusieurs fois. Cela est souvent possible en combinant les conditions *Inclure* et *Exclure* dans la mesure calculée ou en utilisant des segments.
1. **Vérifier la granularité temporelle.** Assurez-vous que la mesure calculée a la même granularité temporelle que les mesures sources utilisées dans la formule.
1. **Utiliser des données précises :** vous n’obtiendrez de résultats précieux que si vous utilisez des données précises et fiables dans le calcul.

## Bonnes pratiques relatives aux segments personnalisés

Lors de la création de segments dans Adobe Analytics, gardez à l’esprit les bonnes pratiques suivantes :

1. **Restez simple.** Évitez de surcompliquer le segment. Gardez-le aussi simple que possible et utilisez uniquement les conditions nécessaires pour garantir la précision.
1. **Utilisez les types de conteneur appropriés**. Veillez à utiliser le type de conteneur correct (visiteur, visite ou accès) dans la définition de segment pour éviter d’obtenir des résultats incorrects.
1. **Ne comptez pas deux fois les données**. Comme pour les mesures calculées, assurez-vous que le segment ne compte pas les mêmes données plusieurs fois. Les conteneurs Inclure et Exclure peuvent s’avérer utiles.
   1. Lorsqu’un conteneur d’inclusion est utilisé, il *inclut* *tout le contenu de la visite* si un accès correspond à la condition de la visite.
   1. Lorsqu’un conteneur d’exclusion est utilisé, il *exclut tout le contenu de la visite* si un accès correspond à la condition de la visite.
1. **Imbriquez correctement les conteneurs**. Déterminez les données incluses à l’aide du conteneur le plus à l’extérieur, puis appliquez des règles imbriquées aux données restantes. Lors de l’application de règles imbriquées, le flux de segments agit comme un funnel et les règles suivantes ne s’appliquent pas aux accès exclus par la première règle.
1. **Vérifiez que vos données sont à jour.** Veillez à utiliser des données précises et à jour dans la définition de segment pour obtenir des résultats précis.
1. **Tester le segment.** Testez toujours le segment pour vous assurer qu’il fonctionne comme prévu avant de le diffuser à d’autres personnes.
1. **Tenez compte des performances.** Les segments peuvent ralentir le traitement des rapports. Tenez donc compte de cet impact lors de leur création.

## Points clés

La combinaison de segments et de mesures calculées dans Adobe Analytics peut absolument conduire à une analyse des données plus robuste et plus efficace. En découpant vos données et en créant des calculs à des fins de comparaison, vous pouvez obtenir des informations plus précises sur le comportement des clients afin d’optimiser vos campagnes marketing et créer des tableaux de bord et des rapports personnalisés. Toutefois, n’oubliez pas que les mesures calculées ne sont pas disponibles dans toutes les zones d’Adobe Analytics. Veillez également à suivre les bonnes pratiques pour vous assurer que vous obtenez des données précises et utiles.


## Auteur

Ce document a été rédigé par :

![Debbie Kern](assets/calc13.jpeg)

**Debbie Kern**, responsable principale d’Adobe Analytics chez Adswerve

![Adswerve](assets/calc14.png)
