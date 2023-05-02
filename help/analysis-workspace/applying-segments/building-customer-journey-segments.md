---
title: Création de segments de Parcours client
description: Découvrez comment créer des segments de parcours client basés sur le comportement dans Adobe Analytics et améliorer l’expérience de vos clients avec Adobe Experience Cloud en suivant ce guide détaillé.
feature: Segmentation
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13180
thumbnail: KT-13180.jpeg
source-git-commit: d7b1fac5c98080f9ca786ea21a3700d2937c7ebc
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---


# Création de segments de Parcours client

Découvrez comment créer des segments de parcours client basés sur le comportement dans Adobe Analytics et améliorer l’expérience de vos clients avec Adobe Experience Cloud en suivant ce guide détaillé.

Créons de meilleurs segments de parcours client ! Dans cette série, nous utiliserons Adobe Analytics pour définir des segments basés sur le comportement, estimer la taille des audiences et suivre les mouvements des utilisateurs. D’ici la fin, vous pourrez personnaliser les médias et améliorer l’expérience de vos clients avec Adobe Experience Cloud. Gardez à l’esprit que ces segments sont actifs et doivent être mis à jour au fur et à mesure que vous en apprendrez plus sur vos clients. Bien que le reporting puisse présenter quelques défis, ne vous inquiétez pas, je vous guiderai à travers ! Commençons par créer notre premier ensemble de segments de Parcours client, en commençant par le segment &quot;One Hit Wonders&quot;.

Aujourd’hui, nous allons créer des espaces réservés pour notre premier ensemble de segments de Parcours client, créer un espace de travail Adobe Analytics pour nous aider à définir nos segments, et définir notre tout premier segment, &quot;One Hit Wonders&quot;.

D’ici la fin de cette série, vous pourrez créer des segments de parcours client dans Adobe Analytics en fonction des signaux comportementaux. Vous pourrez estimer la taille de chaque audience à chaque étape du parcours et comprendre le taux de déplacement des utilisateurs entre ces étapes. Et vous pourrez exporter ces audiences de parcours client vers Adobe Experience Cloud pour activer la personnalisation et le ciblage multimédia.

Chaque entreprise est différente, ce qui signifie que vos segments de parcours client auront un aspect différent du mien. Donc, plutôt que de prescrire des formules spécifiques pour vos segments, suggérez quelques éléments à examiner et un processus global pour les construire.

Il est également important de noter que vos segments de parcours client seront des segments actifs. Ce n&#39;est pas un exercice unilatéral. À mesure que vous en apprendrez plus sur vos clients, vous allez mettre à jour ces segments. Cela présente certains défis pour les rapports. Les utilisateurs souhaitent la cohérence de leurs rapports, et si nos définitions de segment changent, les nombres dans les rapports changent également.

## Prise en main des segments d’intention de visite

La première étape de la création de segments de parcours client consiste à déduire pourquoi un invité se trouve sur votre site web à l’aide de signaux de comportement et, si possible, de données de voix du client. Nous allons créer un ensemble de segments d’intention de visite afin de classer toutes les visites sur le site web. À ce stade, nos segments d’intention de visite doivent s’exclure mutuellement et être complètement exhaustifs. Chaque visite doit appartenir à un seul segment, Intention de visite.

Les segments Intention de visite décrivent une visite. Nous utiliserons donc le conteneur Visites dans la définition de segment.

Mon jeu initial de segments d’intention de visite était le suivant :

* Un accès se demande
* Sensibilité
* Considération
* Réservation (Achat)
* Rétention (gérer une réservation/un achat)

Pour faciliter l’utilisation de mes segments d’intention de visite, j’ai ajouté le préfixe &quot;Intention :&quot; dans les noms de mes segments, leur ai donné un numéro pour activer le tri et leur ai balisé &quot;intention&quot;. Mes segments ressemblaient à l&#39;image ci-dessous.

![segments d’intention](assets/intent-segments.png)

**Continuez et créez vos segments d’intention de visite à l’aide du conteneur Visites avec une définition d’espace réservé de Pages vues >= 1.**

Comme nous le verrons, la création de ces segments est un processus itératif et interconnecté. Je décrirai le processus de création de ces segments dans une prochaine publication.

## Espace de travail de qualité des données de segment d’intention de visite

![espace de travail des intentions de visite](assets/visit-intent-workspace.png)

J’ai utilisé un simple espace de travail pour m’assurer que je définissais bien mes segments d’intention de visite. Souvenez-vous que chaque visite doit appartenir à un seul segment, Intention de visite. L’espace de travail que je configure garantit que toutes les visites sont prises en compte et qu’il n’y a pas de chevauchement entre les segments.

J’ai appelé cet espace de travail &quot;QUALITÉ DES DONNÉES : Segments d’intention de visite&quot; avec les balises &quot;qualité des données&quot;, &quot;intention de visite&quot; et &quot;parcours client&quot;. Par la suite, nous allons créer un &quot;Tableau de bord de l’intention de visite&quot; de sorte que le préfixe &quot;QUALITÉ DES DONNÉES&quot; indique que cet espace de travail est destiné à configurer et à gérer les segments. Il s’agit d’un tableau de bord administratif qui n’a que peu d’informations sur l’entreprise, mais qui est important pour s’assurer que les segments sont conservés. Revenez régulièrement à ce tableau de bord ou configurez des alertes pour vous assurer que vos segments restent correctement définis.

La visualisation la plus importante de cet espace de travail est la visualisation à structure libre de chevauchement de segments au milieu à gauche. À l’aide de la mesure Visites , créez des filtres de colonnes pour chaque segment d’intention de visite, plus le segment Toutes les visites dans la colonne la plus à droite. Créez des lignes pour chaque segment d’intention de visite à gauche. Vous disposez désormais d’une visualisation sur plusieurs onglets. Lorsque vos segments sont correctement configurés, il n’y a que des données dans une colonne et une ligne, à l’intersection de chaque segment d’intention de visite avec lui-même.

Les visualisations les plus importantes suivantes sont les mesures de résumé en haut à gauche. Le résumé des visites segmentées reprend sa valeur de la colonne Toutes les visites dans la visualisation de chevauchement de segments immédiatement ci-dessous. Le résumé Toutes les visites comporte son propre tableau masqué.

![toutes les visites](assets/all-visits.png)

En haut à droite, j’ai ajouté des mesures supplémentaires à chacun des segments pour donner un aperçu de la manière dont les segments sont en train de se former. En particulier, étant donné que ces segments s’excluent mutuellement, je m’attends uniquement à voir les réservations pour le segment d’intention de réservation (par crainte de ne pas le faire, nous atteindrons les taux de conversion lorsque nous créerons ces segments d’intention de visite en fonction des visiteurs.

Souvenez-vous que nous venons de créer des segments d’espace réservé. Au départ, votre espace de travail aura l&#39;air surprenant. Tous vos segments d’intention de visite chevaucheront 100 %, car ils ont la même définition. C&#39;est correct, et exactement ce que vous souhaitez voir à ce stade du processus. Au fur et à mesure que nous créons les définitions de segment, ces segments commencent à prendre forme.

![Définitions de segment d’intention de visite](assets/visit-intent-segment-defs.png)

## Création de votre premier segment d’intention de visite

La définition des segments d’intention de visite est un processus d’élimination, et il y a beaucoup d’interdépendance entre eux. Je n&#39;ai donc pas créé ces segments dans l&#39;ordre du parcours, je les ai créés dans l&#39;ordre du plus facile à définir au plus difficile. Cela m&#39;a donné cet ordre :

1. Intention : 0 - Un accès se demande
1. Intention : 3 - Réservation
1. Intention : 4 - Rétention
1. Intention : 2 - Considération
1. Intention : 1 - Sensibilisation

Plutôt aléatoire, hein ? La définition de ces segments d’intention de visite était un processus itératif, aller-retour, et souvent un ajustement à un segment nécessitait des mises à jour à d’autres segments. Cela deviendra plus clair lorsque je décrirai la manière dont j’ai défini chacun de ces segments.

Aujourd’hui, nous définirons notre premier segment, le plus simple, qui se demande un accès

## Création du segment One Hit Wonders

Mon premier segment, &quot;One Hit Wonders&quot;, était facile à définir. Il s’agit simplement de toute visite avec une seule page vue. Nous ne savons vraiment pas pourquoi cet utilisateur était sur le site, parce qu&#39;il a rebondi. Je suppose que nous pourrions deviner une intention en fonction de leur page d&#39;entrée, mais avec une seule page vue, il n&#39;y a tout simplement pas assez d&#39;informations pour faire une hypothèse éclairée de l&#39;intention.

![Définition de segment](assets/segment-def.png)

Après avoir défini ce segment, vous commencerez à voir l’espace de travail d’intention de visite prendre forme.

![Plus de définitions de segment](assets/more-segment-defs.png)

La création de segments de parcours client à l’aide d’Adobe Analytics est un processus difficile mais enrichissant. En créant des segments basés sur le comportement, en estimant la taille des audiences et en suivant les mouvements des utilisateurs, les entreprises peuvent personnaliser les médias et améliorer l’expérience client. Chaque entreprise est unique et il n’existe pas de formules spécifiques pour créer des segments, mais des instructions et un processus à suivre. Les segments doivent être mis à jour au fur et à mesure que les entreprises découvrent leurs clients, ce qui présente des défis en termes de création de rapports. En suivant le processus de création de segments d’intention de visite, les entreprises peuvent améliorer l’expérience client globale.

## Auteur

Ce document a été rédigé par :

![Aaron Fossum](assets/aaron-headshot.png)

**Aaron Fossum**, Director, Digital Analytics

Adobe Analytics Champion


