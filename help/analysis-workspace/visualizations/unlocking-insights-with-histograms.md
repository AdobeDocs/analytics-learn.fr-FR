---
title: Déverrouillage des informations à l’aide d’histogrammes ; au-delà des moyennes dans Analytics
description: Découvrez l’impact des histogrammes dans les analyses pour obtenir des informations au-delà des moyennes.
feature: Visualizations
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-08-18T00:00:00Z
jira: KT-13833
thumbnail: KT-13833.jpeg
exl-id: 8712b293-4d31-4a2b-ada3-59c20094b1d3
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 1%

---

# Déverrouillage des informations à l’aide d’histogrammes : au-delà des moyennes dans Analytics

_Découvrez l’impact des histogrammes dans les analyses pour obtenir des informations au-delà des moyennes. Les histogrammes révèlent des schémas de données dans le comportement des clients, l&#39;engagement des visiteurs, les performances techniques et les erreurs de formulaire, ce qui permet d&#39;obtenir des informations plus approfondies et de prendre des décisions éclairées dans Adobe Workspace._

Sautons tout de suite. Vous devriez utiliser [histogrammes](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/histogram.html?lang=fr). Je vais expliquer pourquoi, mais je veux répondre à votre première question : Qu&#39;est-ce qu&#39;il y a dans le monde un histogramme ? Je comprends. La plupart du temps, quand vous voyez un tas de barres monter, vous pourriez penser que c&#39;est un graphique à barres. Oui, les histogrammes ont l&#39;air semblables, mais je vous assure, ils sont différents. Un graphique à barres compare des éléments, tandis qu’un histogramme indique la fréquence à laquelle une variable s’est produite. Jette un oeil ! Voici un graphique à barres :

![Graphique à barres 1](assets/bar-chart-1.png)

Nous avons six modèles, et nous pouvons comparer les revenus de chaque modèle. Nous voyons que le modèle de Johannesburg a le plus de revenus, alors que Berlin en a le moins.

Maintenant, regardons un histogramme :

![Histogramme 1](assets/histogram-1.png)

Au bas de l’axe X, nous avons le nombre d’unités achetées par chaque client. La première barre représente la fréquence à laquelle un client a acheté une unité, la seconde le nombre de clients qui ont acheté deux unités, etc., jusqu’à ce que les clients achètent dix unités ou plus.

Alors, en quoi est-ce utile ? Eh bien, nous voyons que la plupart des gens n&#39;achètent qu&#39;une seule unité. Il continue à décliner jusqu&#39;à ce que nous atteignions cinq unités. Puis il décline encore jusqu&#39;à ce que nous atteignions dix unités. Cela montre que les clients aiment vraiment acheter en multiples de cinq, et peut-être devrions-nous proposer des prix spéciaux ou des emballages pour en profiter. Mais il y a certainement beaucoup d&#39;autres utilisations.

## Présentation de l’engagement des visiteurs

Si votre site ou application repose sur le trafic répété, vous souhaitez connaître le nombre de visiteurs qui reviennent sur votre site ou votre application et la fréquence de leur retour. L’un des histogrammes les plus simples que vous puissiez utiliser consiste à déterminer le nombre de visiteurs qui reviennent plusieurs fois. Pendant que vous suivez cet histogramme au fil du temps, vous pouvez voir votre progression, avec un peu de chance les barres sur la droite deviennent plus grandes et celles sur la gauche plus courtes.

Peut-être que vous voulez garder les gens sur le site, lire des articles. Un histogramme montrant le nombre de visiteurs qui lisent différents nombres d’articles vous donne un aperçu du niveau d’engagement. Pourquoi est-ce utile ? Supposons que la plupart des visiteurs lisent un article et partent, mais certains visiteurs très actifs lisent trois articles et partent. C&#39;est une excellente information ! Vous savez maintenant que vous devez personnaliser la page du premier et du troisième articles lus dans le but d’inciter les visiteurs à lire un autre article.

## Compréhension du comportement des clients

Le propriétaire du produit pour les dossiers de patients dans un système hospitalier m&#39;a demandé des données. Il y avait six régions parmi lesquelles choisir pour obtenir votre dossier médical. Elle voulait savoir combien de personnes cliquaient sur plus d&#39;une. J’ai créé un histogramme qui montrait le nombre de visiteurs qui cliquaient sur les options 1, 2, 3, 4, 5 ou 6. Cela peut sembler excessif, mais plus de la moitié des visiteurs cliquaient sur au moins deux options et 3,2 % des visiteurs cliquaient sur les six options. Avec cet histogramme en face d&#39;elle, elle est passée à l&#39;action, a réorganisé sa feuille de route, et a simplifié les options jusqu&#39;à deux. Cela a rendu l&#39;expérience du patient beaucoup plus simple.

## Comprendre les performances techniques

Si vous configurez un histogramme pour le nombre de visiteurs qui rencontrent le nombre d’erreurs techniques, vous pouvez mieux comprendre les performances techniques de votre site. Un grand nombre de visiteurs qui rencontrent de nombreuses erreurs techniques est un signe pour commencer à hiérarchiser ces correctifs techniques.

## Compréhension des performances des formulaires

Les messages d’erreur d’un formulaire sont différents. Il s’agit d’erreurs du visiteur, et non d’erreurs de votre part. Vous pouvez toutefois bénéficier d’un histogramme qui indique le nombre de visiteurs qui rencontrent le nombre d’erreurs. Si un histogramme s’affiche indiquant que de nombreux visiteurs rencontrent de nombreuses erreurs, cela peut ne pas être de leur faute. Ce serait une bonne indication que votre formulaire comporte des champs mal nommés, des instructions peu claires, ou peut-être une conception qui masque les champs obligatoires.

## Pourquoi pas une mesure calculée ?

Vous pouvez vous demander en quoi cela diffère-t-il du simple fait d’avoir une mesure calculée ? Hé, j&#39;ai l&#39;air d&#39;une bonne mesure calculée. Je pense que ce sont des outils absolument essentiels pour comprendre les performances de votre site. Le problème pour la plupart des cas d&#39;utilisation que j&#39;ai répertoriés, cependant, est qu&#39;une moyenne peut vous montrer l&#39;ampleur du problème mais en obscurcir l&#39;étendue. Examinons comment les histogrammes vous donnent des informations supplémentaires pour certains des cas d’utilisation ci-dessus :

- Engagement du visiteur : si vous avez une moyenne d’articles lus sur 1.2, la personnalisation du premier article est assez évidente. Vous allez rater qu&#39;il y a un autre grand groupe qui sort après avoir lu le troisième article, ce qui est ce que l&#39;histogramme rend évident.

  ![Histogramme 2](assets/histogram-2.png)

- Erreurs techniques : si vous constatez une moyenne de 8,7 erreurs par visiteur, vous savez que vous avez rencontré un problème. L’histogramme peut vous montrer que 97 % des visiteurs rencontrent une ou moins d’erreurs, mais une poignée de valeurs aberrantes font augmenter la moyenne. Vous pourriez alors décider qu&#39;il ne vaut pas la peine de consacrer beaucoup de temps à améliorer l&#39;expérience pour ce petit groupe de valeurs aberrantes.

  ![Histogramme 3](assets/histogram-3.png)

- Erreurs de formulaire : si vous avez une moyenne de 3,6 messages d’erreur de formulaire par visiteur, c’est un indicateur d’un problème. Vous pourriez rencontrer le même problème plus aberrant que les erreurs techniques, mais il existe également des informations à tirer de la vue d’un pic dans l’histogramme à un nombre particulier d’erreurs. Un pic énorme à une erreur ? Il peut s’agir d’un problème courant rencontré par tous ces visiteurs ou d’une erreur différente qui s’est produite une seule fois. Un pic géant à trois erreurs ? Ah, maintenant c&#39;est intéressant. Si cela entraîne une enquête qui montre qu’il s’agit des mêmes trois erreurs, vous vous êtes intéressé aux données qui vous permettent de comprendre vos visiteurs et de résoudre ce qui est probablement un groupe de problèmes interconnectés.

  ![Histogramme 4](assets/histogram-4.png)

Comme vous pouvez le voir, les histogrammes n&#39;ont pas seulement leur propre utilité, ils approfondissent aussi l&#39;idée que vous gagnez d&#39;une moyenne. Il s’agit d’une visualisation prête à l’emploi dans Adobe Analytics et facile à créer. Heureusement, ces cas d&#39;utilisation vous sont utiles ou vous inspirent quelque chose. Bonne visualisation !

## Auteur

Ce document a été rédigé par :

![Gitai Ben-Ammi](assets/gitai-headshot.png)

**Gitai Ben-Ammi**, consultant principal chez Concentrix Catalyst

Adobe Analytics Champion
