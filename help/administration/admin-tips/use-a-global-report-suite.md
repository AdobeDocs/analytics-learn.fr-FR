---
title: Utilisation d’une suite de rapports globale
description: Disposer d’une seule suite de rapports globale peut vous aider de plusieurs façons et vraiment simplifier votre mise en oeuvre.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10536.jpg
kt: 10536
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---


# Utilisation d’une suite de rapports globale

**QUOI :** Il est tentant de créer des suites de rapports pour chacun de vos sites, mais cela peut rapidement devenir votre pire cauchemar, tant en termes de compliquer vos rapports que votre mise en oeuvre. Disposer d’une seule suite de rapports globale peut vous aider de plusieurs façons et vraiment simplifier votre mise en oeuvre.

**POURQUOI :** La création d’une suite de rapports globale est votre seule option pour obtenir une vue unifiée de vos propriétés numériques et des parcours des utilisateurs sur chaque propriété. Si vous disposez d’une application mobile et d’un site web, vous devez toujours combiner les données de l’application et les données web dans une suite de rapports afin de tirer parti des parcours entre appareils et de suivre les visiteurs qui visitent les deux propriétés comme un seul visiteur et avec des suites de rapports distinctes, dans lesquelles un jeu de données disjoint présentant 2 visiteurs (1 sur chaque propriété) est impossible de connaître le croisement.

Voici les avantages/inconvénients d’une seule suite de rapports pour vous aider à évaluer vos options :

* PROS :
   * Être capable de comprendre facilement l&#39;ensemble de votre paysage numérique. Si vous avez implémenté la dimension &quot;propriétés&quot; (eVar) référencée dans d’autres conseils, vous pourrez facilement obtenir une vue unique de tous vos sites et applications, trafic et conversions. Avoir cette vue d&#39;ensemble est essentiel pour comprendre votre entreprise dans son ensemble.
   * Dans le même sens, vous pouvez maintenant voir comment les utilisateurs se déplacent dans toutes vos propriétés et comprendre leur parcours dans votre paysage numérique.
   * Facilité d&#39;administration. Lors de l’utilisation de plusieurs suites de rapports, vous devrez conserver l’interface à plusieurs endroits, ainsi que plusieurs documents de balisage (ou un document plus complexe). Garder tout en un seul endroit signifie qu&#39;il n&#39;y a qu&#39;un seul endroit pour faire des mises à jour. Cela facilite également l&#39;accès.
   * Amélioration de la convivialité de l’interface. Si vos utilisateurs n’ont qu’un seul emplacement, ils n’ont pas besoin de réfléchir à la suite de rapports à sélectionner. Gardez à l’esprit que vous ne pouvez pas utiliser plusieurs suites de rapports dans le même panneau de l’espace de travail. Plusieurs d’entre elles peuvent dérouter vos utilisateurs.
   * Moins d’appels au serveur = moins de coûts. Si vous effectuez des appels vers plusieurs suites de rapports, vous augmentez les coûts. Le simple fait de conserver votre mise en oeuvre permet également de réduire vos coûts.
   * Vous pouvez simplement tirer parti des suites de rapports virtuelles pour ventiler les données spécifiques au site dans la suite de rapports globale et limiter les autorisations d’utilisateur en fonction d’une suite de rapports virtuelle, si nécessaire. Une fois que les données sont séparées dans des suites de rapports individuelles, vous ne pouvez pas les cumuler, mais si elles sont déjà jointes à un jeu de données (RS global), elles sont facilement ventilées.
* CONS :
   * Si vous disposez de propriétés très distinctes dans lesquelles les utilisateurs ne passent pas d’un à l’autre et ne sont jamais censés le faire, vous pouvez conserver des suites de rapports distinctes.
   * Si vos propriétés ont des besoins de balisage et de création de rapports très différents, il peut être logique de configurer des suites de rapports distinctes dans un souci d’efficacité variable. Disposer de suites de rapports distinctes vous offre davantage de flexibilité pour l’utilisation de variables personnalisées (davantage d’eVars).
   * Valeurs uniques dépassées : L’interface d’Adobe Analytics vous permet uniquement d’afficher 500 000 valeurs uniques au sein d’une seule dimension pour une période donnée. Une fois cette limite dépassée, les valeurs seront regroupées sous la forme de &quot;Valeurs uniques dépassées&quot; ou &quot;Faible trafic&quot; dans l’interface. Ces valeurs restent disponibles pour vous sur le serveur principal (c’est-à-dire Data Warehouse, flux de données), mais ne peuvent pas être visualisées dans l’interface. Si vous disposez de données très granulaires (comme l&#39;identifiant utilisateur, le standard de vie, etc.), il est facile d&#39;atteindre ce niveau. Disposer de suites de rapports distinctes peut aider à résoudre ce problème.

**COMMENT :** Il est simple et simple de commencer par une nouvelle mise en oeuvre AA et d’utiliser une seule suite de rapports globale. Vous devez simplement créer la suite de rapports globale (une pour le développement et une pour la production) dans l’interface utilisateur d’administration d’AA et appliquer les mêmes valeurs d’identifiant de suite de rapports (RSID) sur toutes vos propriétés.

La migration à partir d’une stratégie à balisage multiple avec une suite de rapports unique par propriété nécessite davantage de stratégie et de planification. Voici quelques points à prendre en compte :

* L’alignement de vos variables (c’est-à-dire eVar1 sur Propriété A doit capturer le même point de données que eVar1 sur Propriété B)
* Consolidation de toutes les règles de traitement, règles de canal marketing, classifications (SAINT et Créateur de règles)
* Migration de flux de données et de sources de données
* Choix d’une date de coupure et communication de cette dernière à tous les utilisateurs professionnels

## Auteurs

Ce document a été co-écrit par :

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, responsable de la plateforme Digital Analytics chez NortonLifeLock Champion Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, conseillère principale chez Adobe
