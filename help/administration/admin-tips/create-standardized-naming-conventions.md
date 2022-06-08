---
title: Créer des conventions d’affectation de noms normalisées
description: Les conventions d’appellation normalisées s’appliquent à la fois au nom de variable lui-même lorsqu’il est activé dans l’interface utilisateur d’administration d’AA et aux valeurs transmises à la dimension.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10531.jpg
kt: 10531
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---


# Créer des conventions d’affectation de noms normalisées

**QUOI :** Les conventions d’appellation normalisées s’appliquent à la fois au nom de variable lui-même lorsqu’il est activé dans l’interface utilisateur d’administration d’Adobe Analytics (AA) et aux valeurs transmises à la dimension. (c’est-à-dire que les noms de page seraient &quot;nom de page (v1)&quot; comme nom de variable et que les valeurs de nom de page transmises doivent être uniformes et suivre une structure/hiérarchie spécifique telle que &quot;nom_site|page&quot; ou &quot;nom_site|recherche|résultats_recherche&quot;).

**POURQUOI :** Les conventions d’attribution de noms sont un excellent moyen de maintenir tout l’uniforme et de faciliter la compréhension de l’interface pour vos utilisateurs. Si vous les créez à partir du début et que vous les appliquez dans la plateforme et le code, elles seront plus faciles à mettre à l’échelle.

**COMMENT :** L’interface et le document de balisage doivent correspondre à la fois à &quot;Nom&quot; et à &quot;Description&quot;. Ainsi, vos utilisateurs n’auront plus à extraire un document Excel et pourront comprendre directement vos données dans l’interface. Il est également recommandé de maintenir la casse de tous les éléments pour garantir la cohérence.

Il est toujours préférable de préserver la cohérence des noms de page sur l’ensemble de la plateforme (ou des noms d’écran pour les applications). Par exemple, vous pouvez définir &quot;property&quot;:section:sous-section:sous-section:nom de page unique&quot; dans une variable/dimension. Si tous ces champs sont distincts dans votre couche de données, vous pouvez même créer le nom de page directement dans votre fichier JS/Launch. Si tous ces éléments sont définis dans leurs propres dimensions, vous pouvez ventiler plus facilement des propriétés ou des zones spécifiques de votre site/application et mieux comprendre le trafic et les flux.

Tout ce qui permet aux utilisateurs de trouver et de comprendre plus facilement les données, y compris des informations aussi simples que des conventions de dénomination, accroît l’utilisation d’Adobe Analytics et fournit de meilleures informations pour l’entreprise.

## Auteurs

Ce document a été co-écrit par :

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, responsable de la plateforme Digital Analytics chez NortonLifeLock Champion Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, conseillère principale chez Adobe
