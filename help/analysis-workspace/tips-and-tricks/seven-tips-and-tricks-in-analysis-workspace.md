---
title: 7 conseils et astuces pour accélérer et faciliter la création de projets Analytics personnalisés
description: Analysis Workspace est un outil puissant intégré à Adobe Analytics qui peut vous aider à créer des projets dʼanalyse plus efficaces. Doté dʼun large éventail de fonctionnalités qui offrent puissance et échelle, il vous permet de réaliser n’importe quelle analyse à structure libre, tout en restant accessible grâce à son expérience utilisateur simple.
feature: Workspace Basics
topics: topics
activity: use
doc-type: feature video
team: Technical Marketing
kt: 3945
role: User, Developer, Data Engineer, Architect, Data Architect, Admin, Leader
level: Beginner
exl-id: af0e66cb-4e74-4ce0-9429-4a461fd54263
source-git-commit: 8fc641743bc9e07b838a22ca64ccc15344d52764
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 100%

---

# 7 conseils et astuces pour accélérer et faciliter la création de projets Analytics personnalisés

**Améliorez votre connaissance dʼAnalysis Workspace !**
Analysis Workspace est un outil puissant intégré à Adobe Analytics qui peut vous aider à créer des projets d’analyse plus efficaces. Doté dʼun large éventail de fonctionnalités qui offrent puissance et échelle, il vous permet de réaliser n’importe quelle analyse à structure libre, tout en restant accessible grâce à son expérience utilisateur simple.

## Création : rechercher les points de données pertinents

### ***Conseil 1 : dépôt des [!UICONTROL dimensions], [!UICONTROL périodes], [!UICONTROL segments] ou [!UICONTROL mesures] souhaités dans nʼimporte quelle partie de votre projet***

Pour ce faire, faites glisser, puis déposez un [!UICONTROL segment] ou tout autre composant dans la zone de dépôt de [!UICONTROL segments] en haut de nʼimporte quel panneau. Vous pouvez alors rapidement segmenter ce panneau en fonction de certains points de données. Par exemple, vous pouvez segmenter votre panneau pour nʼafficher que les accès pour lesquels des commandes existent en déposant la [!UICONTROL mesure] « commandes » dans la zone de dépôt de [!UICONTROL segments]. Vous pouvez même effectuer une segmentation en fonction des données qui nʼexistent pas dans un composant (par exemple pour afficher les accès sans commande) en déposant lʼélément de dimension « non spécifié » ou « aucun » dans la zone de dépôt de segments.

>[!VIDEO](https://video.tv.adobe.com/v/37601/?quality=12&learn=on&captions=fre_fr)

>[!TIP]
>
>**Essayez ceci :** le menu contextuel vous simplifie la tâche en un clic (droit). À partir de ce menu, vous pouvez accéder à de nombreux outils et fonctionnalités directement dans votre workflow Analysis Workspace. La prochaine fois que vous avez besoin dʼun outil ou dʼune fonctionnalité, cliquez avec le bouton droit pour voir sʼil est présent à portée de clic.

### ***Conseil 2 : création de mesures simples sans quitter votre workflow***

Grâce aux [!UICONTROL Mesures calculées] rapides, vous pouvez créer des [!UICONTROL mesures] directement dans Analysis Workspace, au lieu de passer par le Créateur de [!UICONTROL mesures calculées]. Sélectionnez simplement les colonnes des [!UICONTROL mesures] à calculer, puis, dans le menu contextuel, cliquez sur « [!UICONTROL Créer une mesure à partir de la sélection] ». Vous pouvez désormais ajouter, soustraire, diviser, multiplier et plus encore, sans quitter votre projet et interrompre le flux de vos idées.

>[!VIDEO](https://video.tv.adobe.com/v/41466/?quality=12&learn=on&captions=fre_fr)

>[!TIP]
>
>**Astuce :** vous pouvez sélectionner jusqu’à deux colonnes de [!UICONTROL mesures] en utilisant les [!UICONTROL Mesures calculées] rapides. Utilisez le Créateur de [!UICONTROL Mesures calculées] pour créer des [!UICONTROL mesures] qui comprennent plus de deux [!UICONTROL mesures].

## Visualisation : activation des données dans les projets

### ***Conseil 3 : copie et insertion de visualisations et de panneaux où vous le souhaitez***

Copiez en toute facilité les visualisations et les panneaux dʼun endroit et ajoutez-les à un autre, voire à un autre projet. Vous pouvez ainsi facilement déplacer les données au fur et à mesure que votre projet se développe et partager vos observations avec de nouveaux utilisateurs, afin quʼils nʼaient pas à recommencer une analyse depuis le début. Pour ce faire, cliquez avec le bouton droit sur le panneau ou la visualisation à copier, puis sélectionnez « [!UICONTROL Copier la visualisation] » et cliquez avec le bouton droit sur un panneau vierge pour l’insérer.

>[!VIDEO](https://video.tv.adobe.com/v/39122/?quality=12&learn=on&captions=fre_fr)

>[!TIP]
>
>**Fonctionnalité très demandée :** nos clients nous ont demandé de faciliter la copie et l’insertion de visualisations et de panneaux. Désormais, ils passent moins de temps à recréer des informations pertinentes et plus de temps à en découvrir de nouvelles.

### ***Conseil 4 : basculement entre les visualisations de granularité temporelle en un seul clic***

Modifiez facilement la vue temporelle des visualisations de tendances. Pour modifier la période dans les itérations précédentes dʼAnalysis Workspace, vous deviez afficher un tableau source, y faire glisser une nouvelle [!UICONTROL dimension], puis masquer à nouveau le tableau. Désormais, il suffit de sélectionner la granularité temporelle à afficher directement à partir du menu déroulant « [!UICONTROL Paramètres des visualisations] » (icône dʼengrenage en haut à droite).

>[!VIDEO](https://video.tv.adobe.com/v/41451/?quality=12&learn=on&captions=fre_fr)

## Partage : faciliter l’utilisation et la compréhension des résultats pour les autres utilisateurs

### ***Conseil 5 : création d’une [!DNL Virtual Report Suite] personnalisée pour des unités commerciales spécifiques***

Adobe Analytics collecte de grandes quantités de données. Grâce au traitement des composants dans les [!DNL Virtual Report Suites], les administrateurs peuvent créer un jeu de données pour chaque unité commerciale dʼune entreprise. Le bénéfice revient aux analystes à lʼœuvre dans Analysis Workspace, qui ne doivent pas se perdre dans des méandres de données pour trouver les informations souhaitées. Il vous suffit de cocher la case intitulée « [!UICONTROL Activer la personnalisation des composants de la suite de rapports virtuelle] » dans le Créateur de [!UICONTROL suites de rapports virtuelles], sous « [!UICONTROL Composants] », puis de sélectionner les [!UICONTROL composants] correspondant à ce que mesure une équipe spécifique.

>[!VIDEO](https://video.tv.adobe.com/v/3425531/?quality=12&learn=on&captions=fre_fr)

>[!TIP]
>
>**Astuce :** vous pouvez également modifier le nom des composants dʼune [!UICONTROL suite de rapports virtuelle] pour correspondre à la nomenclature dʼunités commerciales spécifiques. Il vous suffit de cliquer sur l’icône en forme de crayon, en regard du composant, puis de saisir un nouveau nom.

### ***Conseil 6 : création de liens vers des panneaux et visualisations au sein d’un projet ou entre plusieurs projets***

Créez des liens afin dʼamener les audiences où vous le souhaitez dans Analysis Workspace. Il vous suffit de cliquer avec le bouton droit sur le panneau vers lequel vous souhaitez créer un lien, de sélectionner « [!UICONTROL Obtenir le lien du panneau] », puis de copier. Ensuite, mettez en surbrillance le texte à partir duquel vous souhaitez créer un lien, sélectionnez lʼicône de lien dans lʼéditeur de texte dʼune zone de texte ou dʼune description, puis collez. Pour créer un lien vers un projet entier, il suffit de cliquer sur lʼonglet « [!UICONTROL Partage] », de sélectionner « [!UICONTROL Obtenir le lien du projet] » et de suivre les mêmes étapes que ci-dessus.

>[!VIDEO](https://video.tv.adobe.com/v/327480/?quality=12&learn=on&captions=fre_fr)

>[!TIP]
>
>**Astuce :** les liens permettent dʼaméliorer lʼexpérience de vos utilisateurs de plusieurs manières. Vous pouvez les diriger vers des illustrations reflétant les résultats et les recommandations des projets. Vous pouvez aussi leur permettre de passer directement de la table des matières aux sections qui les intéressent. Vous pouvez également créer des liens vers les projets dʼautres utilisateurs en rapport avec votre analyse.

### ***Conseil 7 : enregistrement de projets en tant que modèles personnalisés réutilisables***

Vous pouvez désormais transformer en toute facilité nʼimporte quel projet en un modèle personnalisé. Pour ce faire, sélectionnez « [!UICONTROL Enregistrer en tant que modèle] » dans le menu déroulant « [!UICONTROL Projet] », ajoutez des balises qui permettent de retrouver facilement le modèle, puis cliquez sur « [!UICONTROL Enregistrer le projet en tant que modèle] ». Le modèle est alors disponible pour tous les utilisateurs d’Analysis Workspace sous lʼonglet « [!UICONTROL Modèles personnalisés] ». Cela permet aux analystes de disposer de points de données pertinents dès le début de leurs projets, au lieu de partir dʼune feuille blanche.

>[!VIDEO](https://video.tv.adobe.com/v/3428573/?quality=12&learn=on&captions=fre_fr)

>[!TIP]
>
>**Fonctionnalité très demandée :** plusieurs clients nous ont demandé de rendre possible lʼenregistrement des projets en tant que modèles personnalisés. Nous avons répondu à leur demande et cette fonctionnalité est d’ores et déjà lʼune des plus populaires.

[Cliquez ici pour prendre connaissance d’autres conseils et astuces pour Experience League.](https://experienceleague.adobe.com/fr?search=tips&amp;lang=fr#recommended/solutions/analytics)

| À propos de l’auteur |            |
|------------|------------|
| ![Jen Lasser](assets/jlasser-headshot-s.jpg) | Jen Lasser est responsable de l’équipe de gestion de produit Adobe Analytics. <br> Cette fonction lui offre la possibilité de rencontrer des clients et de saisir leurs attentes sur le plan professionnel, <br>afin dʼen tenir compte dans lʼélaboration de la feuille de route dʼAdobe Analytics <br>et pour intégrer de nouvelles fonctionnalités de produit. Avant dʼoccuper son poste actuel, <br>Jen était consultante principale au sein de l’équipe de conseillers dʼAdobe. Ses <br>domaines dʼexpertise étaient la visualisation de données, Analysis Workspace et [!DNL Report Builder]. <br><br>Grâce à ses informations glanées auprès de nos clients, nous avons élaboré les conseils et astuces suivants pour <br>aider à faciliter la création, la visualisation et le partage de vos projets Analysis Workspace. |
