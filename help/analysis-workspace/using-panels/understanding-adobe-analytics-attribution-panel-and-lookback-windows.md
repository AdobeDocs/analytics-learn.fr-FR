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
exl-id: 1da9334b-0edb-4237-b7ca-57640865208c
source-git-commit: f1bb981a83eb698f4185a22c367346a9ddd0c755
workflow-type: tm+mt
source-wordcount: '1664'
ht-degree: 1%

---

# Présentation du panneau d’attribution Adobe Analytics et des intervalles de recherche en amont

Quand j&#39;ai pensé pour la première fois au [panneau d&#39;attribution](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=en) et à l&#39;**intervalle de recherche en amont**, je me suis immédiatement souvenu du concept de &#39;*voyage horaire&#39;* ; puis, bien sûr, on m&#39;a aussi rappelé notre réponse habituelle à de nombreux nouveaux outils comme ceux-ci est de simplement reporter l&#39;utilisation, parce qu&#39;ils ont l&#39;air si compliqués.

Je veux dire, honnêtement, regardez toutes ces options, ces interrupteurs, ces panneaux, ces lectures, et ces boutons.  Et sérieusement, parlons de ces lumières clignotantes compliquées, des tuyaux, des jauges.... WAIT!!  Ce n&#39;est pas le moment de se laisser distraire en parlant de machines à remonter le temps, nous n&#39;avons tout simplement pas le temps... ou est-ce que nous en avons ?

Je reconnais que le **panneau d’attribution** est un outil assez complexe ; cependant, notre tâche typique, en tant qu’analystes, jour après jour, consiste à utiliser un autre de nos outils favoris et très complexes pour également examiner ce qui s’est passé dans le passé. Cet outil s’appelle ***Adobe Analytics***!  Donc oui, pour répondre à notre question très pertinente, je crois que ces deux choses disent que nous avons beaucoup de temps.

Par conséquent, pourquoi devrions-nous laisser quelque chose comme une petite peur se mettre en travers de ces outils incroyables, sophistiqués et puissants comme ceux-ci qui nous permettent littéralement de regarder *vers l&#39;arrière* dans le temps, chaque jour ?

Après tout - c&#39;est le TIME VOYAGE, les gars!!  Nous parlons de ce genre de choses.  Right???!!

Alors, qu&#39;attendons-nous - une voiture en métal brillant, une boîte de police, ou une cabine téléphonique vintage utilisant le câblage d&#39;un vieux parapluie comme antenne pour apparaître sur le pas de notre porte ?

Non !  Nous avons quelque chose d&#39;encore mieux, alors raccrochons-nous !

Eh bien.. vous avez l&#39;idée.


Maintenant que nous sommes tous excités par les voyages dans le temps, prenons un souffle profond, reculez un peu, déterminons ce qu&#39;est le **panneau d&#39;attribution** *vraiment*, et ventilez les choses un petit peu :

![Attribution](assets/attribution.png)

*Figure 1 - Les nombres affichés sont alignés avec le texte plus bas sous*

Dans **attribution**, considérez simplement la manière dont les événements/actions peuvent être causés par un individu, plusieurs individus, ou l’un des nombreux événements différents au fil du temps.

Selon [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=en), *attribution* permet aux analystes de personnaliser la manière dont les éléments *Dimension* reçoivent du crédit pour les *événements de succès*.


>[!WARNING]
>
>Les **modèles d’attribution** sont si souvent associés aux **canaux marketing** que j’ai volontairement *❷ CANAL dans l’image ci-dessus pour illustrer qu’il est possible d’effectuer une analyse d’**attribution**&#x200B;par rapport à la plupart des autres&#x200B;*** dimensions &#x200B;***.*


En fait, rarement un parcours client donné est vraiment linéaire et encore moins prévisible.  De plus, chaque client procédera à son propre rythme ; il peut souvent doubler, bloquer, abandonner ou adopter un autre comportement non linéaire. Ces actions organiques rendent difficile ou pratiquement impossible de connaître l’impact des efforts marketing sur le parcours client. Cela complique également les efforts visant à relier plusieurs canaux de données.

C&#39;est vrai.  Laissez vos analogies de &quot;domino&quot; à la porte et ouvrez vos esprits à des concepts plus proches de l&#39;effet papillon et de la théorie des cordes - mais comme tout le reste, nous devons commencer par quelques principes de base.

## **Modèles d’attribution**

Lorsque nous utilisons le **panneau d’attribution**, nous pouvons commencer à observer plusieurs choses différentes.  Par exemple, les **modèles d’attribution** nous montrent comment nos *conversions* (c’est-à-dire ❶ **mesures de succès**) peuvent être distribuées sur *accès* dans n’importe quel groupe donné.

En d&#39;autres termes, si **10 personnes** appuient sur un **BOUTON GRAND ROUGE** pour passer par une porte, nos **modèles d&#39;attribution** vont nous dire lequel de ces **10 personnes** nous voulons attribuer un &quot;crédit&quot; - ou mieux encore dire, quel *beaucoup* de &quot;crédit&quot; nous voulons leur attribuer - pour ce bouton.

![Bouton](assets/button.png)

En gardant cela à l’esprit, voici quelques exemples de la façon dont les **modèles d’attribution** ❸ peuvent affecter ces **10 personnes** :

- **Première touche** : ce modèle fonctionne exactement comme il semble en accordant **100 % du crédit** à la *première* personne qui a traversé la porte.  Les marketeurs sont plus susceptibles d’utiliser cette approche pour des tactiques telles que ***social media*** ou ***display*** ; toutefois, il s’agit également d’une excellente tactique à utiliser souvent pour l’efficacité des recommandations de produits sur site.
- **Dernière touche** : Cette tactique fonctionne aussi exactement comme elle semble, mais à la place, elle accorde **100 % de crédit** à la DERNIÈRE personne qui a traversé la porte.  Ce modèle est généralement utilisé pour analyser des éléments tels que la ***recherche naturelle (organique)*** et d’autres campagnes de cycle marketing *à court terme*.
- **Linear** : ce modèle distribue un crédit égal à CHAQUE PERSONNE qui a traversé la porte.

  >[!CAUTION]
  >
  >Il est toutefois conseillé de faire attention, car vous avez la possibilité de diffuser vos résultats très rapidement lorsque vous appliquez cette tactique, en tenant compte du temps d’exécution et de l’audience plus grande qu’elle atteint.

- **En forme de U** : cette approche attribue **40%** du crédit à la *première personne* dans la porte, propage **20%** du crédit sur *toutes les personnes entre*, puis donne **40%** au **dernier** par . Ce modèle est le plus souvent utilisé dans les situations où vous avez un **long cycle de conversion/vente** contenant *plusieurs points de contact* en cours de route.  Dans ce cas, votre objectif est principalement de mettre en évidence les tactiques marketing ***first*** et ***last*** qui ont contribué à la conversion des clients.
- **J**-**En forme** et **En forme de J inverse** :
   - Pensez à **En forme de U**, mais à la place, ce modèle attribue **60%** crédit à la *dernière personne* qui passe par la porte, **20%** à la *première*, puis *divise* le reste **20%** 4&rbrace;tous les autres *au milieu.*  **Inverse J** fait exactement le contraire.

     L’objectif ici est de mettre l’accent sur l’élément de contribution, soit au *début*, soit à la *fin* de votre campagne. Cependant, vous souhaitez tout de même attribuer un certain crédit à l’élément de contribution à l’autre bout tout en reconnaissant les &quot;petits&quot; en cours de route.

- **Décroissance temporelle** : Maintenant, je ne serais plus ici si je ne partagais pas celle-ci. Ce modèle a littéralement une demi-vie qui diminue exponentiellement - au fil du temps !  Dans ce cas, le paramètre *default* de la demi-vie de ce modèle est **7 days**.  Son fonctionnement consiste alors à appliquer *weight* à chaque **canal marketing**, *en fonction de la durée* qui s&#39;écoule après le *point de contact initial* et lorsque le client effectue une conversion.

  Les **modèles d’attribution Décroissance temporelle** et **En forme de U** sont généralement utilisés pour mesurer les campagnes à plus long terme, mais comme vous pouvez le voir, ils ont des objectifs légèrement différents, en fonction de la manière dont ils *pèsent* sur la valeur du résultat.

- **Personnalisé** : vous choisissez qui obtiendra le crédit.  C&#39;est votre campagne !

Pour plus d’informations sur ces modèles et d’autres modèles d’attribution, [cliquez ici](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=en)

Pour rendre cela encore plus intéressant, parlons de revenir en arrière !

## **Intervalles de recherche en amont**

Il est maintenant temps de commencer à penser à un autre niveau.  C&#39;est là que nous ajoutons littéralement l&#39;élément voyage dans le temps à notre analyse - et là encore, nous commençons avec les bases.

***Adobe*** définit ❹ **intervalles de recherche en amont** comme &quot;la durée pendant laquelle une conversion doit revenir en arrière pour inclure des points de contact. Les modèles d’attribution qui accordent plus de crédit aux premières interactions voient des différences plus importantes lors de l’affichage de différents intervalles de recherche en amont.&quot;


En d’autres termes, les **intervalles de recherche en amont** déterminent la période pendant laquelle les *conversions* sont prises en compte et fournissent le *contexte* à l’analyse d’attribution. ***Adobe Analytics*** offre trois types de **intervalles de recherche en amont** :

- **Intervalle de recherche en amont des visites :** recherchent en amont le début d’une ***visite*** lorsqu’une conversion s’est produite, fournissant des informations sur les interactions immédiates menant aux conversions.

  Souvenez-vous qu’il s’agit généralement de la **période de recherche arrière la plus courte** à utiliser.
- **Intervalle de recherche en amont des visiteurs :** recherche toutes les ***visites*** jusqu’au premier du mois au cours de la **période** sélectionnée, offrant une vue beaucoup plus large des interactions du client et permettant d’identifier les schémas au fil du temps.
- **Intervalle de recherche en amont personnalisé :** permet d’étendre l’ **intervalle d’attribution** au-delà de la **période** jusqu’à un *maximum* de **90 jours**.  Il offre une *flexibilité* pour capturer les points de contact qui se sont produits *en dehors de* de la **période sélectionnée**, ce qui garantit une analyse complète.

En réglant un **intervalle de recherche en amont** donné, les analystes peuvent alors examiner l’impact d’un ou de plusieurs points de contact au cours de périodes spécifiques et obtenir des informations plus précises sur la manière dont les différentes durées affectent les résultats d’attribution.

## **Rassembler tout**

Qu&#39;est-ce que tout cela signifie pour nous en tant qu&#39;analystes ?

Le **panneau d’attribution** et l’ **intervalle de recherche en amont** nous permettent de regarder au-delà des données ordinaires au niveau de la surface, et d’approfondir nos recherches dans le parcours client. En comprenant les points de contact qui ont eu le plus d’impact sur les *conversions*, nous pouvons prendre des décisions éclairées sur nos stratégies marketing et allouer les ressources plus efficacement.

Souvenez-vous qu’une fois que vos **modèles d’attribution** et **intervalles de recherche en amont** sont sélectionnés, vous pouvez continuer à manipuler vos données en les filtrant avec un ❺ **segment,** ou tout autre composant que vous souhaitez à ce stade.  De plus, une fois le panneau rendu, vous disposez de toutes les fonctionnalités d’un Workspace traditionnel.

## **Finalement la mettre en pratique**

Maintenant que vous avez terminé les concepts, imaginez que vous exécutez une campagne marketing et que vous essayez de déterminer quel canal est le *le plus efficace* pour générer des conversions. Avec l’aide du **panneau d’attribution**, non seulement vous pouvez voir la **dernière touche**, mais aussi la **première touche**, la **même touche** et tout autre **modèle** que vous choisissez pour déterminer les **canaux** les *conversions les plus efficaces&#x200B;**.* Ensuite, ces informations peuvent être utilisées pour *optimiser* vos campagnes et améliorer les performances globales simplement en retournant l’horloge avec l’ &#x200B;** intervalle de recherche en amont** de votre choix !

Maintenant que vous avez vu ce qu’il peut faire, ne soyez pas dupé ou intimidé par les fonctionnalités apparemment complexes du panneau d’attribution.  **Visez-le**.  *Embrace* it.  **Comprendre**.
MAIS LA PLUPART DE TOUS - *Utilisez-le à votre avantage.* Le **panneau d’attribution** et l’ **intervalle de recherche en amont** sont les clés pour déverrouiller une compréhension plus approfondie de vos clients et de leur parcours avec votre marque.

Désormais, nous pouvons voyager &quot;[dans le temps](https://youtu.be/gVryJmZNFdU)&quot; en toute confiance et utiliser la puissance de notre machine à remonter le temps fiable (également appelée ***Adobe Analytics***) pour prendre des décisions basées sur les données.

## Auteur

Ce document a été rédigé par :

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, responsable de l’analyse numérique chez Kroger Personal Finance

Adobe Analytics Champion
