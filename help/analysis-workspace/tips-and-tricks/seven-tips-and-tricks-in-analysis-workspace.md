---
title: 7 Conseils et astuces pour faciliter et accélérer la création de projets Analytics personnalisés
description: Analysis Workspace est un outil puissant d’Adobe Analytics qui peut vous aider à créer des projets d’analyse plus pertinents. Il dispose d’un vaste ensemble de fonctionnalités qui vous permet d’effectuer n’importe quelle analyse de forme libre, mais d’une expérience utilisateur simple qui rend cette puissance et cette échelle accessibles.
feature: Concepts de base de Workspace
topics: topics
activity: use
doc-type: feature video
team: Technical Marketing
kt: 3945
role: User, Developer, Data Engineer, Architect, Data Architect, Admin, Leader
level: Beginner
exl-id: af0e66cb-4e74-4ce0-9429-4a461fd54263
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 0%

---

# 7 Conseils et astuces pour faciliter et accélérer la création de projets Analytics personnalisés

**Développez vos compétences Analysis Workspace !**
Analysis Workspace est un outil puissant d’Adobe Analytics qui peut vous aider à créer des projets d’analyse plus pertinents. Il dispose d’un vaste ensemble de fonctionnalités qui vous permet d’effectuer n’importe quelle analyse de forme libre, mais d’une expérience utilisateur simple qui rend cette puissance et cette échelle accessibles.

## Build : Exploration vers les points de données appropriés

### ***Conseil 1 : Déposez toute  [!UICONTROL dimension],  [!UICONTROL période],  [!UICONTROL segment] ou   mesure dans n’importe quelle partie de votre projet.***

Il vous suffit de faire glisser et de déposer un [!UICONTROL segment] ou tout autre composant dans la zone de dépôt [!UICONTROL segment] au haut d’un panneau, et vous pouvez rapidement segmenter ce panneau vers certains points de données. Par exemple, vous pouvez segmenter votre panneau pour afficher uniquement les accès pour lesquels des commandes existent en déposant la [!UICONTROL mesure] &quot;commandes&quot; dans la zone de dépôt [!UICONTROL segment]. Vous pouvez même segmenter par données qui n’existent pas dans un composant (pour afficher les accès sans commandes, par exemple) en déposant l’élément de dimension &quot;non spécifié&quot; ou &quot;aucun&quot; dans la zone.

>[!VIDEO](https://video.tv.adobe.com/v/24036/?quality=12)

>[!TIP]
>
>**Essayez ceci :** un monde d’efficacité vous attend dans le menu contextuel. Dans ce menu, vous pouvez accéder à de nombreux outils et fonctionnalités directement dans votre workflow Analysis Workspace. En cas de doute, cliquez avec le bouton droit pour voir si l’outil ou la fonctionnalité dont vous avez besoin est proche.

### ***Conseil 2 : Créer des mesures simples sans quitter votre workflow***

Avec les [!UICONTROL mesures calculées rapides], vous pouvez créer de nouvelles [!UICONTROL mesures] directement dans Analysis Workspace au lieu de vous rendre dans le créateur de [!UICONTROL mesures calculées]. Sélectionnez simplement les colonnes [!UICONTROL metric] que vous souhaitez calculer, puis, dans le menu contextuel, sélectionnez &quot;[!UICONTROL Créer une mesure d’après la sélection]&quot;. Maintenant, vous pouvez ajouter, soustraire, diviser, multiplier, et plus, sans quitter votre projet et rompre le cours de votre pensée.

>[!VIDEO](https://video.tv.adobe.com/v/23126/?quality=12)

>[!TIP]
>
>**Conseil utile :** Vous pouvez sélectionner jusqu’à deux colonnes de   mesures lors de l’utilisation de  [!UICONTROL mesures calculées rapides]. Utilisez le créateur [!UICONTROL Mesure calculée] pour créer des [!UICONTROL mesures] qui incluent plus de deux [!UICONTROL mesures].

## Visualiser : Activation des données dans les projets

### ***Conseil 3 : Copier et insérer des visualisations et des panneaux n’importe où***

Copiez facilement des visualisations et des panneaux d’un emplacement, puis ajoutez-les à un autre, même dans un autre projet. Cela signifie que vous pouvez facilement déplacer des données au fur et à mesure que votre projet se développe, et partager vos résultats avec de nouveaux utilisateurs afin qu’ils n’aient pas à lancer une analyse à partir de zéro. Il vous suffit de cliquer avec le bouton droit sur le panneau ou la visualisation à copier, de sélectionner &quot;[!UICONTROL Copier la visualisation]&quot; et de cliquer avec le bouton droit sur un panneau vierge pour l’insérer.

>[!VIDEO](https://video.tv.adobe.com/v/23230/?quality=12)

>[!TIP]
>
>**Fonctionnalité hautement requise :**  nos clients nous ont demandé de faciliter la copie et l’insertion de visualisations et de panneaux. Maintenant, ils passent moins de temps à recréer des idées, et plus de temps à en découvrir de nouvelles.

### ***Conseil 4 : Basculer entre les visualisations de granularité temporelle en un seul clic***

Modifiez facilement l’affichage du temps lorsque vous utilisez des visualisations de tendances. Dans les itérations Analysis Workspace précédentes, le changement de temps signifiait l’affichage d’une table source, le glissement dans une nouvelle [!UICONTROL dimension], puis le nouveau masquage de la table. Il est désormais aussi simple de sélectionner la granularité temporelle à démontrer directement dans le menu déroulant &quot;[!UICONTROL Paramètres des visualisations]&quot; (engrenage supérieur droit).

>[!VIDEO](https://video.tv.adobe.com/v/23548/?quality=12)

## Partager : Faciliter l’utilisation et la compréhension des résultats pour les autres

### ***Conseil 5 : Créer une personnalisation  [!DNL Virtual Report Suite] pour des entités commerciales spécifiques***

Adobe Analytics collecte de grandes quantités de données. Le traitement des composants dans [!DNL Virtual Report Suites] permet aux administrateurs de créer un jeu de données pour chaque unité opérationnelle d’une organisation. Cela signifie que les analystes travaillant dans Analysis Workspace n’ont pas à parcourir les données pour trouver ce qui leur importe le plus. Cochez simplement la case intitulée &quot;[!UICONTROL Activer la personnalisation des composants de suites de rapports virtuelles]&quot; dans le [!UICONTROL créateur de suites de rapports virtuelles] sous [!UICONTROL  &quot;Composants]&quot;, puis sélectionnez les [!UICONTROL composants] qui correspondent aux mesures d’une équipe spécifique.

>[!VIDEO](https://video.tv.adobe.com/v/23544/?quality=12)

>[!TIP]
>
>**Conseil utile :** vous pouvez également modifier le nom des composants d’une  [!UICONTROL suite de rapports ] virtuelle afin qu’il corresponde à la nomenclature de certaines unités opérationnelles. Il vous suffit de cliquer sur l’icône en forme de crayon en regard du composant et de saisir un nouveau nom.

### ***Conseil 6 : Lien vers des panneaux et des visualisations au sein d’un projet ou entre plusieurs projets***

Créez des liens qui amènent des audiences n’importe où dans Analysis Workspace. Cliquez avec le bouton droit de la souris sur le panneau auquel vous souhaitez créer un lien, sélectionnez &quot;[!UICONTROL Obtenir le lien du panneau]&quot;, puis copiez-le. Mettez ensuite en surbrillance le texte à partir duquel vous souhaitez créer un lien, sélectionnez l’icône de lien dans l’éditeur de texte d’une zone de texte ou d’une description, puis collez-la. Pour créer un lien vers un projet entier, cliquez simplement sur l’onglet &quot;[!UICONTROL Partager]&quot;, sélectionnez &quot;[!UICONTROL Obtenir le lien du projet]&quot; et procédez comme indiqué ci-dessus.

>[!VIDEO](https://video.tv.adobe.com/v/23724/?quality=12)

>[!TIP]
>
>**Conseil utile :** Il existe plusieurs façons d’améliorer l’expérience de vos lecteurs. Vous pouvez les pointer vers des illustrations qui correspondent aux résultats et aux recommandations dans les projets. Vous pouvez également leur permettre de passer d’une table des matières directement aux sections qui les intéressent. Vous pouvez également créer un lien vers les projets d’autres utilisateurs en relation avec votre analyse.

### ***Conseil 7 : Enregistrement de projets en tant que modèles personnalisés réutilisables***

Vous pouvez désormais facilement transformer n’importe quel projet en modèle personnalisé. Sélectionnez simplement &quot;[!UICONTROL Enregistrer comme modèle]&quot; dans le menu déroulant &quot;[!UICONTROL Projet]&quot;, ajoutez des balises qui facilitent la recherche du modèle, puis cliquez sur &quot;[!UICONTROL Enregistrer le projet comme modèle]&quot;. Désormais, le modèle sera disponible pour tous les utilisateurs d’Analysis Workspace sous l’onglet &quot;[!UICONTROL Modèles personnalisés]&quot;. Cela permet aux analystes de commencer leurs projets avec des points de données significatifs, au lieu de commencer à partir du point carré.

>[!VIDEO](https://video.tv.adobe.com/v/23231/?quality=12)

>[!TIP]
>
>**Fonctionnalité hautement requise :**  plusieurs clients nous ont demandé de rendre possible l’enregistrement de projets en tant que modèles personnalisés. Cette fonctionnalité est devenue l&#39;une de leurs préférées.

[Cliquez ici pour trouver d’autres conseils et astuces sur Experience League](https://experienceleague.adobe.com/?search=tips&amp;tag=Analysis+Workspace#recommended/solutions/analytics)

| À propos de l’auteur |  |
|------------|------------|
| ![Jen Lasser](assets/jlasser-headshot-s.jpg) | Jen Lasser est directeur de l’équipe de gestion de produits Adobe Analytics. <br> Dans ce rôle, elle rencontre les clients pour comprendre leurs besoins commerciaux, en  <br>utilisant ce qu’elle apprend pour informer la feuille de route du produit Adobe Analytics  <br>et donner la priorité aux nouvelles fonctionnalités du produit. Avant d’occuper son poste actuel, <br>Jen était consultante principale au sein de l’équipe de conseillers en Adobe, travaillant comme <br>experte en visualisation de données, Analysis Workspace et [!DNL Report Builder]. <br><br>Grâce à ses connaissances du monde réel, nous avons organisé les conseils et astuces suivants pour  <br>faciliter la création, la visualisation et le partage de vos projets Analysis Workspace : |
