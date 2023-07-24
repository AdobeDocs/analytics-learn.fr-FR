---
title: Astuces simples pour une plus grande efficacité et un meilleur libre-service - Partie 1
description: Découvrez les principaux défis auxquels sont confrontées les équipes d’analyse et nos recommandations pour les surmonter à l’aide de stratégies en dehors de l’interface utilisateur d’Adobe Analytics.
feature: Analytics Basics
role: Admin, Leader
level: Intermediate
solution: Analytics
exl-id: 5d1077fd-d006-4a85-bf1c-54f6b2d31934
source-git-commit: d7fd77640928697f5857ccfcaf2c0f561aebeac3
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 100%

---

# Adobe Analytics : astuces simples pour une plus grande efficacité et un meilleur libre-service

**Partie 1 : en dehors de l’interface utilisateur**

Cet article décrit les principaux défis auxquels sont confrontées les équipes Analytics aujourd’hui et nos recommandations pour les surmonter à l’aide de stratégies en dehors de l’interface d’Adobe Analytics.

## Principaux défis pour les équipes Analytics

De nombreuses équipes Analytics se retrouvent avec une répartition déséquilibrée du travail. Au lieu d’un mélange de 80 % d’analyses et 20 % d’implémentation, beaucoup d’organisations se retrouvent dans la situation inverse. Elles voient que la plupart de leurs efforts sont consacrés à la configuration, à la création de rapports et à l’assistance plutôt qu’à la production d’analyses générant des informations de grande valeur.

Pour différentes raisons, la productivité et l’efficacité des équipes Analytics diminuent drastiquement. Cela est notamment dû aux implémentations en constante évolution, à la volonté de maintenir la confiance de l’organisation dans les données et à la réduction de la rotation des analystes. La réduction de la rotation du personnel permet d’éviter le long processus de formation des nouveaux membres de l’équipe à l’utilisation d’outils d’implémentation personnalisés et inconnus.

Les autres défis majeurs auxquels sont confrontés les analystes :

* **La concurrence :** les commerces de détail en ligne et multicanaux deviennent plus compétitifs.
* **Les attentes du client :** les expériences client et les stratégies marketing deviennent plus complexes.
* **La valeur des données :** la valeur de données et d’informations précises pour générer un avantage concurrentiel augmente.
* **Les attentes des parties prenantes :** les partenaires commerciaux, les parties prenantes et les cadres supérieurs demandent de plus en plus de données avant de donner leur approbation.
* **La gestion de projets :** l’équipe Analytics croule sous les demandes d’implémentation de la collecte de données pour un flux sans fin de nouvelles fonctionnalités, tout en produisant des rapports précis, en accueillant de nouveaux analystes et en découvrant de nouvelles informations.

## Les clés de l’efficacité : en dehors de l’interface utilisateur

1. Maintenez votre [Référence de conception de solution](/help/implementation/implementation-basics/creating-and-maintaining-an-sdr.md) (SDR) à jour :

   * La SDR est la principale source de vérité pour la définition et l’utilisation prévue de toutes les variables dans votre implémentation d’analyses.
   * La SDR est la référence principale que les utilisateurs doivent connaître pour tirer parti de l’interface utilisateur d’Adobe Analytics.
   * Il est important de la conserver à jour et avec la bonne version (un simple format de date peut être utilisé).

1. Documentation et gouvernance de la collecte de données - Spécifications techniques :

   Les spécifications techniques ont une audience plus limitée que la SDR, mais elle sont aussi importantes, sinon plus, pour une implémentation entièrement fonctionnelle. De bonnes spécifications techniques doivent comprendre les ressources de développement, d’assurance qualité et de gestion des balises nécessaires à l’implémentation de la solution. Veillez à conserver autant de documents que nécessaire pour accueillir des architectures d’implémentation uniques.

   **Spécifications techniques**

   _Cas d’utilisation :_ instructions décrivant comment créer des scripts pour la collecte de données.

   _Utilisateurs principaux :_ développeurs.

   _Autres notes :_

   * Document hautement technique conçu spécifiquement pour vos environnements de déploiement.
   * Utile à la fois pour l’implémenation initiale et la maintenance/référence ultérieure.
   * Organisé par type de solution (par exemple suivi de campagne, métadonnées de page, etc.).
   * Le document principal doit être mis à jour et conservé au fur et à mesure que les modifications de la SDR sont apportées.
   * Référentiel central
   * Numéros de version synchronisés pour la SDR et les spécifications techniques.

1. Communiquer et documenter l’intention de conception de la solution au lancement :

   * Communiquer en pensant à l’utilisateur
   * Lorsque vous lancez ou améliorez la collecte de données, créez des résumés simples qui peuvent être partagés avec les parties prenantes.
   * Renforcer rapidement l’utilisation adaptée des variables
   * Envoyer un e-mail d’annonce de lancement récapitulatif aux principaux intervenants et analystes
   * Créez une bibliothèque qui peut être utilisée pour les heures de bureau, les sessions d’activation de l’équipe ou pour une intégration spécifique à l’équipe.

1. Documentation sur la collecte de données, la gouvernance et l’hygiène des données - AHD :

   Le tableau de bord Analytics Health Dashboard (AHD) étudie en détails une _unique_ suite de rapports et fournit une vue des données collectées dans chaque composant (eVar, prop et événement). Cela peut vous aider à savoir si les données ont cessé de collecter des données dans un composant afin que vous puissiez prendre des mesures pour corriger le problème. À l’avenir, vous pourrez exécuter ce tableau de bord à tout moment et pour n’importe quelle suite de rapports.

   Tableau de bord Analytics Health Dashboard (AHD) :

   _Cas d’utilisation :_ instantané de chaque mesure et dimension capturée par une seule suite de rapports.

   _Utilisateurs principaux :_ responsable SME analyses et/ou Dev.

   _Autres remarques :_
   * Diffusé par le biais d’Excel à l’aide d’une intégration personnalisée de l’API de création de rapports Adobe.
   * Les utilisateurs doivent disposer d’un accès à l’API de services web Analytics.
   * Des options de semi-automatisation existent.

1. Gagner en élargissant le monde des experts en la matière (SME) :

   * Mettre en place des experts en la matière (SME) au sein des différentes équipes de l’organisation
   * Établir leur présence en contribuant à la socialisation des versions et des succès
   * Utiliser les heures de bureau standard pour former les formateurs et réduire les tâches ad hoc

Pour en savoir plus sur la stratégie et le leadership, voir le hub [Succès client](https://experienceleague.adobe.com/docs/customer-success/customer-success/overview.html?lang=fr).