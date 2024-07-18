---
title: Utiliser une suite de rapports globale
description: Disposer d’une seule suite de rapports globale peut vous aider de diverses manières et véritablement simplifier votre implémentation.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10536.jpg
kt: 10536
exl-id: 490addfd-b810-4f15-b065-e0e58048c882
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 100%

---

# Utiliser une suite de rapports globale

**QUOI :** bien qu’il soit tentant de créer des suites de rapports pour chacun de vos sites, cela peut rapidement entraîner de nombreuses complications, tant au niveau du compte rendu des performances que de votre implémentation. Disposer d’une seule suite de rapports globale peut vous aider de diverses manières et véritablement simplifier votre implémentation.

**POURQUOI :** la création d’une suite de rapports globale est la seule option qui vous permet d’obtenir une vue unifiée de vos propriétés numériques et des parcours des utilisateurs sur chaque propriété. Si vous disposez d’une application mobile et d’un site web, vous devez toujours combiner les données de l’application et les données web dans une seule suite de rapports afin de tirer parti des parcours entre appareils. Vous pouvez ainsi suivre les utilisateurs qui visitent les deux propriétés comme un seul visiteur. Avec des suites de rapports distinctes, vous obtiendriez un jeu de données incohérent, présentant 2 visiteurs (1 pour chaque propriété) sans possibilité de connaître le croisement.

Voici les avantages/inconvénients liés à une suite de rapports unique pour vous aider à évaluer vos options :

* AVANTAGES :
   * Être capable de comprendre facilement l’ensemble de votre paysage numérique. Si vous avez implémenté la dimension « propriétés » (eVar) évoquée dans d’autres conseils, vous pouvez facilement obtenir une vue unique de tous vos sites et applications, ainsi que du trafic et des conversions liés. Cette vue d’ensemble est essentielle à la compréhension de votre activité dans sa totalité.
   * Dans la même idée, vous pouvez désormais voir comment les utilisateurs se déplacent dans toutes vos propriétés et comprendre leur parcours dans votre paysage numérique.
   * Facilité d’administration. L’utilisation de plusieurs suites de rapports nécessite de conserver l’interface dans plusieurs emplacements. Cela requiert également plusieurs documents de balisage (ou un document plus complexe). Conserver tous les éléments au sein d’un seul emplacement permet de n’effectuer les mises à jour qu’en ce même emplacement. Cela facilite également l’accès.
   * Amélioration de la convivialité de l’interface. En n’ayant qu’un seul emplacement vers lequel se diriger, vos utilisateurs n’ont pas besoin de réfléchir à la suite de rapports à sélectionner. Gardez à l’esprit que vous ne pouvez pas utiliser plusieurs suites de rapports dans le même panneau d’espace de travail. En outre, la présence de multiples suites peut dérouter vos utilisateurs.
   * Moins d’appels au serveur = moins de coûts. Si vous effectuez des appels vers plusieurs suites de rapports, vous augmentez les coûts. Maintenir une implémentation simple permet également de réduire vos coûts.
   * Vous pouvez simplement tirer parti des suites de rapports virtuelles pour ventiler les données spécifiques au site dans la suite de rapports globale et limiter les autorisations d’utilisateur en fonction d’une suite de rapports virtuelle, si nécessaire. Une fois les données séparées dans des suites de rapports individuelles, vous ne pouvez pas les cumuler. Toutefois, elles sont facilement ventilées si elles sont déjà reliées dans un jeu de données (suite de rapports globale).
* INCONVÉNIENTS :
   * Si vous disposez de propriétés très distinctes, où aucun transfert d’utilisateurs n’a lieu et où cela n’est jamais censé se produire, vous pouvez conserver des suites de rapports distinctes.
   * Si vos propriétés ont des besoins de balisage et de compte rendu des performances très différents, il peut être logique de configurer des suites de rapports distinctes dans un souci d’efficacité des variables. Disposer de suites de rapports distinctes vous offre davantage de flexibilité pour l’utilisation de variables personnalisées (davantage d’eVars).
   * Valeurs uniques dépassées : l’interface d’Adobe Analytics vous permet uniquement d’afficher 500 000 valeurs uniques au sein d’une seule dimension pour une période donnée. Une fois cette limite dépassée, les valeurs sont regroupées en tant que « Valeurs uniques dépassées » ou « Faible trafic » dans l’interface. Ces valeurs restent à votre disposition sur le serveur principal (c’est-à-dire Data Warehouse, flux de données), mais ne peuvent pas être visualisées dans l’interface. Si vous disposez de données très granulaires (par exemple ID d’utilisateur, PSN, etc.), il est facile d’atteindre ce niveau. Disposer de suites de rapports distinctes peut aider à résoudre ce problème.

**COMMENT :** démarrer avec une nouvelle implémentation d’AA et utiliser une seule suite de rapports globale est très simple. Il vous suffit de créer la suite de rapports globale (une pour le développement et une pour la production) dans l’interface utilisateur d’administration d’AA, et d’appliquer les mêmes valeurs d’identifiant de suite de rapports (RSID) sur toutes vos propriétés.

Effectuer une migration à partir d’une stratégie à balisage multiple avec une suite de rapports unique par propriété nécessite davantage de stratégie et de planification. Voici quelques points à prendre en compte :

* L’alignement de vos variables (c’est-à-dire, eVar1 sur Propriété A doit capturer le même point de données qu’eVar1 sur Propriété B).
* La consolidation de toutes les règles de traitement, règles de canal marketing, classifications (SAINT et Créateur de règles).
* La migration des flux de données et des sources de données.
* Le choix d’une date de transfert et la communication de cette dernière à tous les utilisateurs professionnels.

## Auteurs

Ce document a été rédigé par :

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, responsable de la plateforme Digital Analytics chez NortonLifeLock
Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, conseillère principale chez Adobe
