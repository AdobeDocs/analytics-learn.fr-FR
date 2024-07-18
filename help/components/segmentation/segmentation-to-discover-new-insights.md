---
title: Maintenant, attendez un segment.. Utilisation de la segmentation pour découvrir de nouvelles informations dans Analysis Workspace.
description: Découvrez comment utiliser des segments dans Adobe Analytics pour découvrir de nouvelles informations à partir de vos visualisations Analysis Workspace et de vos tableaux à structure libre.
feature: Segmentation
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13268
thumbnail: KT-13268.jpeg
exl-id: 7743debd-57d8-4c79-a332-187180fc9701
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 1%

---

# Maintenant, attendez un segment.. Utilisation de segments pour découvrir de nouvelles informations dans Analysis Workspace.

Que vous soyez un nouvel utilisateur d’Adobe Analytics ou un professionnel chevronné, vous exploiterez les segments assez légèrement dans vos projets Analysis Workspace. Comme le décrit [Adobe Experience League](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=fr), &quot;les segments vous permettent d’identifier des sous-ensembles de visiteurs en fonction de caractéristiques ou d’interactions sur le site Web.&quot; Bien que le résultat de base de cette fonctionnalité signifie isoler des groupes d’utilisateurs, des visites ou des accès à votre site, un analyste perspicace comme vous peut obtenir des informations créatives avec cet outil et trouver de nouvelles façons d’obtenir des informations sur l’activité de votre site. La liste des options possibles est vaste. N’hésitez donc pas à essayer de créer la vôtre et de la partager avec d’autres personnes de votre entreprise ou en ligne dans des communautés comme la [communauté Adobe Analytics](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community?profile.language=fr) sur Experience League ou la communauté [#Measure Slack](https://www.measure.chat/).

Si vous avez besoin d’une actualisation rapide sur la création d’un segment, consultez la documentation Experience League sur l’utilisation du [créateur de segments](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=en) dans Analysis Workspace.

## Comparaison et contraste des segments

Dans Analysis Workspace, vous pouvez comparer deux segments à l’aide de &quot;[Comparaison de segments](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html?lang=fr)&quot;. La comparaison de segments se trouve dans la section Panneaux de la barre de navigation de gauche :

![Seg 01](assets/seg01.png)

Cependant, il arrive parfois que vous n’ayez pas besoin d’un panneau de comparaison complet pour fournir des informations clés à vos utilisateurs finaux. Heureusement, certaines fonctionnalités peuvent également être comparées dans un panneau standard.

La [visualisation de diagramme de Venn](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/venn.html?lang=fr) peut vous aider à créer une comparaison rapide, ce qui vous permet de survoler et de voir les sessions, commandes, utilisateurs, etc. qui se chevauchent. entre 2 et 3 segments personnalisés. Vous pouvez également créer rapidement des segments en cliquant avec le bouton droit de la souris sur l’une des sections qui se chevauchent :

![Seg 02](assets/s02.png)

Parfois, les informations importantes ne se trouvent pas dans les données qui se chevauchent, mais dans les données qui ne se chevauchent pas. Pour le visualiser rapidement, vous pouvez créer une copie d’un segment et en faire un segment &quot;Exclure&quot; :

![Seg 03](assets/s03.png)

En empilant votre segment &quot;exclusion&quot; avec l’autre segment dans votre comparaison, vous pouvez maintenant calculer rapidement le nombre de visites dans votre page de menu sans afficher également la page d’accueil dans la même session :

![Seg 04](assets/s04.png)

## Empiler l&#39;attaque

De même, vous pouvez créer les données d’intersection d’un diagramme de Venn en empilant simplement n’importe quel segment. Le nombre de segments ou de dimensions individuelles empilés n’est pas limité. Par exemple, si je voulais savoir rapidement quels jours de la semaine le mois dernier, mon site a eu une visite sur un téléphone portable, en particulier un Samsung Galaxy A52, qui a vu mes pages de menu et de nutrition, mais QUI N&#39;a PAS vu ma page d&#39;accueil, je peux la construire rapidement à la volée comme ceci :

![Seg 05](assets/s05.png)

Mais encore mieux, une fois que je trouve ce sous-ensemble parfait de mon utilisateur ou de ma base de visites, je peux sélectionner toutes ces valeurs, cliquer avec le bouton droit et créer instantanément un segment :

![Seg 06](assets/s06.png)

![Seg 07](assets/s07.png)

![Seg 08](assets/s08.png)

C&#39;est beaucoup de pouvoir dans un seul segment.

## Un segment de nombres pour un nombre de segments

De nombreux utilisateurs observent souvent les valeurs nominales, ordinales ou d’intervalle lors de la création de segments, par exemple une page visitée, une tranche d’âge d’utilisateurs ou le nombre de visites qu’un utilisateur a effectuées dans le passé. Cependant, vous pouvez également utiliser les données de rapport lors de la création d’un segment en regroupant ces valeurs, qu’il s’agisse de dimensions standard, de mesures standard ou de variables et de mesures personnalisées pour votre organisation.

Par exemple, la Durée de consultation de la page ou la Durée de la visite comporte des intervalles prédéfinis :

![Seg 09](assets/s09.png)

Cependant, elles peuvent ne pas toujours correspondre aux besoins de votre entreprise : la plupart des visites du site durent peut-être moins de 10 minutes. Vous pouvez utiliser la mesure granulaire pour créer des intervalles de taille différente. En voici une créée pour examiner les visites qui durent entre 1 minute, 1 seconde et 1 minute, 30 secondes :

![Seg 10](assets/s10.png)

Une fois créée, je peux désormais consulter mes visites, commandes et autres événements selon les différents groupes temporels regroupés que j’ai personnalisés :

![Seg 11](assets/s11.png)

Vous pouvez même commencer à examiner la manière dont vos indicateurs de performance clés (IPC) changent en fonction du temps passé par un utilisateur, du nombre de pages consultées au cours d’une visite, du nombre de visites passées ou de toute autre valeur numérique, ce qui vous permet d’examiner une mesure comme un facteur d’une autre mesure :

![Seg 12](assets/s12.png)

Les possibilités d’utilisation des segments pour trouver de nouvelles informations sont infinies. Ce n&#39;est qu&#39;un point de départ. Essayez-en quelques-unes par vous-même et faites savoir à la communauté ce que vous découvrez : [Adobe Analytics Community](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community?profile.language=fr) sur Experience League ou la communauté [#Measure Slack](https://www.measure.chat/).

Bonne segmentation !

## Auteur

Ce document a été rédigé par :

![Dan Cummings](assets/seg13.png)

**Dan Cummings**, chef d&#39;analyse d&#39;ingénierie produit chez McDonald&#39;s Corporation

Adobe Analytics Champion
