---
title: Différences entre le créateur de segments et les segments rapides dans Analysis Workspace
description: Apprivoisez les segments et bénéficiez de l’un des outils d’analyse des données les plus performants. Découvrez les différences entre le créateur de segments et les segments rapides dans Analysis Workspace et utilisez-les à bon escient.
feature: Segmentation
role: User
level: Beginner
doc-type: article
kt: KT-13118
exl-id: fefadd3c-820b-4e53-bd76-e51cb52c33e1
source-git-commit: 5ad32bd6cb6046ab54ecf31ebcf643f758d9ecc5
workflow-type: ht
source-wordcount: '1264'
ht-degree: 100%

---

# Différences entre le créateur de segments et les segments rapides dans Analysis Workspace

Apprivoisez les segments et bénéficiez de l’un des outils d’analyse des données les plus performants. Découvrez les différences entre le créateur de segments et les segments rapides dans Analysis Workspace et utilisez-les à bon escient.

>[!TIP]
>
> Cliquez sur l’image au bas de la page et téléchargez le document reprenant les différents scénarios d’utilisation de chaque outil dans Analysis Workspace.

Apprivoisez les segments et bénéficiez de l’un des outils d’analyse des données les plus performants. Lorsque vous souhaitez en savoir plus sur des groupes spécifiques de trafic, des sections de site ou des parcours clients, les segments peuvent répondre à vos besoins et cibler l’analyse sur un sous-ensemble particulier de trafic sur votre site. Dans un environnement de vente au détail, les segments les plus utiles portent sur les différents types de groupes de clients, par exemple la nouvelle clientèle par rapport à la clientèle existante, la clientèle connectée à son compte ou les invités et invitées, etc. Mais vous pouvez également créer des segments en fonction des différentes sections du site, des clients et clientes qui effectuent des actions spécifiques ou de toute autre événement qui vous vient à l’esprit !

**Vous pouvez créer des segments de deux façons :**

* à l’aide du créateur de segments (dans le menu Composants)
* à l’aide des segments rapides (en haut d’un panneau)

Si vous créez un segment à l’aide du créateur de segments, vous pouvez l’enregistrer afin de le réutiliser dans d’autres projets. Ils se révèlent précieux pour cibler des groupes de clients ou de clientes spécifiques, par exemple, les personnes qui visitent certaines sections du site, puis réalisent un achat. En revanche, si vous lancez une analyse exploratoire et souhaitez tester différents paramètres de segment, le créateur de segments rapides peut se révéler idéal. Comparons les avantages de chaque outil.

## Segments rapides

Dans la partie supérieure de chaque panneau, cliquez sur l’icône de segment rapide (un entonnoir avec le symbole +) pour ouvrir le créateur. Vous pouvez créer un segment à n’importe quel niveau (accès, visite ou visiteur et visiteuse) avec jusqu’à trois conditions. Tout comme le créateur de segments principal, le côté droit vous indique si le segment renvoie des données et le pourcentage de la population totale du trafic incluse dans le segment. Il s’agit toutefois d’une version simplifiée de la vue complète du volume de segment affichée dans le créateur de segments. Lors de l’ajout de plusieurs conditions, vous pouvez utiliser les opérateurs « AND » et « OR ». Il n’existe hélas pas d’option « Then » pour les segments rapides. Si vous avez besoin de segments séquentiels, vous devez donc utiliser le créateur de segments complet. De plus, le segment rapide est limité à un conteneur. Tout l’intérêt du créateur de segments rapides réside dans la création et modification rapides de segments de base. Une fois qu’un segment rapide est appliqué à un panneau ou enregistré, il ne peut plus être modifié dans le panneau.

Lorsque vous effectuez une analyse exploratoire et que vous souhaitez tester différents types de segments pour voir comment différents groupes de clients ou clientes réagissent ou comment différentes catégories se comportent, utilisez les segments rapides, car leur création est beaucoup plus rapide que les segments complets. En outre, ces segments ne sont disponibles que dans le projet dans lequel ils ont été créés. Nul besoin donc de supprimer le segment enregistré de la liste principale si vous n’obtenez pas les résultats souhaités. Une fois les segments testés, si vous estimez qu’ils seront utiles dans d’autres projets, il vous suffit de cliquer sur le bouton « Ouvrir le créateur » pour afficher le segment dans le créateur de segments complet et l’enregistrer en tant que segment standard. Notez qu’une fois cette opération effectuée, vous ne pourrez plus modifier le segment dans le créateur de segments rapides.

![Segment rapide](assets/quick-segement.png)

## Créateur de segments

Pour accéder au créateur de segments, cliquez sur le symbole + situé au-dessus de la liste des segments dans le menu Composants, situé à gauche, ou cliquez sur la liste déroulante Composants et sélectionnez « Créer un segment… ». Contrairement aux segments rapides, toutes les options sont disponibles. Pour ajouter plusieurs conditions, vous pouvez créer des segments séquentiels à l’aide de l’opérateur « THEN ». Les segments séquentiels vous permettent également d’utiliser le « groupe logique » comme niveau (au lieu de l’accès, de la visite ou du visiteur et de la visiteuse). Le créateur de segments vous permet également d’ajouter une description aux segments, afin de renseigner sur la personne qui a créé le segment ou le type de données qu’il a été conçu pour filtrer. Vous pouvez aussi ajouter des « balises » au segment à des fins d’organisation. Ces deux opérations ne sont pas possibles dans le créateur de segments rapides.

Utilisez le créateur de segments si votre segment comporte plus de 3 conditions, si vous devez utiliser des conteneurs ou si vous souhaitez des segments séquentiels. Le créateur de segments complet dispose de beaucoup plus d’options pour créer des segments plus complexes, ce qui peut vous aider à ventiler différents types de clients, catégories, parcours clients, etc. Une fois ces segments créés et enregistrés, ils sont ajoutés à la liste principale des segments. Ils peuvent alors être balisés, approuvés, partagés, utilisés dans plusieurs rapports et publiés sur Experience Cloud. Une fois le segment publié dans Experience Cloud, il est disponible pour d’autres produits Adobe, comme Adobe Target pour le ciblage de personnalisation. Les segments créés dans le créateur de segments ne peuvent pas être modifiés dans le panneau des segments rapides. Vous devez ouvrir le créateur de segments complet pour y apporter des modifications. Heureusement, la prévisualisation à droite fournit une analyse plus détaillée du trafic généré par le segment au cours des 90 derniers jours. Vous pouvez ainsi vous assurer plus facilement que le segment est conforme à vos attentes avant de l’enregistrer.

![Créateur de segments](assets/segment-builder-quick.png)

## Cas d’utilisation

Selon le secteur d’activité, la finalité des segments personnalisés peut être différente. Prenons l’exemple d’une division e-commerce d’un grand détaillant. Des analyses exploratoires sont régulièrement menées afin de déterminer les chemins empruntés par les clients et clientes avant d’acheter. Lorsque des pics ou des baisses d’actions sont recensés, comme l’ajout de produits à un panier ou le passage d’une commande, c’est là que l’utilisation des segments rapides peut s’avérer utile. Au cours d’une analyse, je peux rapidement créer un segment pour un type spécifique de client ou cliente ou pour une action ou un lien spécifique sur lequel il ou elle clique. Comme il n’est pas nécessaire d’ouvrir le créateur de segments et d’enregistrer chaque segment, je peux ajouter rapidement les conditions et les supprimer tout aussi rapidement. Cela permet de gagner un temps certain lorsqu’un changement survient sur le site.

Mais le créateur de segments complet n’est pas en reste. Tous les clients et clientes ne se ressemblent pas comme deux gouttes d’eau. Bien souvent, il s’avère utile d’examiner des types spécifiques de clients et clientes identifié(e)s par les actions ou chemins empruntés. Grâce au créateur de segments, il est possible d’ajouter plusieurs conditions pour identifier les différents types de clients et clientes, ainsi qu’enregistrer les segments en vue de leur partage ou emploi par plusieurs analystes. Il est important que ces types de segments soient cohérents entre les rapports. Il est donc préférable de créer un segment que tout le monde peut utiliser plutôt que de laisser chaque personne créer sa propre version, car les résultats peuvent différer.

En résumé, les segments rapides et le créateur de segments complet sont tous deux d’excellents outils à employer dans votre analyse. Chaque outil poursuit un objectif différent, avec ses avantages et ses inconvénients. Consultez notre guide de référence rapide et téléchargez notre fiche pratique de conseils et d’astuces ci-dessous.

## Auteur

Ce document a été rédigé par :

![Mandy George](assets/mandy-george.jpg)

**Mandy George**, analyste numérique III à Best Buy Canada

Adobe Analytics Champion

## Télécharger

[![Téléchargement des segments rapides](assets/quick-segments-download-small.jpg)](assets/Adobe_Analytics_Segments_Vs_Segment_Builder_Reference_Guide.pdf)
