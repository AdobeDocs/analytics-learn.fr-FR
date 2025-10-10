---
title: Créer des segments de parcours client
description: Découvrez comment créer des segments de parcours client basés sur le comportement dans Adobe Analytics et améliorer l’expérience de vos clients avec Adobe Experience Cloud en suivant ce guide détaillé.
feature: Segmentation
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13180
thumbnail: KT-13180.jpeg
exl-id: c06afc7b-e997-404d-82a4-e7ec5d5ba44d
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1243'
ht-degree: 1%

---

# Créer des segments de parcours client

Découvrez comment créer des segments de parcours client basés sur le comportement dans Adobe Analytics et améliorer l’expérience de vos clients avec Adobe Experience Cloud en suivant ce guide détaillé.

Créons de meilleurs segments de parcours client ! Dans cette série, nous utiliserons Adobe Analytics pour définir des segments comportementaux, estimer les tailles d’audience et suivre les mouvements des utilisateurs. À la fin, vous serez en mesure de personnaliser les médias et d’améliorer l’expérience de vos clients avec Adobe Experience Cloud. Gardez à l’esprit que ces segments sont actifs et doivent être mis à jour au fur et à mesure que vous en apprenez plus sur vos clients. Bien que les rapports puissent présenter certains défis, ne vous inquiétez pas, je vous guiderai à travers cela ! Commençons par créer notre premier ensemble de segments de Parcours client, en commençant par le segment « Merveilles à un seul accès ».

Aujourd’hui, nous allons créer des espaces réservés pour notre premier ensemble de segments de Parcours client, créer un Workspace Adobe Analytics pour nous aider à définir nos segments et définir notre tout premier segment, « Merveilles à un accès ».

D’ici la fin de cette série, vous pourrez créer des segments de parcours client dans Adobe Analytics en fonction de signaux comportementaux. Vous pourrez estimer la taille de chaque audience à chaque étape du parcours et connaître le taux de déplacement des utilisateurs entre ces étapes. Vous pourrez également exporter ces audiences de parcours client vers Adobe Experience Cloud pour activer la personnalisation et le ciblage multimédia.

Chaque entreprise est différente, ce qui signifie que vos segments de parcours client seront différents des miens. Ainsi, plutôt que de prescrire des formules spécifiques pour vos segments, suggérez quelques éléments à examiner et un processus global pour les créer.

Il est également important de noter que vos segments de parcours client seront des segments vivants. Il ne s&#39;agit pas d&#39;un exercice ponctuel. Au fur et à mesure que vous en apprendrez plus sur vos clients, vous mettrez à jour ces segments. Cela présente certains défis pour la création de rapports. Les utilisateurs souhaitent une cohérence dans leurs rapports. Si nos définitions de segment changent, les nombres dans les rapports changent également.

## Prise en main des segments d’intention de visite

La première étape de création de segments de parcours client consiste à déduire la raison pour laquelle un invité se trouve sur votre site web à l’aide de signaux de comportement et, le cas échéant, de données de la voix du client. Nous allons créer un ensemble de segments d’intention de visite pour classer toutes les visites sur le site web. À ce stade, nos segments d’intention de visite doivent s’exclure mutuellement et être complètement exhaustifs. Chaque visite doit appartenir à un segment d’intention de visite et à un seul segment.

Les segments Intention de visite décrivent une visite. Nous utiliserons donc le conteneur Visites dans la définition de segment.

Mon ensemble initial de segments d’intention de visite comprenait :

* Les merveilles d&#39;un seul coup
* Sensibilisation
* Considération
* Réservation (achat)
* Rétention (Gérer une réservation/un achat)

Pour faciliter l’utilisation de mes segments avec intention de visite, j’ai ajouté le préfixe « Intention : » à mes noms de segment, je leur ai donné un nombre pour activer le tri et je les ai balisés « intention ». Mes segments ressemblaient à l’image ci-dessous.

![segments d’intention &#x200B;](assets/intent-segments.png)

**Créez vos segments d’intention de visite à l’aide du conteneur Visites avec une définition d’espace réservé de Pages vues >= 1.**

Comme nous le verrons, la création de ces segments est un processus itératif et interconnecté. Je décrirai le processus de création de ces segments dans un prochain article.

## Workspace de qualité des données du segment d’intention de visite

![espace de travail intention de visite](assets/visit-intent-workspace.png)

J’ai utilisé un espace de travail simple pour m’assurer que je définissais bien mes segments d’intention de visite. N’oubliez pas que chaque visite doit appartenir à un seul segment d’intention de visite. L’espace de travail que j’ai configuré garantit que toutes les visites sont prises en compte et qu’il n’y a pas de chevauchement entre les segments.

J’ai nommé cet espace de travail « QUALITÉ DES DONNÉES : segments d’intention de visite » avec les balises « qualité des données », « intention de visite » et « parcours client ». Plus tard, nous allons créer un « Tableau de bord de l’intention de visite » afin que le préfixe « QUALITÉ DES DONNÉES » indique que cet espace de travail sert à configurer et à gérer les segments. Il s’agit d’un tableau de bord administratif qui comporte assez peu d’insight métier, mais qui est important pour s’assurer que les segments sont conservés. Nous vous recommandons de revenir régulièrement à ce tableau de bord ou de configurer des alertes pour vous assurer que vos segments restent correctement définis.

La visualisation la plus importante de cet espace de travail est la visualisation à structure libre Chevauchement de segments , au milieu à gauche. À l’aide de la mesure Visites , créez des filtres de colonne pour chacun de vos segments d’intention de visite, ainsi que le segment Toutes les visites dans la colonne la plus à droite. Créez des lignes pour chaque segment avec intention de visite sur la gauche. Vous disposez désormais d’une visualisation entre onglets. Lorsque vos segments sont correctement configurés, il n’y a que des données dans une colonne et une ligne, à l’intersection de chaque segment d’intention de visite avec lui-même.

Les visualisations les plus importantes suivantes sont les mesures récapitulatives en haut à gauche. Le résumé des visites segmentées prend sa valeur dans la colonne Toutes les visites de la visualisation Chevauchement des segments immédiatement ci-dessous. Le résumé Toutes les visites comporte son propre tableau masqué.

![toutes les visites](assets/all-visits.png)

En haut à droite, j’ai ajouté des mesures supplémentaires à chacun des segments pour donner un aperçu de la mise en forme des segments. En particulier, comme ces segments s’excluent mutuellement, je m’attends uniquement à voir les réservations pour le segment Intention de réservation (ne craignez pas, nous atteindrons les taux de conversion lorsque ces segments Intention de visite seront basés sur les visiteurs.

N’oubliez pas que nous venons de créer des segments d’espace réservé. Ainsi, au début, votre espace de travail aura l’air bancal. Tous vos segments d’intention de visite se chevauchent à 100 %, car ils ont la même définition. C&#39;est exact, et c&#39;est exactement ce que vous voulez voir à ce stade du processus. À mesure que nous créerons les définitions de segment, vous commencerez à voir ces segments commencer à prendre forme.

![Définitions de segment d’intention de visite](assets/visit-intent-segment-defs.png)

## Création de votre premier segment d’intention de visite

La définition des segments d’intention de visite est un peu un processus d’élimination, et il y a beaucoup d’interdépendance entre eux. Donc je n&#39;ai pas construit ces segments dans l&#39;ordre du parcours, je les ai construits dans l&#39;ordre du plus facile à définir au plus difficile. Cela m&#39;a donné cet ordre :

1. Intention : 0 - Un Accès Aux Merveilles
1. Intention : 3 - Réservation
1. Intention : 4 - Rétention
1. Intention : 2 - Considération
1. Intention : 1 - Sensibilisation

Plutôt aléatoire, hein ? La définition de ces segments d’intention de visite était un processus itératif, de va-et-vient, et souvent un ajustement à un segment nécessitait des mises à jour d’autres segments. Cela deviendra plus clair lorsque je décrirai comment j’ai défini chacun de ces segments.

Aujourd’hui, nous allons définir notre premier segment, les plus faciles, les merveilles d’un seul accès

## Création du segment des merveilles avec un seul accès

Mon premier segment, « One Hit Wonders », était facile à définir. Il s’agit simplement de toute visite avec une seule page vue. Nous ne savons vraiment pas pourquoi cet utilisateur était sur le site Web, parce qu&#39;il a rebondi. Je suppose que nous pourrions deviner une intention en fonction de leur page d&#39;entrée, mais avec une seule page vue, il n&#39;y a tout simplement pas assez d&#39;information pour faire une estimation éclairée de l&#39;intention.

![Définition du segment](assets/segment-def.png)

Après avoir défini ce segment, vous commencerez à voir votre Workspace d’intention de visite prendre forme.

![Plus de définitions de segment](assets/more-segment-defs.png)

La création de segments de parcours client à l’aide d’Adobe Analytics est un processus difficile mais gratifiant. En créant des segments basés sur le comportement, en estimant la taille des audiences et en suivant les mouvements des utilisateurs, les entreprises peuvent personnaliser les médias et améliorer l’expérience client. Chaque entreprise est unique et il n’existe pas de formule spécifique pour créer des segments, mais des directives et un processus à suivre. Les segments doivent être mis à jour à mesure que les entreprises en apprennent plus sur leurs clients, ce qui présente des défis en matière de création de rapports. En suivant le processus de création des segments d’intention de visite, les entreprises peuvent améliorer l’expérience client globale.

## Auteur

Ce document a été rédigé par :

![Aaron Fossum &#x200B;](assets/aaron-headshot.png)

**Aaron Fossum**, directeur, Analytique numérique

Adobe Analytics Champion
