---
title: Piratages simples pour une plus grande efficacité et un libre-service - 1ère partie
description: Découvrez les principaux défis auxquels sont confrontées les équipes d’analyse et nos recommandations pour les surmonter à l’aide de stratégies en dehors de l’interface utilisateur d’Adobe Analytics.
solution: Analytics
exl-id: 5d1077fd-d006-4a85-bf1c-54f6b2d31934
source-git-commit: dad200fdb5c5d15c00254d693fb47bbcec80afaf
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 0%

---

# Adobe Analytics : Des pirates simples pour une plus grande efficacité et un libre-service

**Partie 1 : En dehors de l’interface utilisateur**

Cet article décrit les principaux défis auxquels sont confrontées les équipes d’analyse aujourd’hui et nos recommandations pour les surmonter à l’aide de stratégies en dehors de l’interface d’Adobe Analytics.

## Principaux défis pour les équipes Analytics

De nombreuses équipes d’Analytics se trouvent avec une répartition déséquilibrée du travail. Au lieu d’un mélange d’analyse à 80 % et de mise en oeuvre à 20 %, de nombreuses organisations se trouvent dans l’inverse de cela. Ils voient que la plupart de leurs efforts ont été consacrés à la configuration, à la création de rapports et à la fourniture d’un soutien plutôt qu’à la production d’analyses générant des informations de grande valeur.

Les équipes d’Analytics trouvent leur productivité et leur efficacité épuisées pour diverses raisons. Il s’agit notamment des implémentations en constante évolution, de la volonté de maintenir la confiance de l’organisation dans les données et de la réduction du roulement des analystes. La réduction du chiffre d’affaires permet d’éviter le long processus de formation des nouveaux membres de l’équipe à l’utilisation d’outils d’implémentation personnalisés et inconnus.

D&#39;autres défis majeurs auxquels sont confrontés les analystes :

* **Concurrence :** Les commerces de détail en ligne et multicanaux deviennent plus compétitifs.
* **attentes du client :** Les expériences client et les stratégies marketing deviennent plus complexes.
* **Valeur de données :** La valeur de données et d’informations précises pour générer un avantage concurrentiel augmente.
* **Attentes des parties prenantes :** Les partenaires commerciaux, les parties prenantes et les cadres supérieurs demandent de plus en plus de données avant approbation.
* **Gestion de projet :** L’équipe d’analyse se noie dans les demandes de mise en oeuvre de la collecte de données pour un flux sans fin de nouvelles fonctionnalités, tout en produisant des rapports précis, en embarquant de nouveaux analystes et en découvrant les nouvelles informations suivantes.

## Raccourcis clavier : En dehors de l’interface utilisateur

1. Conservez votre [Référence de conception de solution](/help/implementation/implementation-basics/creating-and-maintaining-an-sdr.md) (DTS) à jour :

   * Le DTS est la Principale source de vérité pour la définition et l’utilisation prévue de toutes les variables dans votre implémentation d’Analytics.
   * Le DTS est la référence principale que les utilisateurs doivent connaître pour tirer parti de l’interface utilisateur d’Adobe Analytics.
   * Il est important de le conserver à jour et versionné (un format de date simple peut être utilisé).

1. Documentation et gouvernance de la collecte de données - spécifications techniques :

   La spécification technique a une audience plus limitée que le DTS, mais elle est aussi importante, sinon plus, pour une mise en oeuvre entièrement fonctionnelle. Toutes les ressources de développement, d’assurance qualité et de gestion des balises nécessaires à la mise en oeuvre de la solution doivent être de bonnes spécifications techniques. Veillez à conserver autant de documents que nécessaire pour s’adapter à des architectures d’implémentation uniques.

   **Tech Spec**

   _Cas pratique :_ Instructions décrivant comment créer des scripts pour la collecte de données

   _Utilisateurs Principal :_ Développeurs

   _Autres notes:_

   * Document hautement technique conçu spécifiquement pour vos environnements de déploiement
   * Utile à la fois pour la mise en oeuvre initiale et la maintenance/référence ultérieure
   * Organisé par type de solution (suivi de campagne, métadonnées de page, etc.)
   * Le document Principal doit être mis à jour et conservé au fur et à mesure que les modifications du DTS sont apportées
   * Référentiel central
   * Numéros de version synchronisés pour le SDR et les spécifications techniques

1. Communication et document de l’intention de conception de la solution au lancement :

   * Communication avec l’utilisateur en tête
   * Lorsque vous lancez ou améliorez la collecte de données, créez des résumés simples qui peuvent être partagés avec les parties prenantes.
   * Renforcer l’utilisation correcte des variables en dehors de la porte
   * Envoyer un courrier électronique d’annonce de lancement récapitulatif aux principaux intervenants et analystes
   * Créez une bibliothèque qui peut être utilisée pour les heures de bureau, les sessions d’activation de l’équipe ou pour l’intégration spécifique à l’équipe.

1. Documentation sur la collecte de données, gouvernance et hygiène des données - TDAH :

   Le tableau de bord de l’intégrité d’Analytics (AHD) plonge profondément dans une _single_ suite de rapports et fournit une vue des données collectées dans chaque composant (eVar, prop et événement). Cela peut vous aider à savoir si les données ont cessé de collecter des données dans un composant afin que vous puissiez prendre des mesures pour corriger le problème. Vous pouvez exécuter ce tableau de bord à tout moment à l’avenir pour n’importe quelle suite de rapports.

   Tableau de bord de l’intégrité d’Analytics (AHD) :

   _Cas pratique :_ Instantané de chaque mesure et dimension capturée par une seule suite de rapports

   _Utilisateurs Principal :_ Responsive Analytics PME et/ou Dev

   _Autres notes:_
   * Diffusée par le biais d’Excel à l’aide d’une intégration personnalisée de l’API de création de rapports sur les Adobes
   * Les utilisateurs doivent disposer d’un accès à l’API des services Web Analytics
   * Des options de semi-automatisation existent

1. Gagner en élargissant le monde des experts en la matière (PME) :

   * Créer des PME au sein des différentes équipes de l’organisation
   * Créer leur présence en contribuant à la socialisation des versions et des victoires
   * Utiliser les heures de bureau régulières pour former les formateurs et réduire les tâches ad hoc

Pour en savoir plus sur la stratégie et le leadership de la pensée, voir [Succès des clients](https://experienceleague.corp.adobe.com/docs/customer-success/customer-success/overview.html) hub.