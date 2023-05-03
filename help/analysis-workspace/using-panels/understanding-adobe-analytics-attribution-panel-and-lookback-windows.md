---
title: Présentation du panneau Attribution d’Adobe Analytics et des fenêtres de recherche en amont
description: Découvrez comment utiliser le panneau d’attribution et la fenêtre rétroactive pour comprendre le comportement des clients et personnaliser la manière dont les éléments de dimension obtiennent du crédit pour les événements de succès.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13181
thumbnail: KT-13181.jpeg
source-git-commit: 5d20da6a06c9395f56bccbc97ba1d7fb8bb49ff8
workflow-type: tm+mt
source-wordcount: '1883'
ht-degree: 2%

---


# Présentation du panneau Attribution d’Adobe Analytics et des fenêtres de recherche en amont

Découvrez comment utiliser le panneau d’attribution et la fenêtre rétroactive pour comprendre le comportement des clients et personnaliser la manière dont les éléments de dimension obtiennent du crédit pour les événements de succès.

## Utilisation du panneau Attribution 

![Delorean](assets/delorean.png)

&quot;Super Scott !&quot;

Dès que j&#39;ai pensé au [Panneau d’attribution](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html) et **Intervalle de recherche en amont** Je me suis souvenu de la chanson &quot;Back in Time&quot; de Huey Lewis et the News ; alors bien sûr, on m&#39;a aussi rappelé que notre réponse typique à de nombreux nouveaux outils comme ceux-ci est de simplement repousser le fait d&#39;essayer de l&#39;utiliser, parce qu&#39;ils ont l&#39;air si compliqués.

Je veux dire, regardez toutes ces options, ces interrupteurs, ces panneaux, ces lectures, et ces boutons.  Et sérieusement, parlons de ce condensateur.  Attendez, est-ce que je viens de dire un condensateur de flux ?

OK, je vais admettre que la **Panneau d’attribution** est un outil assez complexe; cependant, notre tâche habituelle en tant qu&#39;analystes, jour après jour, est d&#39;utiliser un outil très complexe pour examiner ce qui s&#39;est passé dans le passé.  Cet outil s&#39;appelle **Adobe Analytics**!

Alors, pourquoi devrions-nous laisser quelque chose comme une petite peur se mettre en travers d&#39;un outil aussi cool et puissant qui nous permet littéralement de regarder en arrière dans le temps chaque jour ?

On parle de tout ça, n&#39;est-ce pas ?  DROITE???!! (Je veux dire, allez, je suis presque sûre qu&#39;il est toujours acceptable et &quot;politiquement correct&quot; de nous appeler geeks ?)

Ah, qui s&#39;en soucie ?  Je peux maintenant entendre l&#39;autoradio de la voiture, les Geeks, Nerds, Goobers, Dweebs, et Techies (oui même les Trekkkies) :

&quot;Alors emmenez-moi, ça ne me dérange pas !  Mais vous feriez mieux de me promettre.. JE REVIENDRAI À TEMPS !&quot;

J&#39;ai votre attention, maintenant, n&#39;est-ce pas ?  Super !


Faisons un peu la différence.  Maintenant que nous sommes tous excités à propos de **voyage**, prenons un peu de recul et déterminons ce que la variable **Panneau d’attribution** est :

![Contrôle de durée](assets/time-control.gif)

Non, non, non, non, non !  Ne nous laissons pas distraire tout de suite.  Peut-être réessayons-nous :

![Fenêtre d’attribution](assets/attribution-window.png)

Dans **Attribution**, il vous suffit d’examiner la manière dont les événements/actions peuvent être causés par un individu, plusieurs individus ou une ou plusieurs choses différentes au fil du temps.

Selon [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/attribution.html), l’attribution permet aux analystes de personnaliser la manière dont les éléments de dimension obtiennent du crédit pour les événements de succès.  En fait, aucun parcours client donné n’est jamais vraiment linéaire et est moins souvent prévisible.  De plus, chaque client procédera à son propre rythme. souvent ils peuvent reculer, bloquer, abandonner ou adopter un autre comportement non linéaire. Ces actions organiques rendent difficile ou pratiquement impossible de connaître l’impact des efforts marketing sur le parcours client. Cela complique également les efforts visant à relier plusieurs canaux de données.

Cela vous semble-t-il familier ?  Pensez-y dans le contexte du parcours de Marty McFly :

![Retour vers l&#39;avenir 1](assets/back-to-the-future1.png)![Retour vers l&#39;avenir 2](assets/back-to-the-future2.png)

Depuis le moment où il a fui le parking du Twin Pines Mall jusqu&#39;au moment où il s&#39;est littéralement jeté hors du DeLorean avant qu&#39;il ne soit oblitéré par une locomotive de 210 tonnes semble loin d&#39;être linéaire, et il n&#39;y a rien que quiconque aurait pu prédire.

Pourtant, grâce à la puissance de la magie du film, nous pouvons suivre le chemin de Marty à travers le temps et comprendre tous ses points de contact, ses étals, ses doubles dos et ses abandons.

## Modèles d’attribution

Dans la vraie vie, nous utilisons le **Panneau d’attribution** pour voir plusieurs choses différentes.  Par exemple, la variable **Modèles d’attribution** montrez-nous comment notre **conversions** sont distribués sur **accès** dans un groupe particulier.

En d&#39;autres termes, si 10 personnes appuient sur un bouton pour passer par une porte, nos Modèles d&#39;Attribution vont nous dire laquelle de ces 10 personnes nous voulons donner le crédit d&#39;avoir appuyé sur ce bouton.  Dans ce contexte, voici quelques exemples de la manière dont les modèles d’attribution peuvent affecter ces 10 personnes :
* **Première touche**: Celui-ci est exactement comme ça a l&#39;air.  Dans ce cas, il accorde 100% de crédit à la première personne qui a traversé la porte.  Pour ce faire, les spécialistes du marketing sont plus susceptibles de l’utiliser pour des tactiques telles que Social ou Affichage, mais il s’agit souvent d’une excellente tactique pour l’efficacité des recommandations de produits sur site.
* **Dernière touche**: Et exactement comme ça a l&#39;air.   Ce modèle accorde 100% de crédit à la dernière personne qui a marché à la porte.  Ce modèle est souvent utilisé pour analyser des éléments comme la recherche et les campagnes de cycle marketing à court terme.
* **Linéaire**: Cela accorde le même crédit à chaque personne qui a franchi la porte.  C&#39;est vrai - vous avez un DeLorean, et vous avez un DeLorean, et vous avez un DeLorean.  TOUT LE MONDE OBTIENT UN DÉLORÉEN!!!
* **En forme de U**: Celui-ci donne 40% du crédit à la première dans la porte, diffuse 20% du crédit à toutes les personnes entre et donne 40% à la dernière jusqu&#39;au dernier.  Imaginez une situation dans laquelle vous souhaitez reconnaître la majorité des conversions à la fois sur le front-end et le back-end, mais aussi où vous souhaitez arroser une petite partie du crédit pour certaines des interactions de contribution entre les deux.
* **Décroissance temporelle**: Je manquerais à mon devoir si je ne partagais pas celui-ci avec vous avant de vous envoyer vers la documentation officielle pour examiner les modèles restants.  Comme le plutonium de Doc Brown, ce modèle a littéralement une demi-vie qui se décompose de manière exponentielle !  Dans ce cas, le paramètre par défaut de la demi-vie de ce modèle est de 7 jours.  Son fonctionnement consiste à appliquer un poids à chaque canal marketing, en fonction du temps qui s’écoule après le point de contact initial et du moment où le client effectue la conversion.

Pour plus d’informations à ce sujet et le reste **Modèles d’attribution**, [cliquez ici](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=fr).

Pour rendre cela encore plus intéressant, parlons du **Windows de recherche en amont**.

Ouais, on y va - on y retourne dans le temps!!  Parce que c&#39;est là que commence le plaisir !

Définition des Adobes **Windows de recherche en amont** comme &quot;durée pendant laquelle une conversion doit revenir en arrière pour inclure des points de contact. Les modèles d’attribution qui accordent plus de crédit aux premières interactions voient des différences plus importantes lors de l’affichage de différents intervalles de recherche en amont.&quot;

* **Intervalle de recherche en amont des visites**: Recherche en amont jusqu’au début d’une visite lorsqu’une conversion s’est produite
* **Intervalle de recherche en amont des visiteurs**: Recherche toutes les visites en amont jusqu’au 1er du mois de la période en cours.
* **Intervalle de recherche en amont personnalisé**: Permet d’étendre la fenêtre d’attribution au-delà de la période de création de rapports, jusqu’à un maximum de **90 jours**.

Si vous avez vu TOUS les films de Retour au Futur, vous savez que Marty McFly est revenu dans le temps plus d&#39;une fois, et vous savez aussi qu&#39;il est retourné plus d&#39;une fois en 1955.  Si nous dépendons de l’acquisition de &quot;Gray&#39;s Sports Almanac&quot; comme événement de conversion, tenez compte des points suivants :

![Sports almanach](assets/sports-almanac.png)

1. Un peu avant **1 h 30** on **26 octobre 1985**, Marty McFly revient en arrière pour **5 novembre 1955**, où il court pour la première fois sur un pin dans un DeLorean itinérant.  Au cours de la semaine et demie qui a suivi, il interagit avec plusieurs personnes, dont ses parents, ce qui a finalement affecté l&#39;avenir en obligeant son père à se dresser contre une brute appelée Biff, afin que son père puisse réaliser son propre potentiel pour devenir un auteur de science-fiction qui a réussi.
1. Plus tard le même matin le **26 octobre 1985**, le docteur Emmett Brown arrive sur l&#39;allée de Marty McFly pour l&#39;informer, lui et sa petite amie, que quelque chose n&#39;allait pas chez leurs enfants et qu&#39;ils doivent se précipiter vers le futur pour résoudre leurs problèmes.  Au moment de leur départ, Biff est le témoin de leur départ, qui trouve étrange de voir un DeLorean en plein vol.  Plus tard, dans le futur, alors que Biff voit encore un DeLorean volant et plus tard voit &quot;deux versions&quot; de Marty, il commence à rassembler les choses.   Lorsqu&#39;il entend Doc Brown et Marty argumenter sur la façon dont la &quot;machine à remonter le temps&quot; ne doit jamais être utilisée à des fins personnelles et uniquement pour la recherche (parce que Marty avait réfléchi à la possibilité de ramener un almanach sportif dans le passé pour faire des paris personnels), Biff vole la machine à remonter le temps tandis que les deux sont distraits pour livrer l&#39;almanach sportif à lui-même plus jeune dans le passé.
1. Après leur voyage vers l&#39;avenir, Doc Brown et Marty retournent à une **26 octobre 1985** ils ne reconnaissent pas, et ils déduisent que la chronologie a été modifiée par un diabolique Biff.  En réalisant qu&#39;ils doivent réparer ce qui s&#39;est passé, Doc et Marty se décident à retourner à **12 novembre 1955**, la nuit fatidique où tout a été changé par Marty lors de sa première visite **1955**.  Doc et Marty ont finalement sauvé la journée en volant l&#39;almanach sportif que Old Biff avait livré à Young Biff à **1955**, mais pas sans un autre rebondissement, vous avez vraiment besoin de regarder la trilogie complète de films pour vraiment apprécier et comprendre.

Selon le **Modèle d’attribution** et **Intervalle de recherche en amont**, nous pouvons finir avec des scénarios intéressants :

* Utilisation **Première touche** et un **intervalle de recherche en amont des visites**, l&#39;attribution examine la visite de Marty où s&#39;est produite la plus récente &quot;conversion&quot;, c&#39;est-à-dire quand Doc et lui ont réussi à voler l&#39;almanach sportif de Young Biff et à maintenir son aversion pour le fumier.

![Biff 1](assets/biff1.png)![Biff 2](assets/biff2.png)

* Croyez-le ou non, en utilisant **Première touche** et un **intervalle de recherche en amont des visiteurs**, l’attribution favoriserait la conversion gagnante par Biff.
* Application d’un **Intervalle de recherche en amont linéaire** entraînerait un multi-univers dans lequel chaque chronologie existe.  Désolé, ce n&#39;est pas le cas **Marvel** ou **Star Trek**!

Et à ce stade, j&#39;espère que vous commencez à avoir l&#39;idée.

Qu&#39;est-ce que tout cela signifie pour nous en tant qu&#39;analystes ?

Le **Panneau d’attribution** et **Intervalle de recherche en amont** nous donner la possibilité de regarder au-delà des données simples au niveau de la surface et d’approfondir l’analyse du parcours client. En comprenant les points de contact qui ont eu le plus d’impact sur les conversions, nous pouvons prendre des décisions éclairées sur nos stratégies marketing et allouer les ressources plus efficacement.

Souvenez-vous, après avoir pris votre **Modèles d’attribution** et **Windows de recherche en amont** sélectionné, vous avez toujours la possibilité de manipuler davantage vos données en les filtrant avec un segment ou tout autre composant de votre choix.  De plus, une fois le panneau rendu, vous disposez de toutes les fonctionnalités d’une **Workspace**, ce qui signifie que vous êtes officiellement autorisé à conduire 88 km/h !

## Finalement la mettre en pratique

Maintenant que vous avez les concepts, imaginez que vous exécutez une campagne marketing et que vous essayez de déterminer quel canal est le plus efficace pour générer des conversions. Avec l’aide de la fonction **Panneau d’attribution**, vous pouvez voir non seulement le **Dernière touche**, mais également la variable **Première touche**, **Même touche**, ainsi que tout autre modèle de votre choix, afin de déterminer les canaux les plus efficaces pour générer vos conversions. Ces informations peuvent ensuite être utilisées pour optimiser vos campagnes et améliorer les performances globales.

Maintenant que vous avez vu ce qu&#39;il peut faire, ne soyez pas intimidé par les caractéristiques apparemment complexes de la **Panneau d’attribution**.  **Visage** c&#39;est le cas.  **Embrasser** c&#39;est le cas.  **Comprendre** c&#39;est le cas.  Surtout, utilisez-le à votre avantage. Le **Panneau d’attribution** et **Intervalle de recherche en amont** sont les clés d’une meilleure compréhension de vos clients et de leur parcours avec votre marque.

Maintenant, nous pouvons voyager &quot;dans le temps&quot; en toute confiance et utiliser la puissance de notre machine à remonter le temps (c&#39;est-à-dire,  **Adobe Analytics**) pour prendre des décisions fondées sur les données ; et surtout, rappelez-vous, &quot;Où nous allons, nous n&#39;avons pas besoin de routes !&quot; (Juste un condensateur de flux, et un oeil attentif pour l&#39;attribution !)

![Retour vers l&#39;avenir](assets/back-to-the-future3.png)

## Auteur

Ce document a été rédigé par :

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, gestionnaire, Analyses numériques chez Kroger Personal Finance

Adobe Analytics Champion
