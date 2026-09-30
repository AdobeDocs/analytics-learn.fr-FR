---
title: Présentation d’Analytics
description: Comprendre les principes de base de l’analyse avant d’apprendre à utiliser Adobe Analytics
feature: Implementation Basics
role: Developer, Developer, Leader, User
level: Beginner
kt: 10454
thumbnail:
last-substantial-update: 2022-10-14T00:00:00.000Z
exl-id: ba2959f0-b667-40f9-bc59-9364a9d83f19
TQID: 'https://experienceleague.adobe.com/6aNeRhdbEMFR0A9301GsuTWxWe3w-OUCeFhTOOaWUfg'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
    internal-label: Analysis Workspace
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: c67272a6-888e-425e-9e97-a87304637eed
    internal-label: Anomaly Detection
  - id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705c
    internal-label: Marketing Channels
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
    internal-label: Events
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
source-git-commit: 3e00cf9416ba2c6886e5a7efb952cac8ce370930
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 100%
---
# Qu’est-ce que l’analyse ?{#what-is-analytics}

Avant de vous plonger dans le contenu d’Adobe Analytics, il est utile de comprendre la réponse à cette question fondamentale « Qu’est-ce que l’analytics ? » L’analytics est un terme général qui englobe plusieurs disciplines visant à stimuler le développement et la transformation de l’entreprise, en particulier l’analytics métier et la data analytics. Il existe une différence entre les deux. Regardons de plus près.

## Le rôle de l’analytics métier

Ces dernières années, la naissance et la maturité de l’utilisation d’Internet à des fins commerciales ont explosé, tout comme la quantité de données amassées par les organisations sur la façon dont les consommateurs interagissent et adhèrent à leur marque. Si vous avez déjà entendu le terme Big Data, celui-ci relève du domaine de l’analytics métier.

L’analytics métier est une composante de la business intelligence et se concentre sur les risques et les opportunités stratégiques à grande échelle. Il s’agit d’une compétence nécessaire que les entreprises doivent posséder pour rester compétitives dans leur secteur.

Il existe quatre types d’analytics métier :

* **Descriptive** : elle implique l’utilisation de données historiques pour identifier les tendances dans l’activité d’une entreprise. Par exemple, un distributeur doit prévoir la demande de produits avant les périodes de haute activité ou de vacances et disposer d’un stock suffisant pour atteindre ses objectifs commerciaux.
* **Diagnostic** : quelles sont les raisons d’un résultat inattendu ? Pourquoi y a-t-il eu une forte demande pour un produit ou un service pendant la saison creuse ? L’analyse diagnostique est une forme plus approfondie d’analyse descriptive et vise à dégager des corrélations à partir des données.
* **Prédictive** : cette méthode utilise des données historiques pour déterminer des résultats ou des événements probables. Le machine learning (ML) et l’intelligence artificielle (IA) sont généralement utilisés pour des pronostics plus précis. L’attrition client est un exemple d’application réelle de l’analyse prédictive. Cette analyse permet de trouver des corrélations afin d’identifier les attributs des clients et clientes susceptibles de faire l’objet d’attrition, afin que vous puissiez agir pour l’éviter.
* **Prescriptive** : il s’agit d’une forme avancée d’analyse prédictive qui vise à découvrir le meilleur moyen d’atteindre un résultat souhaité. Ce type d’analyse utilise également les technologies de machine learning et d’IA. Les détaillants utilisent l’analyse prescriptive pour augmenter leurs marges en apportant des changements à leurs activités.

![types d’analyse des données](../what-can-aa-do-for-me/assets/data_analytics_types.png)

## Le rôle de la data analytics

La data analytics utilise de nombreuses technologies identiques à celles utilisées pour l’analytics métier, mais sa portée est plus large et sa nature plus technique. L’analyse des Big Data, par exemple, repose sur la qualité et l’organisation des données. Avec quelle efficacité les données sont-elles traitées, stockées et nettoyées ? Les spécialistes des données travaillent dans le domaine de la data analytics. Ils transforment des ensembles de données volumineux que les analystes métier utilisent ensuite pour communiquer des informations à l’organisation afin d’optimiser les processus et les mesures. Les spécialistes des données étudient plus en détail les données, pour déterminer les tendances et les connexions.

![analyse des données](../what-can-aa-do-for-me/assets/data_analytics.png)

## Quel est le rôle d’Adobe Analytics ?

Adobe Analytics est une plateforme d’analyse de données performante qui collecte des données à partir d’expériences digitales multicanaux prenant en charge le parcours client et fournit des outils pour analyser ces données. Il s’agit d’une plateforme généralement utilisée par les spécialistes du marketing et les analystes métier à des fins d’analycs métier.

Les exigences métier, la conception et la collecte des données sont des facteurs clés pour une pratique d’analytics efficace. Dans un premier temps, les clients commencent par collecter des données sur les parcours client clés et les résultats commerciaux escomptés pour les expériences digitales traditionnelles, comme le Web et les appareils mobiles. Les données doivent permettre de répondre à des questions telles que :

* « Quels sont le contenu et les types de contenu les plus appréciés par les visiteurs et visiteuses ? »
* « Quels sont les chemins qui génèrent des conversions à forte valeur ajoutée, comme les revenus, les réservations, les demandes ou les abonnements ? »
* « Quels produits, services ou contenu dois-je présenter aux utilisateurs et utilisatrices habituels et nouveaux ? »
* « Quelles sont les performances des canaux de marketing digital ? »

![exigences en matière d’analyse commerciales](../what-can-aa-do-for-me/assets/analytics_business_requirements.png)

Une fois la base de données collectée dans Adobe Analytics, les spécialistes du marketing et les analystes métier utilisent divers rapports et outils de visualisation de données disponibles dans le produit pour effectuer une analyse et présenter des informations significatives sur ces données. Qui plus est, Adobe Analytics fournit des résultats sous diverses formes. Il peut s’agir d’un segment ou d’une audience envoyé à un outil d’optimisation, comme Adobe Target, pour exécuter des tests A/B. Il peut s’agir d’un score prédictif indiquant la probabilité d’une action d’une personne, qui est ensuite utilisé par un autre système pour la modélisation.

![analytics-workspace-project](../what-can-aa-do-for-me/assets/analytics_workspace_project.png)

Au fil du temps, les clients et clientes enrichissent les données web et mobiles traditionnelles avec d’autres canaux, notamment la gestion de la relation client (CRM), les centres d’appel, les magasins physiques, les assistants vocaux, etc. Adobe Analytics offre plusieurs méthodes pour capturer des données à partir de pratiquement n’importe quelle source de canal et ainsi créer une base de données d’analyse fiable.

La collecte de jeux de données supplémentaires permet d’effectuer des analyses de données prescriptives plus avancées, grâce au machine learning ou à des modèles de données avancés, tels que l’attribution marketing et la détection des anomalies.

Nous vous encourageons à consulter les tutoriels sur Experience League pour vous guider à travers les principaux avantages et fonctionnalités d’Adobe Analytics.
