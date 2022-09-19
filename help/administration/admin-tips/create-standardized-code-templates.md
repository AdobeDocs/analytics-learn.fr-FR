---
title: Créer des modèles de code normalisés
description: Pour une implémentation de base (c’est-à-dire ce que votre entreprise considère comme des indicateurs de performance clés obligatoires pour tous les sites Adobe Analytics), votre organisation doit disposer d’une méthode d’implémentation unique, dans la mesure du possible.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
exl-id: be00c8c0-a4bc-4380-98da-d1e2a3d31ec5
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 100%

---

# Créer des modèles de code normalisés

**QUOI :** pour une implémentation « de base » (c’est-à-dire ce que votre entreprise considère comme des indicateurs de performance clés obligatoires pour tous les sites Adobe Analytics), votre organisation doit disposer d’une méthode d’implémentation unique, dans la mesure du possible. Par exemple, utilisez la même structure de couche de données sur plusieurs sites et utilisez le même code personnalisé/règle de gestionnaire de balises pour capturer des éléments tels que des recherches internes ou des informations de profil du visiteur.

**POURQUOI :** une implémentation de base répétable et évolutive permet d’ajouter de nouveaux éléments ou de nouveaux sites/applications dans un effort réduit et rationalisé, tout en préservant votre implémentation et en facilitant la résolution des problèmes. L’utilisation d’une méthode uniforme permet également aux nouveaux administrateurs/développeurs de se connecter et de comprendre ce avec quoi ils travaillent.

**COMMENT :** adoptez un modèle de format unique à transmettre aux développeurs lorsqu’un nouveau site ou une amélioration du balisage est en ligne. En règle générale, un document Word fonctionne bien quand vous pouvez mettre en avant les éléments suivants :

* Variables en cours d’implémentation, leur objectif et quand les définir. Par exemple :

| Variable AA | Description | Quand/où définir | Comment définir |
|--- |--- |--- |--- |
| eVar8 | Mots-clés de recherche interne | En arrivant sur la page de résultats de recherche interne | Couche de données |
| event8 | Nombre de recherches internes | En arrivant sur la page de résultats de recherche interne | Règle Launch |

* Précisions sur la définition. C’est là que vous spécifiez les objets de couche de données nécessaires, leur syntaxe ainsi que les règles TMS à configurer et les détails de la configuration des règles.
* Les cas de test pour vous tout vérifier sont couverts dans l’assurance qualité et toutes les variables que vous vous attendez à voir dans un cas de test réussi. Décrivez ce qu’une implémentation réussie doit inclure lorsque le développeur teste cette amélioration.

Idéalement, il suffira de modifier ce document pour le site suivant où vous mettez à jour les éléments de base tels que le nom de la propriété, la convention de nommage des pages, etc. Pas besoin de réinventer la roue à chaque fois, et vous pouvez gagner du temps.

## Auteurs

Ce document a été rédigé par :

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, responsable de la plateforme Digital Analytics chez NortonLifeLock
Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, conseillère principale chez Adobe
