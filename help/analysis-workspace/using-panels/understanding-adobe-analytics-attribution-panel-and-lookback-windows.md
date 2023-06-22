---
title: Présentation du panneau d’attribution Adobe Analytics et des intervalles de recherche en amont
description: Découvrez comment utiliser le panneau d’attribution et l’intervalle de recherche en amont pour comprendre le comportement des clients et personnaliser la manière dont les éléments de dimension obtiennent du crédit pour les événements de succès.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-06-20T00:00:00Z
jira: KT-13181
thumbnail: KT-13181.jpeg
source-git-commit: ae6fb85c3903986940463a4133f7b46f5efb64e1
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 2%

---


# Présentation du panneau d’attribution Adobe Analytics et des intervalles de recherche en amont

Quand j&#39;ai pensé à la [panneau d’attribution](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=en) et **intervalle de recherche en amont**, le concept de &quot;&quot; m&#39;a immédiatement rappelé.*voyage à l&#39;heure&#39;*; alors, bien sûr, on m&#39;a aussi rappelé que notre réponse typique à de nombreux nouveaux outils comme ceux-ci est simplement de reporter l&#39;utilisation, parce qu&#39;ils ont l&#39;air si compliqués.

Je veux dire, honnêtement, regardez toutes ces options, ces interrupteurs, ces panneaux, ces lectures, et ces boutons.  Et sérieusement, parlons de ces lumières clignotantes compliquées, des tuyaux, des jauges.... WAIT!!  Ce n&#39;est pas le moment de se laisser distraire en parlant de machines à remonter le temps, nous n&#39;en avons tout simplement pas le temps... ou est-ce que nous en avons le temps ?

J&#39;admettrai que **panneau d’attribution** est un outil assez complexe; cependant, notre travail typique d&#39;analystes, jour après jour, est d&#39;utiliser un autre de nos outils préférés et très complexes pour également examiner ce qui s&#39;est passé dans le passé. Cet outil s&#39;appelle ***Adobe Analytics***!  Donc oui, pour répondre à notre question très pertinente, je crois que ces deux choses disent que nous avons beaucoup de temps.

Par conséquent, pourquoi devrions-nous laisser quelque chose comme une petite peur se mettre en travers de ces outils incroyables, sophistiqués et puissants comme ceux-ci qui nous permettent littéralement de regarder *backward* dans le temps, chaque jour ?

Après tout - c&#39;est le VOYAGE DU TEMPS, les gars!!  Nous parlons de ce genre de choses.  Correct???!!

Alors, qu&#39;attendons-nous - une voiture en métal brillant, une boîte de police, ou une cabine téléphonique vintage utilisant le câblage d&#39;un vieux parapluie comme antenne pour apparaître sur le pas de notre porte ?

Non!  Nous avons quelque chose d&#39;encore mieux, alors raccrochons-nous !

Eh bien.. vous avez l&#39;idée.


Maintenant que nous sommes tous excités par les voyages dans le temps, prenons une profonde inspiration, recuchons un peu, établissons ce que la **panneau d’attribution** *vraiment* est et décomposez un peu les éléments suivants :

![Attribution](assets/attribution.png)

*Figure 1 - Nombre affiché en ligne avec le texte plus bas*

Dans **attribution**, il vous suffit d’examiner la manière dont les événements/actions peuvent être causés par un individu, plusieurs individus ou l’un des nombreux événements différents au fil du temps.

Selon [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=en), *attribution* permet aux analystes de personnaliser la manière dont *Dimension* les éléments reçoivent un crédit pour *événements de succès*.


**⛔** DETOUR : Juste une petite note pour rappeler que **modèles d’attribution** sont si fréquemment associés à **canaux marketing** que je suis intentionnellement *barré* CANAL dans l’image ci-dessus pour illustrer qu’il est possible d’effectuer **attribution** l’analyse par rapport à la plupart des autres ***dimension***.


En fait, rarement un parcours client donné est vraiment linéaire et encore moins prévisible.  De plus, chaque client procédera à son propre rythme. souvent, ils peuvent reculer, bloquer, abandonner ou adopter un autre comportement non linéaire. Ces actions organiques rendent difficile ou pratiquement impossible de connaître l’impact des efforts marketing sur le parcours client. Cela complique également les efforts visant à relier plusieurs canaux de données.

C&#39;est vrai.  Laissez vos analogies de &quot;domino&quot; à la porte et ouvrez vos esprits à des concepts plus proches de l&#39;effet papillon et de la théorie des cordes - mais comme tout le reste, nous devons commencer par quelques principes de base.

## **Modèles d’attribution**

Lorsque nous utilisons la variable **panneau d’attribution**, nous pouvons commencer à observer plusieurs choses différentes.  Par exemple, la variable **modèles d’attribution** nous montrer comment nous *conversions* (c.-à-d., ***mesures de succès***) peut être réparti entre les *accès* dans un groupe donné.

Autrement dit, si **10 personnes** appuyez sur **BOUTON GRAND ROUGE** pour passer par une porte, notre **modèles d’attribution** vont nous dire lequel de ceux-là **10 personnes** nous voulons attribuer un &quot;crédit&quot; - ou mieux encore dire, comment *many* &quot;crédit&quot; que nous voulons leur attribuer - pour appuyer sur ce bouton.

![Bouton](assets/button.png)

En gardant cela à l’esprit, voici quelques exemples de la façon dont le **modèles d’attribution** peuvent affecter les **10 personnes**:

- **Première touche**: Ce modèle fonctionne exactement comme s’il donnait la valeur **Crédit à 100 %** au *first* qui passa par la porte.  Les marketeurs sont plus susceptibles d’utiliser cette approche pour des tactiques telles que ***médias sociaux*** ou ***display***; cependant, il s’agit également d’une excellente tactique à utiliser souvent pour l’efficacité des recommandations de produits sur site.
- **Dernière touche**: Cette tactique fonctionne aussi exactement comme on dirait, mais à la place, donne **Crédit à 100 %** à la DERNIÈRE personne qui traversa la porte.  Ce modèle est généralement utilisé pour analyser des éléments comme ***recherche naturelle (organique)*** et autres *court terme* campagnes de cycle marketing.
- **Linéaire**: Ce modèle distribue un crédit égal à CHAQUE PERSONNE qui franchissait la porte.

Il est toutefois conseillé de faire attention, car vous avez la possibilité de diffuser vos résultats très rapidement lorsque vous appliquez cette tactique, en tenant compte du temps d’exécution et de l’audience plus grande qu’elle atteint.

- **En forme de U**: Cette approche attribue **40 %** du crédit à la variable *première personne* à la porte, des planches **20 %** de l’ensemble du crédit *tout le monde entre*, puis donne **40 %** au **last one** par . Ce modèle est le plus souvent utilisé dans les situations où vous avez une **cycle de conversion/vente long** contain *plusieurs points de contact* en chemin.  Dans ce cas, votre objectif est de mettre principalement en évidence la variable ***first*** et ***last*** tactiques marketing qui ont contribué à la conversion des clients.
- **J**-**En forme** et **Inverse J**:
   - Réfléchissez à **En forme de U**, mais à la place, ce modèle affecte **60 %** au *dernière personne* passer par la porte, **20 %** au *first*, puis *divides* le reste **20 %** cross *everyone* au milieu.  **Inverse J** fait exactement le contraire.

L’objectif ici est de mettre l’accent sur l’ *début* ou le *end* de votre campagne ; toutefois, vous souhaitez tout de même attribuer un certain crédit à l’élément de contribution de l’autre côté tout en reconnaissant les &quot;petits gars&quot; en cours de route.

- **Décroissance temporelle**: Maintenant, je manquerais à mon devoir si je ne partage pas celui-ci. Ce modèle a littéralement une demi-vie qui diminue exponentiellement - au fil du temps !  Dans ce cas, la variable *default* le paramètre de la demi-vie de ce modèle est **7 jours**.  Cela fonctionne de la manière suivante : *poids* à chaque **canal marketing**, *en fonction de la durée* qui passe après la *point de contact initial* et lorsque le client effectue la conversion.

  **Décroissance temporelle** et **Modèles d’attribution en forme de U** sont généralement utilisés pour mesurer les campagnes à plus long terme, mais comme vous pouvez le voir, ils ont des objectifs légèrement différents, en fonction de la manière dont ils sont finalement utilisés. *poids* la valeur du résultat.

- **Personnalisé**: Vous choisissez qui obtiendra du crédit.  C&#39;est votre campagne !

Pour plus d’informations sur ces modèles d’attribution et sur d’autres modèles d’attribution, [cliquez ici](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=fr)

Pour rendre cela encore plus intéressant, parlons de revenir en arrière !

## **Intervalles de recherche en amont**

Il est maintenant temps de commencer à penser à un autre niveau.  C&#39;est là que nous ajoutons littéralement l&#39;élément voyage dans le temps à notre analyse - et là encore, nous commençons avec les bases.

***Adobe*** définit **intervalles de recherche en amont** comme &quot;durée pendant laquelle une conversion doit revenir en arrière pour inclure des points de contact. Les modèles d’attribution qui accordent plus de crédit aux premières interactions voient des différences plus importantes lors de l’affichage de différents intervalles de recherche en amont.&quot;


En d&#39;autres termes, **intervalles de recherche en amont** déterminer la période pendant laquelle *conversions* sont considérés et fournissent *contexte* à l’analyse d’attribution. ***Adobe Analytics*** offre trois types de **intervalles de recherche en amont**:

- **Intervalle de recherche en amont des visites :** Revient au début d’une ***visite*** lorsqu’une conversion s’est produite, fournissant des informations sur les interactions immédiates menant aux conversions.

  N’oubliez pas que c’est généralement le plus court **intervalle de recherche en amont** à utiliser.
- **Intervalle de recherche en amont des visiteurs :** Recherche tout ***visites*** jusqu’au premier du mois dans la **période**, offrant une vue beaucoup plus large des interactions du client et permettant d’identifier les schémas au fil du temps.
- **Intervalle de recherche en amont personnalisé :** Permet de développer la variable **fenêtre d’attribution** au-delà du reporting **période** jusqu’à un *maximum* de **90 jours**.  Il fournit *flexibilité* lors de la capture des points de contact qui se sont produits *external* la sélection **période**, en assurant une analyse complète.

En ajustant une donnée **intervalle de recherche en amont**, les analystes peuvent alors examiner l’impact d’un ou de plusieurs points de contact au cours de périodes spécifiques et obtenir des informations plus approfondies sur la manière dont les différentes durées affectent les résultats d’attribution.

## **Rassembler tout cela**

Qu&#39;est-ce que tout cela signifie pour nous en tant qu&#39;analystes ?

Le **panneau d’attribution** et **intervalle de recherche en amont** nous donner le pouvoir de regarder au-delà des données ordinaires et superficielles, et de creuser plus profondément le parcours client. En comprenant quels points de contact ont eu le plus d’impact sur *conversions*, nous pouvons prendre des décisions éclairées sur nos stratégies marketing et allouer les ressources plus efficacement.

Souvenez-vous, après avoir pris votre **modèles d’attribution** et **intervalles de recherche en amont** sélectionné, vous pouvez continuer à manipuler vos données en les filtrant à l’aide d’un  **segment,** ou tout autre composant que vous souhaitez à ce stade.  De plus, une fois le panneau rendu, vous disposez de toutes les fonctionnalités d’un espace de travail classique.

## **Finalement la mettre en pratique**

Maintenant que vous avez les concepts, imaginez que vous exécutez une campagne marketing et que vous essayez de déterminer quel canal est la *le plus efficace* pour générer des conversions. Avec l’aide de la fonction **panneau d’attribution**, vous pouvez non seulement voir la variable **Dernière touche**, mais également la variable **Première touche**, **même touche**, etc. **model** vous choisissez de déterminer laquelle **channels** sont les variables *le plus efficace* en conduisant votre *conversions*. Ces informations peuvent ensuite être utilisées pour *optimize* vos campagnes et améliorez les performances globales simplement en revenant en arrière avec la fonction **intervalle de recherche en amont** de votre choix !

Maintenant que vous avez vu ce qu’il peut faire, ne soyez pas dupé ou intimidé par les fonctionnalités apparemment complexes du panneau d’attribution.  **Rendez-vous compte**.  *Embrasser* c&#39;est le cas.  Comprenez-le*.* MAIS LA PLUPART - *Utilisez-le à votre avantage.* Le **panneau d’attribution** et **intervalle de recherche en amont** sont les clés d’une meilleure compréhension de vos clients et de leur parcours avec votre marque.

Maintenant, nous pouvons voyager &quot;[Retour dans le temps](https://youtu.be/gVryJmZNFdU)&quot; en toute confiance et en utilisant la puissance de notre machine à remonter le temps fiable (c&#39;est-à-dire, ***Adobe Analytics***) pour prendre des décisions basées sur les données.
