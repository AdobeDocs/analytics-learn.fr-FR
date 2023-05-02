---
title: Adieu Excel, bonjour des mesures calculées
description: Découvrez les avantages de l’utilisation des mesures calculées dans Adobe Analytics et comment elles peuvent vous fournir une vue continue et dynamique de vos données dans cet article.
feature: Calculated Metrics
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13178
thumbnail: KT-13178.jpeg
source-git-commit: 28db96c38e5318942ddc9f39ec0a2d561e14200c
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%

---


# Adieu Excel, bonjour des mesures calculées

Découvrez les avantages de l’utilisation des mesures calculées dans Adobe Analytics et comment elles peuvent vous fournir une vue continue et dynamique de vos données dans cet article.

Hé ! Pourquoi êtes-vous dans Excel en ce moment ? Je sais pourquoi. Vous avez des rapports pour atteindre les bonnes personnes. Vous êtes occupé à saisir des données provenant d’Adobe Analytics et à calculer des taux de conversion, à les tracer et à vous préparer à les placer tous dans un PowerPoint qui s’adresse aux décideurs. J&#39;espère vraiment que vous utilisez au moins le Report Builder pour le faire, mais je sais que certains d&#39;entre vous copient et collent manuellement des données d&#39;un espace de travail vers Excel.

Pourquoi ?

Pourquoi passer par un processus manuel chaque mois ? Pourquoi présenter une vue statique une fois par mois au lieu d’une vue continue et dynamique ? Pourquoi le copier dans PowerPoint ? Pourquoi ne pas créer directement des mesures calculées dans Adobe Analytics ?

## Les mesures calculées sont puissantes

Les mesures calculées sont puissantes, mais même les fonctions mathématiques de base sont vraiment utiles et offrent une amélioration sérieuse par rapport aux maths dans Excel. Examinons certains avantages et certains cas pratiques :

1. **Les mesures calculées sont actuelles et dynamiques**

   Lorsque vous exportez des nombres depuis Adobe Analytics, ils sont verrouillés à un moment donné. Vous avez absolument besoin de savoir comment votre site ou application a fonctionné le mois précédent, mais comment les décisionnaires peuvent-ils garder une trace de la façon dont les choses évoluent au milieu du mois ? Si votre taux de conversion plonge pendant un jour, puis revient à la moyenne d’ici la fin du mois, le sauriez-vous ? Ce plongeon pourrait être de précieuses données qui révèlent un problème de télémétrie important, ou encore plus essentiel, un changement dans le comportement des visiteurs. Avec une mesure calculée, vous pouvez la représenter sous forme graphique et la voir le jour où elle se produit, ce qui vous laisse prêt à répondre.

1. **Les mesures calculées vous font gagner du temps**

   J&#39;y ai été. Copiez/collez. Entrez la formule ou faites glisser la cellule au-dessus vers le bas. Cliquez sur le graphique et modifiez la plage pour obtenir les douze ou treize derniers mois. Copiez maintenant le graphique. Maintenant, recommencez. Et encore une fois. Et encore une fois. Envoyez le PowerPoint. C&#39;est fastidieux et chronophage, et c&#39;est comme si vous deviez le faire tous les mois pour toujours.

   Vous pouvez à la place créer un espace de travail qui utilise votre mesure calculée, dont la période correspond aux 12 ou 13 derniers mois complets, et dont les données et le graphique sont automatiquement mis à jour au contour de minuit le premier jour de chaque mois. Les destinataires peuvent avoir un accès direct à Workspace. Une copie de PDF peut leur être automatiquement envoyée par courriel le premier jour du mois ou après que vous avez utilisé les visualisations de texte pour ajouter vos commentaires sur les données (vous savez, la partie amusante des rapports).

1. **Les mesures calculées peuvent être appliquées à de grands ensembles de données**

   Vous pouvez exporter tous les noms de produits dans Excel et commencer à calculer les taux de conversion et les recettes par visiteur, mais cela devient fastidieux lorsque vous en avez environ 100 000. Aucun problème avec les mesures calculées. Déposez votre dimension dans un tableau comme vous le faites habituellement, puis utilisez vos mesures calculées comme mesures. Vous disposez maintenant d’une table de tri dynamique qui se met à jour automatiquement lorsque des produits ou toute dimension que vous utilisez sont ajoutés à votre catalogue.

1. **Mesures calculées : éviter les erreurs**

   Des erreurs Excel se produisent. Nous y avons tous été. Heck, toute l&#39;économie de la Grèce et la réputation de deux éminents universitaires ont été ruinées à cause d&#39;une erreur de formule Excel. Vous n&#39;avez probablement pas d&#39;économie européenne basée sur vos compétences Excel, mais il y a certainement une décision sur les budgets qui vont changer en fonction de vos chiffres. L’utilisation des mesures calculées signifie que vous pouvez créer une mesure, lui demander un contrôle qualité, puis ne plus vous en soucier.

### Maintenant que nous avons passé en revue les avantages de l’utilisation des mesures calculées, regardons comment nous pouvons les mettre en pratique.

**Cas d’utilisation 1 : Taux de conversion**

La plupart des taux de conversion ne sont que des divisions simples. Divisez le nombre de conversions par le nombre de visiteurs ou de visites. Divisez le nombre de pages vues pour la dernière page d’un entonnoir par le nombre de pages vues pour la première page d’un entonnoir. Divisez le nombre de clics publicitaires de campagne internes par le nombre d’impressions. Toutes ces tâches peuvent facilement être effectuées sous forme de mesures calculées et placées dans un tableau de bord avec une faible latence des données, une mise à jour des visualisations et une plus grande partageabilité.

**Cas d’utilisation 2 : Recherche interne**

La recherche interne est l’un des outils les plus importants pour comprendre votre site. Les résultats de la recherche sur le site vous indiquent ce qui intéresse vos visiteurs et s’ils peuvent facilement le trouver par le biais de la navigation ou non. Vous devez être en mesure de déterminer si la recherche de votre site fonctionne bien et l’utilisation d’un peu d’ajout et de division de base peut vous donner cette réponse.

Commençons par les résultats de la recherche. Vous voulez savoir si un terme de recherche obtient des résultats ou n’apporte rien. Il s’agit généralement d’événements distincts. Voulez-vous avoir la difficulté d’obtenir un troisième événement pour toutes les recherches de site internes ajoutées ? Faites plutôt une pause à vos appareils et utilisez les mesures calculées pour ajouter la recherche interne : Résultats et recherche interne : Aucun résultat pour obtenir le total des recherches internes.

Quel pourcentage de recherches ne renvoient aucun résultat ? Diviser la recherche interne : Aucun résultat par cette nouvelle mesure calculée Total des recherches internes . Vous savez maintenant si la création de contenu pour ces termes de recherche est urgente ou si votre équipe de contenu peut s’attaquer à des priorités plus élevées.

Nous voulons savoir combien de ces recherches avec résultats obtiennent des clics publicitaires et ont généralement une mesure distincte pour cela également. Utilisez les mesures calculées pour diviser le nombre de clics publicitaires par le nombre de fois où ce terme a généré des résultats de recherche et les afficher sous forme de pourcentage. Vous disposez maintenant du taux de clics pour chaque terme de recherche interne de votre site. Vous pouvez isoler les termes de recherche qui génèrent des résultats peu utiles. Il contient toutes les données historiques pour que vous puissiez les tracer, et en améliorant, vous pouvez facilement voir s&#39;ils travaillent en regardant ce taux monter ou descendre.

Divisez le nombre de recherches internes par le nombre de visiteurs effectuant une recherche. Vous avez des recherches par visiteur pour chaque terme. Si ce nombre est élevé (plus il est proche de 1,0, mieux c&#39;est), vous avez l&#39;un des deux problèmes possibles. Les résultats sur lesquels le visiteur clique sont mauvais et les visiteurs effectuent plusieurs recherches pour trouver les meilleurs résultats, ou ils ne trouvent pas les pages qu’ils recherchent par le biais de la navigation.

Comment pouvez-vous mesurer si ces pages clés peuvent être recherchées par le biais de votre navigation ? Créez une mesure calculée pour les pages vues qui ont suivi une page vue de résultats de recherche. Divisez cette valeur par le nombre total de pages vues pour cette page. Vous connaissez maintenant le pourcentage de pages vues provenant des résultats de la recherche. Si vous avez un pourcentage élevé, vous avez probablement du travail à faire sur la navigation.

### Les mesures calculées sont puissantes

J’espère que cela vous a montré certaines des possibilités d’utilisation des fonctions mathématiques de base dans les mesures calculées et que vous commencerez à en créer vous-même. Cela commence uniquement à décrire les possibilités de maths que vous pouvez faire dans les mesures calculées, même avec quatre fonctions simples. Les mesures calculées peuvent vous aider à comprendre le comportement des visiteurs à un niveau entièrement nouveau. Une fois que vous en avez l’air, vous avez ouvert la porte à l’utilisation de fonctions plus complexes qui vous sont également disponibles.

## Auteur

Ce document a été rédigé par :

![Capture d&#39;écran de Gittai](assets/gittai.png)

**Gitai Ben Ammi**, consultant principal chez Concentrix Catalyst

Adobe Analytics Champion
