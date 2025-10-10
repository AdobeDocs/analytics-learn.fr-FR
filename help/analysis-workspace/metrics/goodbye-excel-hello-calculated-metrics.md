---
title: Au revoir Excel, bonjour les mesures calculées !
description: Dans cet article, découvrez les avantages des mesures calculées dans Adobe Analytics et la manière dont elles permettent d’obtenir une vue continue et dynamique de vos données.
feature: Calculated Metrics
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13178
thumbnail: KT-13178.jpeg
exl-id: d4f69244-6614-41f3-ac48-70adabb8a8e7
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1286'
ht-degree: 2%

---

# Au revoir Excel, bonjour les mesures calculées !

Dans cet article, découvrez les avantages des mesures calculées dans Adobe Analytics et la manière dont elles permettent d’obtenir une vue continue et dynamique de vos données.

Hé ! Pourquoi êtes-vous dans Excel en ce moment ? Je sais pourquoi. Il faut faire rapport pour s&#39;adresser aux bonnes personnes. Vous êtes occupé à saisir des données à partir d’Adobe Analytics, à calculer les taux de conversion, à les représenter graphiquement et à vous préparer à les placer toutes dans un document PowerPoint qui sera bientôt à l’attention des décideurs. J&#39;espère vraiment que vous utilisez au moins Report Builder pour le faire, mais je sais que certains d&#39;entre vous copiez et collez manuellement des données d&#39;un Workspace vers Excel.

Pourquoi ?

Pourquoi passer par un processus manuel tous les mois ? Pourquoi présenter une vue statique une fois par mois au lieu d’une vue continue et dynamique ? Pourquoi le copier dans PowerPoint ? Pourquoi ne pas créer directement des mesures calculées dans Adobe Analytics ?

## Les mesures calculées sont puissantes

Les mesures calculées sont puissantes, mais même les fonctions mathématiques de base sont vraiment utiles et une amélioration sérieuse par rapport aux mathématiques dans Excel. Examinons quelques-uns des avantages et quelques cas d’utilisation :

1. **Les mesures calculées sont actuelles et dynamiques**

   Lorsque vous exportez des nombres à partir d’Adobe Analytics, ils sont verrouillés à un moment donné. Vous devez absolument savoir comment s’est comporté votre site ou votre application le mois précédent, mais comment les décideurs suivent-ils l’évolution de la situation au milieu du mois ? Si votre taux de conversion plonge pendant un jour, puis revient à la moyenne à la fin du mois, le saurez-vous ? Cette chute pourrait être des données précieuses qui révèlent un important problème de télémétrie, ou plus important encore, un changement du comportement des visiteurs. Avec une mesure calculée, vous pouvez créer un graphique et l’afficher le jour même, ce qui vous permet de répondre.

1. **Les Mesures Calculées Vous Font Gagner Du Temps**

   J&#39;y suis allé. Copier/coller. Saisissez la formule ou faites glisser la cellule au-dessus vers le bas. Cliquez sur le graphique et modifiez la plage pour avoir les douze ou treize derniers mois. Copiez maintenant le graphique. Refais-le. Et encore. Et encore. Envoyez le fichier PowerPoint. C&#39;est fastidieux et chronophage, et on a l&#39;impression de devoir le faire tous les mois pour toujours.

   Au lieu de cela, vous pouvez créer un Workspace qui utilise votre mesure calculée, dont la période est définie sur Douze ou Treize derniers mois complets, et dont les données et le graphique sont automatiquement mis à jour au trait de minuit le premier jour de chaque mois. Les destinataires peuvent accéder directement au Workspace. Une copie PDF peut lui être automatiquement envoyée par e-mail le premier jour du mois ou après l’utilisation des visualisations textuelles pour ajouter votre commentaire sur les données (vous savez, la partie amusante du compte rendu des performances).

1. **Les mesures calculées peuvent être appliquées à de grands ensembles de données**

   Vous pouvez exporter tous les noms de produits dans Excel et commencer à calculer les taux de conversion et les recettes par visiteur, mais cela devient un problème lorsque vous en avez environ 100 000. Il ne s’agit pas d’un problème lié aux Mesures calculées. Placez votre dimension dans un tableau comme d’habitude, puis utilisez vos Mesures calculées comme mesures. Vous disposez désormais d’un tableau triable dynamique qui se met automatiquement à jour à mesure que des produits ou toute dimension que vous utilisez sont ajoutés à votre catalogue.

1. **Les Mesures Calculées Empêchent Les Erreurs**

   Des erreurs Excel se produisent. Nous y sommes tous allés. Diable, toute l&#39;économie de la Grèce et la réputation de deux éminents universitaires ont été ruinées à cause d&#39;une erreur de formule Excel. Vous n&#39;avez probablement pas d&#39;économie européenne reposant sur vos compétences Excel, mais il y a certainement une décision à prendre au sujet des budgets qui va changer en fonction de vos chiffres. Utiliser les mesures calculées signifie que vous pouvez créer une mesure, obtenir un contrôle qualité pour cette mesure, puis ne plus vous en soucier.

### Maintenant que nous avons passé en revue les avantages de l’utilisation de mesures calculées, regardons comment nous pouvons les mettre en pratique

**Cas D’Utilisation 1 : Taux De Conversion**

La plupart des taux de conversion ne sont qu’une simple division. Divisez le nombre de conversions par le nombre de visiteurs ou de visites. Divisez le nombre de pages vues pour la dernière page d’un funnel par le nombre de pages vues pour la première page d’un funnel. Divisez le nombre de clics internes de la campagne par le nombre d’impressions. Toutes ces actions peuvent être facilement effectuées sous forme de mesures calculées et placées dans un tableau de bord, tout en bénéficiant d’une faible latence des données, de visualisations mises à jour et d’une plus grande partageabilité.

**Cas d’utilisation 2 : recherche interne**

La recherche interne est l’un des outils les plus importants pour comprendre votre site. Les résultats de la recherche sur le site vous indiquent ce qui intéresse vos visiteurs et s’ils peuvent facilement le trouver par le biais de la navigation ou non. Vous devez être en mesure de dire si votre recherche de site fonctionne bien et utiliser un peu d&#39;ajout de base et de division peut vous donner cette réponse.

Commençons par les résultats de recherche. Vous souhaitez savoir si un terme de recherche obtient des résultats ou s’il n’évoque rien. Il s’agit généralement d’événements distincts. Voulez-vous vous donner la peine d’obtenir un troisième événement pour toutes les recherches internes sur le site ajoutées ? Au lieu de cela, faites une pause à vos développeurs et utilisez les Mesures calculées pour ajouter Recherche interne : Résultats et Recherche interne : Aucun résultat ensemble pour obtenir le nombre total de recherches internes.

Quel pourcentage de recherches ne renvoie aucun résultat ? Diviser la recherche interne : aucun résultat par cette nouvelle mesure calculée Nombre total de recherches internes . Vous savez maintenant s’il est urgent de créer du contenu correspondant à ces termes de recherche ou si votre équipe de contenu peut s’attaquer à des priorités plus élevées.

Nous voulons savoir combien de ces recherches avec des résultats obtiennent des clics et disposent généralement d’une mesure distincte pour cela également. Utilisez les Mesures calculées pour diviser le nombre de clics publicitaires par le nombre de fois que le terme a affiché des résultats de recherche sous forme de pourcentage. Vous disposez désormais du taux de clics pour chaque terme de recherche interne sur votre site. Vous pouvez isoler les termes de recherche qui génèrent des résultats inutiles. Il y a toutes les données historiques à votre disposition pour que vous puissiez les représenter graphiquement, et à mesure que vous apportez des améliorations, vous pouvez facilement voir s&#39;ils fonctionnent en regardant ce taux monter ou descendre.

Divisez le nombre de recherches internes par le nombre de visiteurs effectuant la recherche. Vous disposez de recherches par visiteur pour chaque terme. Si ce nombre est élevé (plus il est proche de 1,0, mieux c&#39;est), vous avez l&#39;un des deux problèmes possibles. Soit les résultats sur lesquels l’utilisateur clique sont erronés et ses visiteurs effectuent plusieurs recherches pour trouver les meilleurs résultats, soit ils ne parviennent pas à trouver les pages qu’ils recherchent via la navigation.

Comment pouvez-vous mesurer si ces pages clés sont accessibles via votre navigation ? Créez une mesure calculée pour les pages vues qui ont suivi une page de résultats de recherche vue. Divisez ce chiffre par le nombre total de pages vues pour cette page. Vous connaissez désormais le pourcentage de pages vues qui provient des résultats de recherche. Si vous avez un pourcentage élevé, vous avez probablement du travail à faire sur la navigation.

### Les Mesures Calculées Sont Puissantes

J’espère que cela vous a montré certaines des possibilités d’utiliser des fonctions mathématiques de base dans les Mesures calculées et que vous commencerez à en créer vous-même. Cela ne fait que commencer à décrire les possibilités des calculs que vous pouvez effectuer dans les mesures calculées, même avec quatre fonctions simples. Les mesures calculées peuvent vous aider à comprendre le comportement des visiteurs à un tout nouveau niveau. Une fois que vous en avez pris connaissance, vous avez ouvert la porte à l’utilisation de fonctions plus complexes qui sont également disponibles pour vous.

## Auteur

Ce document a été rédigé par :

![Portrait de Gittai](assets/gittai.png)

**Gitai Ben-Ammi**, consultant principal chez Concentrix Catalyst

Adobe Analytics Champion
