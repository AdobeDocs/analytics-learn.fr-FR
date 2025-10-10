---
title: Présentation du panneau d’attribution et des intervalles de recherche en amont d’Adobe Analytics
description: Découvrez comment utiliser le panneau d’attribution et l’intervalle de recherche en amont pour comprendre le comportement des clients et personnaliser la manière dont les éléments de dimension reçoivent du crédit pour les événements de succès.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-06-20T00:00:00Z
jira: KT-13181
thumbnail: KT-13181.jpeg
exl-id: 1da9334b-0edb-4237-b7ca-57640865208c
source-git-commit: f1bb981a83eb698f4185a22c367346a9ddd0c755
workflow-type: tm+mt
source-wordcount: '1659'
ht-degree: 1%

---

# Présentation du panneau d’attribution et des intervalles de recherche en amont d’Adobe Analytics

Quand j&#39;ai commencé à penser au [panneau d&#39;attribution](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=fr) et à **intervalle de recherche en amont**, le concept de &#39;voyage *temps&#39;* m&#39;est immédiatement venu à l&#39;esprit ; puis, bien sûr, notre réponse typique à de nombreux nouveaux outils comme ceux-ci est de simplement remettre à plus tard leur utilisation, car ils ont l&#39;air si compliqués.

Honnêtement, regardez toutes ces options, les commutateurs, les panneaux, les lectures et les boutons.  Et sérieusement, parlons de ces lumières clignotantes compliquées, tuyaux, jauges... ATTENDEZ!!  Ce n&#39;est pas le moment de se distraire en parlant de machines à remonter le temps, nous n&#39;avons tout simplement pas le temps... ou est-ce le cas ?

Je reconnais que le **panneau d&#39;attribution** est un outil assez complexe; toutefois, notre travail typique d&#39;analystes, jour après jour, consiste à utiliser un autre de nos outils préférés et très complexes pour examiner également ce qui s&#39;est passé dans le passé. Cet outil s’appelle ***Adobe Analytics*** !  Donc, oui, pour répondre à notre question très pertinente, je crois que ces deux choses indiquent que nous avons amplement de temps.

Par conséquent, pourquoi devrions-nous permettre à quelque chose comme une petite peur de se mettre en travers du chemin d&#39;outils aussi étonnants, sophistiqués et puissants que ceux-ci qui nous permettent littéralement de regarder *en arrière* dans le temps, chaque jour ?

Après tout - c&#39;est le VOYAGE DANS LE TEMPS, les amis!!  On est tous sur ce genre de choses.  A droite ???!!

Alors, qu&#39;attendons-nous - une voiture en métal brillant, une cabine de police, ou une cabine téléphonique vintage utilisant le câblage d&#39;un vieux parapluie comme antenne pour apparaître sur le pas de notre porte ?

Non !  Nous avons quelque chose d&#39;encore mieux, alors accrochons-nous !

Eh bien... tu comprends l&#39;idée.


Maintenant que nous sommes tous enthousiastes à l’idée de voyager dans le temps, prenons une grande inspiration, prenons un peu de recul, définissons ce qu’est **le panneau d’attribution** *vraiment* et ventilons un peu les choses :

![Attribution](assets/attribution.png)

*Figure 1 : les nombres affichés sont alignés avec le texte plus bas*

Dans **attribution**, réfléchissez simplement à la manière dont les événements/actions peuvent être causés par un individu, plusieurs individus ou un événement parmi un certain nombre d’événements différents au fil du temps.

Selon [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=fr), *attribution* permet aux analystes de personnaliser la manière dont les éléments *Dimension* sont crédités pour les *événements de succès*.


>[!WARNING]
>
>Les **modèles d’attribution** sont si fréquemment associés aux **canaux marketing** que j’ai délibérément *barré* ❷ CANAL dans l’image ci-dessus pour illustrer qu’il est possible d’effectuer une analyse **attribution** par rapport à la plupart des autres ***dimension***.


En fait, un parcours client donné est rarement réellement linéaire et encore moins souvent prévisible.  De plus, chaque client avance à son propre rythme ; souvent, il peut doubler d’avance, décrocher, abandonner ou adopter un autre comportement non linéaire. Ces actions organiques rendent difficile, voire pratiquement impossible, de connaître l’impact des efforts marketing sur le parcours client. Cela complique également les efforts visant à relier plusieurs canaux de données.

C&#39;est vrai.  Laissez vos analogies « domino » à l&#39;entrée et ouvrez vos esprits à des concepts plus proches de l&#39;effet papillon et de la théorie des cordes - mais comme tout le reste, nous devons commencer par quelques bases.

## **Modèles d’attribution**

Lorsque nous utilisons le panneau **attribution**, nous pouvons commencer à observer plusieurs choses différentes.  Par exemple, les **modèles d’attribution** nous montrent comment nos *conversions* (c’est-à-dire ❶ **mesures de succès**) peuvent être distribuées entre *accès* dans un groupe donné.

En termes simples, si **10 personnes** appuyez sur un **GRAND BOUTON ROUGE** pour franchir une porte, nos **modèles d&#39;attribution** vont nous dire laquelle de ces **10 personnes** nous voulons attribuer le « crédit » - ou mieux encore, combien *de « crédit »* nous voulons leur attribuer - pour avoir appuyé sur ledit bouton.

![Bouton](assets/button.png)

Dans cette optique, voici quelques exemples de la manière dont les ❸ **modèles d’attribution** peuvent affecter ces **10 personnes** :

- **Première touche** : ce modèle fonctionne exactement comme il semble en attribuant un crédit de **100 %** à la *première* personne qui a franchi la porte.  Les marketeurs sont plus susceptibles d’utiliser cette approche pour des tactiques telles que ***médias sociaux*** ou ***affichage*** ; cependant, il s’agit également d’une excellente tactique à utiliser souvent pour l’efficacité des recommandations de produits sur site.
- **Dernière touche** : cette tactique fonctionne également exactement comme elle le semble, mais donne plutôt **100 % de crédit** à la DERNIÈRE personne qui a franchi la porte.  Ce modèle est généralement utilisé pour analyser des éléments tels que la recherche ***naturelle (organique)*** et d’autres campagnes de cycle marketing *à court terme*.
- **Linéaire** : ce modèle distribue un crédit égal à CHAQUE PERSONNE qui a franchi la porte.

  >[!CAUTION]
  >
  >La prudence est toutefois recommandée dans ce cas, car vous avez la possibilité de diffuser vos résultats très finement et très rapidement lors de l’application de cette tactique, compte tenu de sa durée et de l’ampleur de l’audience touchée.

- **En U** : cette approche attribue **40 %** du crédit à la *première personne* dans la porte, répartit **20 %** du crédit entre *toutes les personnes entre les deux*, puis donne **40 %** au **dernier** à travers. Ce modèle sera le plus souvent utilisé dans les situations où vous avez un **long cycle de conversion/vente** contenant *plusieurs points de contact* en cours de route.  Dans ce cas, votre objectif est principalement de mettre en évidence les ***première*** et ***dernière*** tactiques marketing qui ont contribué à la conversion des clients.
- **J**-**Shaped** et **Inverse J** :
   - Pensez à **en U**, mais à la place, ce modèle attribue **60%** crédit à la *dernière personne* qui passe la porte, **20%** à la *première*, puis *divise* les 20%**restants à** tout le monde **&#x200B; au milieu.  &#x200B;** Inverse J** fait exactement le contraire.

     L&#39;objectif ici est de mettre l&#39;accent, soit au *début* soit à la *fin* de votre campagne ; cependant, vous voulez quand même attribuer un certain crédit à l&#39;élément contributeur à l&#39;autre bout tout en reconnaissant les « petits » en cours de route.

- **Décroissance temporelle** : Maintenant, je m&#39;en voudrais de ne pas partager celui-ci. Ce modèle a littéralement une demi-vie qui se désintègre de manière exponentielle - au fil du temps !  Dans ce cas, le paramètre *par défaut* de la demi-vie de ce modèle est de **7 jours**.  Son fonctionnement consiste à appliquer ensuite *poids* à chaque **canal marketing**, *en fonction du temps écoulé* après le *point de contact initial* et lorsque le client effectue une conversion.

  Les modèles d’attribution **Atténuation temporelle** et **En U** sont généralement utilisés pour mesurer les campagnes à plus long terme, mais comme vous pouvez le constater, ils ont des objectifs légèrement différents, en fonction de la manière dont ils *pèsent* la valeur du résultat.

- **Personnalisé** : Vous choisissez qui va obtenir du crédit.  C&#39;est votre campagne !

Pour plus d’informations à ce sujet et sur les autres modèles d’attribution, [cliquez ici](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=fr)

Pour rendre cela encore plus intéressant, parlons de revenir en arrière !

## **Intervalles de recherche en amont**

Il est maintenant temps de passer à un autre niveau.  C’est là que nous ajoutons littéralement l’élément du voyage dans le temps à notre analyse - et, encore une fois, nous commençons par les principes de base.

***Adobe*** définit ❹ **intervalles de recherche en amont** comme « la durée pendant laquelle une conversion doit rechercher des points de contact inclus. Les modèles d’attribution qui accordent plus de crédit aux premières interactions constatent des différences plus importantes lors de l’affichage de différents intervalles de recherche en amont. »


En d’autres termes, les **intervalles de recherche en amont** déterminent la période pendant laquelle les *conversions* sont prises en compte et fournissent *contexte* à l’analyse d’attribution. ***Adobe Analytics*** offre trois types d’intervalles de recherche en amont **lookback** :

- **Intervalle de recherche en amont d’une visite :** recherche le début d’une ***visite*** lorsqu’une conversion s’est produite, ce qui fournit des informations sur les interactions immédiates menant aux conversions.

  N’oubliez pas qu’il s’agit généralement du **intervalle de recherche en amont** le plus court à utiliser.
- **Intervalle de recherche en amont du visiteur :** examine toutes les ***visites*** depuis le premier du mois au cours de la période **sélectionnée**, ce qui offre une vue beaucoup plus large des interactions du client et permet d’identifier des modèles au fil du temps.
- **Intervalle de recherche en amont personnalisé :** permet d’étendre le **intervalle d’attribution** au-delà de la période **de création de rapports** jusqu’à un *maximum* de **90 jours**.  Il offre *flexibilité* pour capturer les points de contact qui se sont produits *en dehors* de la **période** sélectionnée, ce qui permet d’assurer une analyse complète.

En ajustant un **intervalle de recherche en amont** donné, les analystes peuvent ensuite examiner l’impact d’un ou de plusieurs points de contact au cours de périodes spécifiques et obtenir de plus amples informations sur la manière dont différentes durées affectent les résultats de l’attribution.

## **Tout rassembler**

Alors, qu&#39;est-ce que tout cela signifie pour nous en tant qu&#39;analystes ?

Le **panneau d’attribution** et **intervalle de recherche en amont** nous permettent de regarder au-delà des données courantes au niveau de la surface, et d’approfondir notre analyse du parcours client. En identifiant les points de contact qui ont eu le plus d’impact sur les *conversions*, nous pouvons prendre des décisions éclairées concernant nos stratégies marketing et allouer les ressources plus efficacement.

N’oubliez pas qu’une fois vos **modèles d’attribution** et **intervalles de recherche en amont** sélectionnés, vous pouvez encore manipuler vos données en les filtrant avec un ❺ **segment** ou tout autre composant de votre choix à ce stade.  De plus, une fois le panneau rendu, vous disposez de toutes les fonctionnalités d’un Workspace traditionnel.

## **Enfin la mise en pratique**

Maintenant que vous avez défini les concepts, imaginez que vous lancez une campagne marketing et que vous essayez de déterminer quel canal est le *plus efficace* pour générer des conversions. À l’aide du **panneau d’attribution**, vous pouvez non seulement voir la **dernière touche**, mais également la **première touche**, **même touche** et tout autre **modèle** que vous choisissez pour déterminer quels **canaux** sont les *plus efficaces* dans la conduite de vos *conversions*. Ensuite, ces informations peuvent être utilisées pour *optimiser* vos campagnes et améliorer les performances globales simplement en remontant le temps avec l’intervalle de recherche en amont **lookback** de votre choix.

Maintenant que vous avez vu ce qu’il peut faire, ne vous laissez pas berner ou intimider par les fonctionnalités apparemment complexes du panneau d’attribution.  **Regardez les choses en face**.  *Embrasse* ça.  **Comprenez** ça.
MAIS SURTOUT - *Utilisez-le à votre avantage.* Le **panneau d’attribution** et **intervalle de recherche en amont** sont les clés pour acquérir une meilleure compréhension de vos clients et de leur parcours envers votre marque.

Désormais, nous pouvons voyager « [&#x200B; dans le passé »](https://youtu.be/gVryJmZNFdU) en toute confiance et utiliser la puissance de notre machine à remonter le temps fiable (également appelée ***Adobe Analytics***) pour prendre des décisions basées sur les données.

## Auteur

Ce document a été rédigé par :

![&#x200B; Jeff Bloomer &#x200B;](assets/jeff-headshot.png)

**Jeff Bloomer**, responsable, Analyses numériques chez Kroger Personal Finance

Adobe Analytics Champion
