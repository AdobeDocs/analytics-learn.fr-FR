---
title: Comprendre le comportement de la clientèle à l’aide de l’Analyse des cohortes
description: Pour améliorer l’expérience client et les recettes, les entreprises doivent comprendre le comportement des clients. L’analyse des cohortes peut vous aider à comprendre l’engagement et la rétention, ce qui mène à des actions telles que l’amélioration de la création de comptes et la création de campagnes pour les mois de gros volume.
feature: Visualizations
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13213
thumbnail: KT-13213.jpeg
exl-id: 23dd43c5-47e4-46c7-88ee-66c7f62ca9cf
source-git-commit: d24bab984f57dbf197c5f6fb39d0a82e6fcf2ad2
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 13%

---

# Comprendre le comportement de la clientèle à l’aide de l’Analyse des cohortes

Pour améliorer l’expérience client et les recettes, les entreprises doivent comprendre le comportement des clients. L’analyse des cohortes peut vous aider à comprendre l’engagement et la rétention, ce qui mène à des actions telles que l’amélioration de la création de comptes et la création de campagnes pour les mois de gros volume.

L’analyse des performances numériques est essentielle pour comprendre comment les clients interagissent avec une entreprise et quelles actions peuvent être entreprises pour améliorer leur expérience. Dans cet article de blog, nous allons explorer comment utiliser l’analyse des cohortes pour mieux comprendre le comportement des clients.

## Partie 1 : Comparaison des performances numériques entre la première et la deuxième visite

### Définition de la scène

Un client cherche à comprendre les performances numériques au cours des 2 dernières années et envisage de développer un programme de fidélité pour stimuler les performances numériques. Tout d’abord, nous pouvons examiner la combinaison actuelle du site entre les nouveaux utilisateurs et les utilisateurs réguliers pour comprendre le comportement actuel des deux groupes de visiteurs.

Performances numériques actuelles

1. En 2022, 62 % des commandes provenaient de premières visites, contre 38 % de commandes de visites récurrentes (soumises à des cookies, appareils multiples).
1. Le taux de conversion des premières visites est légèrement plus élevé que celui des visites récurrentes pour les deux groupes, soit 11,6 % contre 11,4 %.
1. Par rapport à 2021, les taux de conversion ont diminué sur les deux segments.

![Tableau des visites](assets/cohort1.png)

## Partie 2 : Analyse des cohortes - Visites Arrangements comestibles Production mondiale

Pour comprendre l’affinité du canal numérique et l’opportunité de stimuler les acheteurs réguliers, la prochaine question à laquelle il faut répondre est la suivante : quel est le volume de visiteurs qui reviennent sur le site chaque mois en 2022 ?

### Présentation de l’analyse des cohortes

L’analyse des cohortes est un outil utile pour comprendre comment les cohortes interagissent avec une marque au fil du temps. Pour commencer, nous avons déterminé les questions auxquelles répondre :

1. Au cours d&#39;une année donnée, quelle est la période de conservation moyenne par mois?
1. Quel est le volume de visiteurs qui reviennent sur le site chaque mois au cours d’une année donnée ?
1. Quel est l’impact des connexions sur la rétention ?
1. Existe-t-il des produits spécifiques qui ont favorisé une rétention plus élevée ?

Configuration du tableau de cohortes

1. Définir la période de janvier à décembre 2022
1. **Critères d’inclusion :** Visites
1. **Critères de retour :** Visites
1. **Granularité :** Mois
1. **Paramètres :** calcul glissant
\*\*Permet de calculer la rétention en fonction de la colonne précédente, et non de la colonne incluse. Cela signifie donc qu’un utilisateur est inclus dans chacun des mois
1. **Segments :** vous pouvez sélectionner des segments spécifiques pour approfondir cette analyse
   1. Pages de destination spécifiques
   1. Type d&#39;appareil
   1. Canaux marketing
   1. Etc.

### Interpréter les résultats

**En 2022:**

1) Les mois avec les taux de rétention les plus élevés +1 mois incluent janvier, avril et novembre
1) Février et mai sont les mois les plus chargés
1) Environ 1 000 visiteurs et visiteuses reviennent sur le site chaque mois

Tableau de rétention ![2022](assets/cohort2.png)

**En 2021:**

1) Les mois avec les taux de rétention les plus élevés +1 mois incluent avril, janvier et mars
1) Février et mai sont les mois les plus chargés

Table de rétention ![2021](assets/cohort3.png)

**Éléments action:**

Créez un segment basé sur les 1 000 visiteurs et apprenez-en davantage sur eux :

- Où sont-ils situés ?
- Quels produits achètent-ils tout au long de l&#39;année ?
- De quels magasins achètent-ils ?

Les mois clés soulignent l’opportunité de stimuler la rétention en fonction du volume :

- Existe-t-il des tactiques spécifiques qui peuvent accroître l’affinité en février et mai pour tirer parti du volume ?

Analyse des répétitions des commandes pour comprendre les acheteurs réguliers

- Les taux de rétention les plus élevés pour les mêmes mois sont-ils de +1 mois ?
- Les mois de visite les plus élevés sont-ils les mêmes pour les commandes ?

## Partie 3 : ajout de deux mesures aux critères d’inclusion

### Comprendre l’impact de la connexion

Comme ce client cherche à comprendre la valeur d’un programme de fidélité, l’étape suivante de l’analyse incluait l’ajout de à l’événement de succès Connexion en tant que mesure Inclusion à la cohorte .

Attention : l’analyse des cohortes ne peut pas être utilisée pour les mesures calculées (comme le taux de conversion) ou les mesures non entières (comme le chiffre d’affaires). Seules les mesures pouvant être utilisées dans les segments peuvent être utilisées dans l’analyse des cohortes. En outre, elles ne peuvent être incrémentées que de >1 à la fois.

Le site est-il plus susceptible de conserver les utilisateurs qui se connectent ?

Quel serait l’impact si nous pouvions amener plus d’utilisateurs à se connecter ? Est-ce une expérience plus délicate ?

### Configuration du tableau de cohortes

1. **Définir la période :** janvier à décembre 2022
1. **Critères d’inclusion :** Visites + Événement de succès de connexion
1. **Critères de retour :** Visites
1. **Granularité :** Mois
1. **Paramètres :** calcul glissant
\*\*Permet de calculer la rétention en fonction de la colonne précédente, et non de la colonne incluse. Cela signifie donc qu’un utilisateur est inclus dans chacun des mois

### Interprétation des résultats

**En 2022:**

1) Les mois avec les taux de rétention les plus élevés +1 mois incluent janvier, avril et novembre (les mêmes mois que le tableau de première cohorte)
1) Les mois où le volume est le plus élevé sont février, mai et décembre
1) Il y a environ 2 500 visiteurs qui reviennent chaque mois \*\*plus que le double\*\*

**Éléments action:**

Examiner l’expérience utilisateur du site pour amener les utilisateurs à créer un compte lors du passage en caisse

![Tableau de cohorte 4](assets/cohort4.png)

## Partie 4 : cohorte Dimension personnalisée

Cohorte Dimension personnalisée : créez des cohortes basées sur la dimension sélectionnée plutôt que sur le temps (par défaut). Nombre de clients veulent analyser leurs cohortes en fonction d’autres aspects que le temps. La nouvelle fonctionnalité Cohorte de dimension personnalisée vous fournit la flexibilité de créer des cohortes en fonction des dimensions de votre choix. Utilisez des dimensions telles que le canal marketing, la campagne, le produit, la page, la région ou toute autre dimension dans Adobe Analytics de façon à afficher l’évolution de la rétention en fonction des différentes valeurs de ces dimensions. Le   

La définition de segment de cohorte Dimension personnalisée applique la dimension uniquement dans le cadre de la période d’inclusion, et non dans le cadre de la définition du renvoi.

Après avoir choisi l’option Cohorte Dimension personnalisée , vous pouvez faire glisser et déposer la dimension de votre choix dans la zone de dépôt. Cela vous permet de comparer des éléments de dimension similaires sur la même période. Par exemple, vous pouvez comparer les performances des villes côte à côte

côté, produits, campagnes, etc. Il renvoie vos 14 principaux éléments de dimension. Cependant, vous pouvez utiliser un filtre (accessible en survolant la partie droite de la dimension déposée) pour afficher uniquement les éléments de dimension désirés. Une cohorte de dimension personnalisée ne peut pas être utilisée avec la fonctionnalité de tableau de latence.

### Quels produits sont à l&#39;origine de l&#39;affinité du site ?

Le tableau de cohorte Dimension personnalisé met en évidence les produits qui génèrent des taux de rétention plus élevés que la moyenne.  Ce tableau permet d’identifier vos meilleurs produits afin de générer des campagnes marketing internes et externes avec les produits les plus intéressants.

**En février**, 3 produits se démarquent avec des taux de rétention plus élevés

1) Product 1
1) Product 2
1) Product 3

**En mars :**

1) Product 1
1) Product 2
1) Produit 3 : surpasse souvent avec un taux de rétention plus élevé que la rétention moyenne.

![Tableau de cohorte 5](assets/cohort5.png)

## Conclusion

L’analyse des cohortes et la cohorte Dimension personnalisée sont des outils puissants pour comprendre le comportement des clients et améliorer les performances numériques. En analysant les taux de rétention, les taux de connexion et l’impact de produits spécifiques, les entreprises peuvent prendre des décisions basées sur les données afin d’améliorer l’expérience client et stimuler la croissance.

## Auteur

Ce document a été rédigé par :

![Jennifer Yacenda](assets/jennifer-yacenda.png)

**Jennifer Yacenda**, directrice principale chez Marriott

Adobe Analytics Champion
