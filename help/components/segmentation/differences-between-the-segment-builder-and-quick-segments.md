---
title: Différences entre le créateur de segments et les segments rapides dans Analysis Workspace
description: Les segments peuvent être l’un des outils les plus puissants de votre boîte à outils d’analyse des données. Découvrez les différences entre l’utilisation du créateur de segments et des segments rapides dans Analysis Workspace pour plus d’efficacité.
feature: Segmentation
role: User
level: Beginner
doc-type: article
kt: KT-13118
source-git-commit: 9484b2e981d78be59b6ea16eeae2cf6f212c81ab
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 1%

---


# Différences entre le créateur de segments et les segments rapides dans Analysis Workspace

Les segments peuvent être l’un des outils les plus puissants de votre boîte à outils d’analyse des données. Découvrez les différences entre l’utilisation du créateur de segments et des segments rapides dans Analysis Workspace pour plus d’efficacité.

>[!TIP]
>
> Cliquez sur l’image en bas de la page pour télécharger un rappel utile indiquant à quel moment utiliser chaque outil dans Analysis Workspace.

Les segments peuvent être l’un des outils les plus puissants de votre boîte à outils d’analyse des données. Lorsque vous souhaitez examiner des groupes spécifiques de trafic, de sections de site ou de parcours clients, l’utilisation de segments peut être un excellent moyen de concentrer votre analyse sur un sous-ensemble particulier de trafic qui accède à votre site. Dans un environnement de vente au détail, certains des segments les plus utiles que j’ai créés concernent différents types de groupes de clients, par exemple les nouveaux clients par rapport aux clients existants, les clients connectés à un compte par rapport aux invités, etc. Mais vous pouvez également les créer pour différentes sections du site, des clients qui effectuent des actions spécifiques ou tout ce à quoi vous pouvez penser !

**Il existe deux méthodes principales pour créer des segments :**

* Utilisation du créateur de segments dans le menu Composants
* Utilisation des segments rapides en haut d’un panneau

Si vous créez votre segment à l’aide du créateur de segments, vous pouvez l’enregistrer pour le réutiliser dans d’autres projets. C’est un excellent moyen de se concentrer sur des groupes de clients spécifiques, par exemple, les personnes qui visitent certaines sections du site, puis effectuent un achat. D’un autre côté, si vous effectuez une analyse exploratoire et souhaitez tester différents paramètres de segment, le créateur de segments rapide peut vous être très utile. Examinons quelques-uns des principaux avantages de chaque méthode.

## Segments rapides

Dans la partie supérieure de chaque panneau, vous pouvez cliquer sur l’icône de segment rapide (un entonnoir avec le symbole +) pour ouvrir le créateur. Vous pouvez ainsi créer un segment à n’importe quel niveau (accès, visite ou visiteur) avec trois conditions au maximum. Tout comme le créateur de segments principal, il vous donne une indication sur le côté droit qui indique si le segment renvoie des données et % de la population de trafic globale inclus dans le segment, bien qu’il s’agisse d’une version plus simplifiée que l’affichage de volume de segment complet affiché dans le créateur de segments. Lors de l’ajout de plusieurs conditions, vous pouvez utiliser les opérateurs &quot;et&quot; et &quot;ou&quot;. Malheureusement, il n’existe pas d’option &quot;Then&quot; pour les segments rapides. Par conséquent, si vous avez besoin de segments séquentiels, vous devrez utiliser le créateur de segments complet. Il existe également une limite d’un conteneur dans un segment rapide. Puisqu’il est destiné à être utilisé pour les segments de base qui peuvent être créés et modifiés rapidement. Une fois qu’un segment rapide est appliqué à un panneau ou enregistré, il ne peut plus être modifié dans le panneau.

Lors d’une analyse exploratoire et que vous souhaitez tester différents types de segments afin de déterminer la réaction de différents groupes de clients ou les performances de différentes catégories, l’utilisation de segments rapides est beaucoup plus rapide que l’utilisation du créateur de segments. En outre, ces segments ne sont disponibles que dans le projet dans lequel ils ont été créés. Par conséquent, s’il s’avère que ne fournit pas les résultats souhaités, vous n’avez pas à vous soucier de supprimer le segment enregistré de la liste principale. Si, après avoir testé les segments, vous réalisez qu’ils seront utiles dans d’autres projets, vous pouvez toujours cliquer sur le bouton &quot;Ouvrir le créateur&quot; pour ouvrir le segment dans le créateur de segments complet afin de l’enregistrer comme segment normal. Une fois que vous avez effectué cette opération, vous ne pourrez toutefois plus la modifier dans le créateur de segments rapide.

![Segment rapide](assets/quick-segement.png)

## Créateur de segments

Pour accéder au créateur de segments, cliquez sur le symbole + situé au-dessus de la liste des segments dans le menu Composants de gauche, ou cliquez sur la liste déroulante Composants et sélectionnez &quot;Créer un segment...&quot;. Contrairement aux segments rapides, toutes les options sont disponibles. Pour ajouter plusieurs conditions, vous pouvez créer des segments séquentiels à l’aide de l’opérateur &quot;then&quot;. Les segments séquentiels vous permettent également d’utiliser &quot;groupe logique&quot; comme niveau (au lieu d’accès, de visite ou de visiteur). Le créateur de segments vous permet également d’ajouter une description aux segments, qui peut ajouter du contexte sur la personne qui a créé le segment ou le type de données qu’il a été créé pour le filtrer, ou même simplement ajouter des &quot;balises&quot; au segment à des fins d’organisation. Ces deux éléments ne sont pas possibles dans le créateur de segments rapide.

L’utilisation du créateur de segments est essentielle lorsque votre segment comporte plus de 3 conditions, si vous devez utiliser des conteneurs ou si vous souhaitez des segments séquentiels. Le créateur de segments complet dispose de beaucoup plus d’options pour créer des segments plus complexes, ce qui peut vous aider à ventiler différents types de clients, catégories, parcours de clients, etc. Une fois ces segments créés et enregistrés, ils sont ajoutés à la liste principale des segments, ce qui signifie qu’ils peuvent être balisés, approuvés, partagés, utilisés dans plusieurs rapports et publiés sur l’Experience Cloud. La publication dans l’Experience Cloud vous permet d’utiliser le segment dans d’autres produits Adobe, comme dans Adobe Target pour le ciblage de personnalisation. Les segments créés dans le créateur de segments ne peuvent pas être modifiés dans le panneau des segments rapides. Vous devez ouvrir le créateur de segments pour y apporter des modifications. Heureusement, la visualisation d’aperçu à droite fournit une analyse plus détaillée du trafic que le segment amènerait au cours des 90 derniers jours, ce qui signifie qu’il est plus facile de s’assurer que le segment apporte ce à quoi vous souhaitez qu’il arrive avant l’enregistrement.

![Créateur de segments](assets/segment-builder-quick.png)

## Cas d’utilisation

Dans différents secteurs d’activité, vos utilisations pour la création de segments personnalisés peuvent différer. Travaillant pour la division e-commerce d’un grand détaillant, nous effectuons souvent des analyses exploratoires afin de déterminer les chemins empruntés par les clients pour acheter. Lorsque nous constatons des pics ou des baisses d’actions, comme l’ajout de produits à un panier ou le placement de commandes, c’est là que l’utilisation des segments rapides peut s’avérer utile. Au cours d’une analyse, je peux rapidement créer un segment pour un type spécifique de client ou pour une action ou un lien particulier sur lequel il clique. En n’ayant pas à ouvrir le créateur de segments et à enregistrer chaque segment, je peux ajouter rapidement les conditions, puis les supprimer aussi rapidement. Cela permet de gagner beaucoup de temps en essayant d’expliquer pourquoi nous voyons un changement sur notre site.

Parfois, le créateur de segments m’a également été utile. Tous les clients ne sont pas identiques et nous voulons souvent examiner des types spécifiques de clients identifiés par des actions ou des chemins qu’ils empruntent. En utilisant le créateur de segments, nous pouvons ajouter plusieurs conditions pour identifier les différents types de clients et enregistrer les segments afin qu’ils puissent être partagés et utilisés par plusieurs analystes. Il est important que ces types de segments soient cohérents entre les rapports. Dès lors, la création d’un segment que tout le monde peut utiliser est préférable à celle de chaque personne qui crée sa propre version, car les résultats peuvent différer.

Dans l’ensemble, les segments rapides et le créateur de segments sont d’excellents outils à utiliser dans votre analyse. Chacun d&#39;eux a ses objectifs, ses avantages et ses inconvénients. Pour consulter un guide de référence rapide, reportez-vous à notre feuille de conseils et astuces téléchargeables pratique ci-dessous.

## Auteur

Ce document a été rédigé par :

![Mandy George](assets/mandy-george.jpg)

**Mandy George**, Digital Analytics III à Best Buy Canada

Adobe Analytics Champion

## Télécharger

[![Téléchargement rapide de segments](assets/quick-segments-download-small.jpg)](assets/Adobe_Analytics_Segments_Vs_Segment_Builder_Reference_Guide.pdf)
