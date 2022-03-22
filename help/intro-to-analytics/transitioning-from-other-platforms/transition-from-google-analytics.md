---
title: Guide complet de transition vers Adobe Analytics à partir des Google Analytics
description: L’un des plus grands défis de la transition entre les outils est d’apprendre où trouver des fonctionnalités équivalentes et d’apprendre à les utiliser efficacement. Cette discussion s’inscrit dans un guide plus large destiné à aider les utilisateurs à passer plus facilement à Adobe Analytics.
feature: Third-party Integration
role: User
level: Beginner
doc-type: feature video
thumbnail: 34749.jpg
kt: 9830
exl-id: b2be6081-a1c0-4435-affb-454ed5a74662
source-git-commit: de78868e07b0fa59a7babc092c463bbe4d8e2da7
workflow-type: tm+mt
source-wordcount: '3690'
ht-degree: 1%

---

# Guide complet de transition vers Adobe Analytics à partir des Google Analytics

## 1. Introduction

L’un des plus grands défis de la transition entre les outils est d’apprendre où trouver des fonctionnalités équivalentes et d’apprendre à les utiliser efficacement. Cette discussion fait partie d’un guide plus large destiné à aider les utilisateurs à passer plus facilement à Adobe Analytics (en tant que nouvel utilisateur ou en tant que Google Analytics). une comparaison approfondie de la disponibilité générale; comme outil comparatif le plus probable que la plupart des utilisateurs connaîtront; est fourni pour aider les utilisateurs à mettre en relation les connaissances existantes avec le nouvel ensemble d’outils. Bien qu&#39;il n&#39;y ait pas de substitut à la pratique, cela vous aidera à vous lancer et, je l&#39;espère, à réduire les frustrations que vous pouvez rencontrer pendant cette période (ou même comme une actualisation après avoir commencé à vous mettre dans le mouvement des choses).

Nous devrions aussi avoir une rapide comparaison terminologique :

| **Description** | **Adobe Analytics** | **Google Analytics ** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| Une mesure d’événement qui représente une page (ou un écran sur une application) a été affichée. | Page vue | Pageview. |
| Mesure qui représente un groupe d’interactions sur votre site web ou votre application qui ont lieu au cours de la même période. | Visite | Session |
| Mesure qui définit un appareil identifié (en fonction de plusieurs critères, y compris des cookies et d’autres modèles de comportement, pour regrouper les informations sur l’utilisateur). | Visiteur unique | Utilisateur |

## 2. Les interfaces

Une des choses que je vois le plus souvent quand les gens comparent Adobe Analytics et les Google Analytics c&#39;est que l&#39;Adobe a beaucoup de choses en cours - c&#39;est impressionnant pour les gens. C&#39;est vrai, mais c&#39;est aussi vrai. le croire ou non; une force, pas une faiblesse. Adobe offre un large éventail d’outils et de flexibilité dans votre visualisation de données, ce qui vous permet d’obtenir plus de liberté pour créer ce dont vous avez besoin.

Commençons par examiner les rapports &quot;sur site&quot;.

### 2.1. Création de rapports sur site

#### 2.1.1. Écran d’accueil

Adobe Analytics et les Google Analytics permettent de personnaliser la première vue qu’un utilisateur voit lorsqu’il se connecte.

##### 2.1.1.1. Espace de travail / Écran d’accueil du jeu personnalisé (Adobe Analytics)

Adobe Analytics ne présuppose pas la création d’un rapport prédéfini que tous les utilisateurs pourront afficher lors de leur connexion. La page d’accueil par défaut permet à l’utilisateur d’accéder à l’écran d’entrée de l’espace de travail, qui affiche à chaque utilisateur tous les rapports de l’espace de travail qu’il a créés ou qu’il a partagés avec lui. En outre, chaque utilisateur peut définir l’un de ces rapports comme écran d’accueil s’il le souhaite.

![image1](assets/ga-to-aa_1.png)

Vous trouverez plus de détails ci-dessous concernant Workspace plus loin dans ce guide. Voir Section 2.1.2.1

>[!TIP]
>
>Créez/partagez des rapports standard pour votre organisation afin qu’ils disposent d’un point de départ pour afficher les informations sans avoir à créer immédiatement leurs propres rapports.



##### 2.1.1.2. Informations sur l’écran d’accueil (Google Analytics)

* L’écran d’accueil de Google Analytics contient des visualisations préconfigurées.  Elles couvrent des éléments tels que :
* Utilisateurs, sessions, taux de rebond et durée de session au cours des 7 derniers jours
* Utilisateurs par heure de la journée au cours des 30 derniers jours
* Utilisateurs actuels en ce moment et principales pages Principales
* Canal de trafic, source/moyenne et références au cours des 7 derniers jours
* Sessions par pays au cours des 7 derniers jours
* Pages principales des 7 derniers jours
* Tendance des principaux utilisateurs au cours des 30 derniers jours
* et plus encore 

Dans GA4, les utilisateurs disposent d’autres options pour personnaliser et ajouter leurs propres rapports à l’écran d’accueil.

![image2](assets/ga-to-aa_2.png)

C&#39;est probablement la chose qui vous manquera le plus en venant à l&#39;Adobe. ils ne disposent pas d’un écran d’accueil préconfiguré pour vous, mais vous pouvez facilement configurer un espace de travail personnalisé pour répliquer ce dont vous avez besoin dans la partie supérieure et, si vous le souhaitez, le définir comme écran d’entrée. Pour plus d’informations à ce sujet, voir la section 2.1.2.1 Adobe Workspace).

#### 2.1.2. Reports Builder sur site

Outre les rapports simples fournis par les outils d’analyse, chaque outil fournit également des outils plus puissants pour créer vos propres rapports personnalisés.

##### 2.1.2.1. Espace de travail Adobe Analytics

Il s’agit de l’élément phare d’Adobe Analytics. Depuis son introduction en 2017, cette application est devenue le lieu de prédilection pour l’analyse d’Analytics. C’est la Principale raison pour laquelle la section Rapports sera bientôt supprimée.

Cet outil vous permet de créer des rapports avec une liberté presque totale.

Le rapport peut être divisé en panneaux et ces panneaux peuvent contenir un nombre illimité de visualisations. Les panneaux peuvent être définis sur des informations communes, telles que la période et les filtres de segments communs.

Les panneaux et les visualisations qu’ils contiennent peuvent être redimensionnés et déplacés pour afficher les éléments côte à côte ou empilés. Si vous souhaitez comparer deux suites de données différentes côte à côte, vous pouvez créer des panneaux qui divisent 50/50 le milieu affichant les deux sites côte à côte pour faciliter la comparaison.

Les utilisateurs ont accès à une multitude de visualisations :

* Tableau à structure libre
* Tableau de cohortes
* Abandon
* Flux
* Graphiques
   * Zone (empilée et non empilée)
   * Ligne
   * Nuage de points
   * Barre (empilée et non empilée)
   * Puce
   * Anneau
   * Histogramme
   * Barre horizontale (empilée et non empilée)
* Carte
* Blocs récapitulatifs
   * Résumé des changements
   * Texte récapitulatif
   * Texte (champ de texte libre pour saisir des informations supplémentaires pour donner un contexte)
* Venn

Chaque panneau et visualisation peut être intitulé et faire l’objet d’une description afin de donner un contexte à ce que les informations présentent.
Dans Adobe, les segments (essentiellement les filtres pour les données) s’appliquent rétroactivement. Ils peuvent être extraits en colonnes des tableaux à structure libre pour comparer les données côte à côte. Par exemple, si un utilisateur souhaite comparer deux catégories différentes de trafic sur son site ; ils peuvent créer un segment pour la &quot;catégorie A&quot; et un autre pour la &quot;catégorie B&quot;.

![image3](assets/ga-to-aa_3.png)

Les tableaux à structure libre permettent plusieurs colonnes et une segmentation, selon les besoins, afin de visualiser les données comme vous le souhaitez.

Dans la section ci-dessus, ne souhaitez-vous pas afficher une ventilation par date ? Il vous suffit de faire glisser une autre dimension ou un autre segment pour afficher les données d’une manière différente... comme par exemple utiliser des segments pour le type de périphérique, puis d’ajouter une ventilation par système d’exploitation pour vos utilisateurs de périphériques mobiles/tablettes :

![image3](assets/ga-to-aa_4.png)

Workspace permet à votre créativité de voler, vous n’êtes pas limité aux ventilations &quot;standard&quot;. Vous pouvez créer les visualisations dont vous avez besoin pour approfondir les comparaisons à exécuter.

>[!TIP]
>
>N&#39;ayez pas peur de jouer et d&#39;explorer, il y a tellement de façons de sortir de la boîte ici, voir ce que vous pouvez faire ! Mais aussi, assurez-vous d&#39;essayer de valider que ce que vous avez construit montre vraiment ce que vous pensez être. L&#39;expérience ici aidera !

Vous pouvez même créer des mesures calculées à la volée ou des segments qui ne résident que dans le rapport (ce qui évite d’inonder le référentiel de segments et de calculs, mais également vous assurer que vous pouvez créer des éléments ciblés nécessaires à des rapports spécifiques sans confondre votre organisation avec des éléments qui ne sont pas très utilisables dans d’autres contextes.

Cette discussion n’est qu’une introduction à cet outil. Il y aura d’autres guides plus complets pour vous aider à commencer. Une fois que vous l’aurez fait, vous pourrez créer des rapports complets, tels que :

![image3](assets/ga-to-aa_5.png)

Notez également que les espaces de travail n’enregistrent pas automatiquement. Il est donc plus facile d’effectuer un rapport ad hoc unique sans boucher votre référentiel de rapports.

L’autre fonctionnalité puissante des espaces de travail est la possibilité d’appliquer des modificateurs interactifs à vos rapports sous la forme de listes déroulantes. Bien que ces menus déroulants ne fonctionnent pas sur les fichiers CSV ou PDF exportés de vos rapports, ils vous permettent, dans le rapport en direct, de mettre à jour toutes les visualisations d’un panneau afin d’afficher le même rapport sous différentes conditions. Plusieurs listes déroulantes peuvent être utilisées. Tant que les options ne s’excluent pas mutuellement, les éléments sélectionnés s’empilent pour permettre une présentation claire des informations.

>[!IMPORTANT]
>
>Pour en savoir plus sur l’utilisation des listes déroulantes et des ventilations à structure libre, voir <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680>

##### 2.1.2.2. Google Analytics : Tableaux de bord, rapports personnalisés et rapports enregistrés

Google dispose de quelques outils pour créer des rapports dans l’interface, mais ils suivent toujours l’affichage et les limites de la section des rapports.

Maintenant, pour ceux qui connaissent le Google Analytics en lisant ceci, vous pourriez dire, &quot;Bon, attendez une seconde, et Google Data Studio, n&#39;est-ce pas un meilleur équivalent à l&#39;espace de travail d&#39;Adobe ?&quot; et vous auriez raison, mais comme Data Studio ne fait pas techniquement partie de l’outil Analytics et permet de se connecter à différentes sources de données, cet outil est traité plus loin dans la section &quot;Accès aux rapports étendu&quot; de cette discussion (et en particulier dans la section 2.2.3).

Les tableaux de bord Google et les rapports personnalisés vous permettent d’extraire plusieurs visualisations en un seul rapport. Cependant, contrairement à Workspace, vous êtes toujours verrouillé dans des corrélations simples et quelles données peuvent être placées dans quelles colonnes.

Dans les rapports personnalisés, l’un des plus grands défis réside dans le fait que, lorsque vous créez un filtre, il s’applique à tous les onglets du rapport... Il n’est pas possible de comparer deux filtres différents au sein d’un même rapport.

Pour les comparaisons de surface, cela fonctionne. Elles sont toutes similaires aux tableaux de bord, aux rapports personnalisés et aux signets hérités de l’Adobe. Outils de base fournis pour répondre à vos besoins, qui se trouvent dans la suite de rapports.

#### 2.1.3. Rapports

Google et Adobe contiennent tous deux des rapports accessibles, des tableaux par défaut et des graphiques de chronologie de base basés sur une dimension.

##### 2.1.3.1. Rapports Adobe Analytics

Adobe Analytics dispose également d’une section Rapports , bien que celle-ci soit en grande partie supprimée progressivement au profit de leur Analysis Workspace (et en fait, la fin de vie de cette interface a été annoncée depuis Workspace). [Section 2.1.2.1] est un outil beaucoup plus puissant), où la plupart de ces tables peuvent être créées et modifiées plus facilement. Les sections de l’Adobe sont beaucoup plus fragmentées, ce qui peut être décourageant :

![image3](assets/ga-to-aa_6.png)

Comme la plupart des éléments ci-dessus sont accessibles via les espaces de travail, je vais vous donner un bref aperçu de ces sections et de leur relation avec les Google Analytics, et mettre en évidence ici les rapports qui restent pertinents.

Les mesures du site sont ce à quoi vous vous attendez ; elles couvrent les mesures standard (pages vues, visiteurs uniques, visites, ainsi que les événements personnalisés que vous avez configurés). Ceci est similaire à la disponibilité générale du rapport de comportement, mais inclut également certaines de ce que vous trouverez dans Audience (puisque Adobe ne divise pas les types de mesures).

Vous y trouverez également des rapports &quot;Robots&quot;. Le trafic provenant des robots est exclu de tous vos rapports standard. Toutefois, deux rapports vous permettent d’avoir des informations sur ce qui se passe et sur les robots qui se rendent sur votre site. Cela est particulièrement utile si vous configurez des règles de robots personnalisées pour exclure les robots spammeurs connus qui visitent fréquemment votre site. Vous pouvez avoir un aperçu de ce que ces robots font sans que vos principaux rapports ne soient inondés, mais que le trafic en question. Les rapports de robots sont actuellement indisponibles via Workspace (mais de nouvelles fonctionnalités de création de rapports vont bientôt permettre aux utilisateurs d’y obtenir ces informations).

Contenu du site est un groupe de dimensions standard Adobe : Nom de page, Sections du site (canaux), Hiérarchies (moyen de créer des rapports d’analyse personnalisés de l’organisation dans votre site web), Serveurs (cela s’avère particulièrement utile si votre site comporte plusieurs sous-domaines, ou si vous balisez plusieurs sites ensemble dans une seule suite de suivi), etc. Toutes ces options sont disponibles dans Workspace.

Mobile est un groupe de données spécifiques aux périphériques mobiles, telles que les appareils, les types d’appareils, etc. Toutes ces options sont disponibles dans Workspace.

Les chemins sont un autre de ces éléments &quot;pas tout à fait disponibles dans Workspace&quot;... tandis que Workspace comporte un diagramme Flux, vous ne pouvez afficher que les flux d’entrée et de sortie pour une seule page/valeur... tandis que les chemins vous permettent de voir les chemins les plus courants utilisés dans votre site web. Par défaut, Pages est le premier rapport de chemin d’accès configuré pour vous, mais vous pouvez l’activer pour les props personnalisées (par exemple, si vous deviez effectuer le suivi d’une valeur &quot;Type de page&quot;, vous pouvez examiner le cheminement dans les types de page. L&#39;autre chose que j&#39;aime personnellement à propos des Chemins est la façon simple dont les informations sont présentées... Le diagramme de flux dans l&#39;espace de travail (en fonction de ce que vous essayez de regarder) peut devenir accablant. Je vous recommande d&#39;essayer les deux... ils ont tous un usage et une valeur en fonction de ce que vous essayez de réaliser. N’importe quelle dimension peut être utilisée dans les flux, tandis que le cheminement doit être configuré sur une prop dans le panneau d’administration.

Les rapports Sources de trafic, Campagnes et Canaux marketing sont tous similaires au rapport Acquisition de Google. Les sources de trafic se concentrent sur les référents réels, les campagnes se concentrent sur vos codes de campagne et les canaux marketing se concentrent également sur les codes de campagne, mais appliquent également une logique supplémentaire, déterminée par vous, sur la manière de traiter les informations. Je trouve que cet Adobe offre beaucoup plus de liberté sur la façon de configurer vos règles, Google fait beaucoup de choses pour vous, et ça va donc être un peu un changement dans la façon de penser. Il est également à noter que, par défaut, l’attribution Google sur les codes de campagne est de 6 mois, le Adobe est défini par défaut sur 1 semaine. Cela peut être modifié dans vos paramètres d’administration, mais dans Workspace, vous pouvez appliquer une attribution personnalisée en plus de n’importe quelle dimension, ce qui vous offre une flexibilité &quot;à la volée&quot; bien plus grande.

Les rapports Rétention des visiteurs et Profil du visiteur sont similaires aux rapports Audience dans les Google Analytics. La rétention est davantage axée sur la fréquence des retours, tandis que le profil du visiteur est davantage axé sur la géographie et la technologie des utilisateurs.

Les rapports Conversion personnalisée et Trafic personnalisé sont tous deux des rapports de dimension personnalisés. Les conversions sont vos eVars (dans lesquelles vous pouvez définir une expiration personnalisée pour la valeur - c’est-à-dire l’accès, la visite, le mois, l’année, etc.). Cette valeur restera pour cet utilisateur pendant la période spécifiée, sauf si elle a été remplacée). Les variables de trafic sont vos props, mais vous pouvez également les configurer pour les rapports de cheminement ou sous la forme d’éléments de liste (qui divisent plusieurs valeurs en fonction d’un délimiteur de votre choix).

Le média est destiné aux fichiers vidéo ou audio dans lesquels vous avez configuré un suivi multimédia spécial.

Les rapports personnalisés sont une section dans laquelle un utilisateur peut personnaliser les colonnes et les ventilations qu’il a créées dans l’interface des rapports et les enregistrer en tant que rapport personnalisé. Cependant, comme nous l’avons mentionné ci-dessus, Workspace permet des ventilations et des corrélations beaucoup plus puissantes, tout ce qui est personnalisé doit simplement y être fait. C’était une bonne solution avant l’existence de Workspace.

La section Signets est similaire aux rapports personnalisés, où les rapports fréquemment utilisés peuvent être marqués dans l’interface des rapports afin de faciliter leur recherche.

Le tableau de bord est un produit hérité qui permet aux utilisateurs de combiner des mini-rapports de données en une seule visualisation. Toutefois, la fonctionnalité de Workspace (section 2.1.2.1) est tellement plus facile à utiliser que cela n’existe qu’en tant que point d’accès aux rapports hérités qui doivent être recréés avant l’expiration de cette fonctionnalité.

Les cibles sont une zone de rapports spéciale qui permet aux utilisateurs de créer un rapport basé sur une cible pendant une certaine période afin que les équipes puissent surveiller des éléments comme les campagnes et voir s’ils étaient sur la bonne voie pour atteindre leurs cibles de trafic.

Tous les rapports disponibles ici sont autorisés pour plusieurs colonnes de mesures et ventilations de dimensions. mais la simplicité des visualisations et une partie de la logique derrière les éléments qui pourraient être corrélés peuvent parfois être frustrantes.

##### 2.1.3.2. Rapports des Google Analytics

Les Google Analytics divisent ces rapports en sections suivantes : Temps réel, audience, acquisition, comportement et conversations (en GA3) et dans le cycle de vie (avec les sous-sections : Acquisition, engagement, monétisation, conservation) et Utilisateur (avec les sous-sections : Données démographiques et technologie).

![image3](assets/ga-to-aa_7.png)

Vous pouvez apporter des ajustements mineurs à ces visualisations, ajouter une ventilation de dimension secondaire, modifier la visualisation, créer un filtre sur les données, etc. Vous pouvez enregistrer vos personnalisations en tant que rapport enregistré.

Vous obtenez ainsi des informations rapides et faciles sur vos données. Cependant, vous ne pouvez pas comparer des éléments tels que Utilisateurs aux pages vues pour une page dans le même tableau, et vous ne pouvez pas ajouter plusieurs dimensions supplémentaires pour afficher des données supplémentaires.

Ils sont bons pour des données analytiques rapides, mais si vous devez vraiment creuser profondément, ils souffrent des limitations.

### 2.2. Accès aux rapports étendu

Outre la création de rapports sur site, la plupart des outils offrent des fonctionnalités étendues qui vous permettent de passer votre analyse en dehors des outils et de créer quelque chose d’un peu plus personnalisé.

#### 2.2.1. Report Builder Adobe Analytics (extension Microsoft Excel)

Workspace est un excellent outil, mais il est parfois nécessaire d’intégrer vos données dans une feuille de calcul personnalisée, éventuellement pour pouvoir assembler plusieurs sources de données. C&#39;est là que le Report Builder entre en jeu.

Report Builder est un plug-in pour Microsoft Excel qui vous permet de créer des connexions à vos données Adobe Analytics afin d’extraire des données tabulaires que vous pouvez manipuler dans Excel. En règle générale, pour utiliser cette fonctionnalité efficacement, vous devez extraire les données dans certains onglets de données brutes, puis utiliser les références de cellule Excel pour extraire les données de ces onglets dans un seul rapport consolidé, puis créer des graphiques et des visualisations.

>[!NOTE]
>
>Report Builder dispose d’une autorisation spéciale qui doit être appliquée à vos utilisateurs pour accéder à ce module externe. Cela ne doit probablement être accordé qu’aux utilisateurs qui ont appris à utiliser l’outil correctement.

#### 2.2.2. Connexion à l’API Adobe Analytics

Si vous avez besoin que votre Adobe Analytics soit digéré par autre chose qu’excel, mais que vous souhaitez toujours bénéficier des avantages des données traitées (y compris les exclusions de règles de robots), vous pouvez utiliser l’API de l’Adobe pour extraire directement les données, puis les traiter via un script ou les ajouter à une base de données en vue de les utiliser avec un autre système.

Notez que l’API extrait toujours les données de corrélation en appliquant les ventilations et les segments comme indiqué dans la requête de tirage.

L’espace de travail d’Adobe (section 2.1.2.1) utilise en fait l’API pour créer tous les rapports. Si vous activez le mode de débogage dans Workspace, les appels d’API exacts utilisés sont affichés. Il s’agit d’une méthode rapide pour créer vos appels d’API à l’aide de Workspace pour créer et valider les données que vous souhaitez extraire, puis utiliser ces appels d’API pour extraire les données vers votre propre traitement.


#### 2.2.3. Google Analytics Data Studio

Si vous avez déjà lu, vous savez déjà d’en haut que j’ai mentionné Data Studio comme étant un équivalent de l’espace de travail de l’Adobe. Data Studio vous permet d’extraire des données Google Analytics, mais aussi des données provenant d’autres sources. C’est très pratique si vous souhaitez consolider vos données d’analyse avec d’autres données collectées ; mais en ce qui concerne le Google Analytics, j&#39;ai trouvé le même type de limitations de visualisation que celles qui sont présentes en Google Analytics. La façon dont les lignes et les colonnes sont formées reste très limitée dans ce qui peut être fait.

C&#39;est toujours un outil puissant, et je ne dissuaderais pas les gens de l&#39;utiliser de quelque manière que ce soit, mais mon expérience personnelle est qu&#39;ayant utilisé Workspace pendant si longtemps, je trouve personnellement le comportement rigide assez limité.


#### 2.2.4. Extension de feuille de calcul Google

Pour mon propre usage, lorsque je dois extraire des données de manière prolongée des Google Analytics, mon outil de choix personnel est l’extension de feuille de calcul Google. Bien sûr, je dois établir plusieurs connexions avec mes tableaux GA, mais comme le Report Builder de l’Adobe, je peux référencer les cellules des données brutes et créer les rapports dont j’ai besoin, puis les visualiser à l’aide des fonctionnalités de représentation de la feuille de calcul Google.


## 3. Exports de données brutes

Pour cette période, vous avez vraiment besoin de données brutes. Adobe et Google vous offrent la possibilité d’extraire des informations de cette manière.

### 3.1. Flux de données d’Adobe

Dans la section 2.2.2, j’ai mentionné que l’API Adobe Analytics provient des &quot;données traitées&quot;. Le flux de données brutes continue à extraire les données traitées par les &quot;règles de traitement&quot; configurées dans le panneau d’administration (assurez-vous que vos données brutes sont retardées pour vous assurer que toutes ces règles sont terminées au moment où le flux de données brutes est extrait), mais ces données brutes incluront toutes les données qui sont exclues partout ailleurs.

Cela signifie que toutes vos exclusions de robots, vos données internes filtrées par IP, etc. seront incluses dans les flux de données brutes. Il existe des indicateurs pour identifier ces données. Ainsi, si vous créez un lac de données, votre équipe d’ingénieurs peut créer une logique pour traiter ces données en conséquence.

Les flux de données brutes peuvent être personnalisés pour envoyer toutes les colonnes de données ou uniquement des colonnes spécifiques si vous avez besoin d’un flux plus ciblé.

Les flux peuvent être envoyés directement vers FTP, SFTP, S3, etc.


### 3.2. Google Big Query

Malheureusement, il s’agit d’un outil Google que je n’ai jamais utilisé, mais qui, en théorie, doit être similaire au flux de données d’Adobe, ce qui permet à votre équipe d’ingénieurs d’accéder aux données brutes de votre compte de Google Analytics.

Cependant, je crois qu&#39;au lieu d&#39;un vidage complet de données brutes, cela permet à vos ingénieurs d&#39;accéder aux données via des requêtes SQL, afin qu&#39;ils puissent extraire soit des données brutes ciblées, soit s&#39;ils le souhaitent, ils peuvent extraire toutes les colonnes de données brutes à ingérer dans un lac de données.

## 4. Conclusion

Comme n’importe quel système, il est nécessaire de s’y entraîner, mais nous espérons que ce guide vous aidera à démarrer, ou vous donnera des conseils pour améliorer votre utilisation d’Adobe Analytics si vous n’avez que gratté la surface.

Cependant, je vous recommande vivement d’utiliser Adobe Analytics et les Google Analytics dans votre stratégie de mise en oeuvre (même si les Google Analytics ne sont que la version gratuite). Vous pouvez ainsi disposer d’un système de sauvegarde pour vous assurer que vous disposez de données, car aucun système n’est infaillible.

De nombreuses ressources sont disponibles au-delà de ce guide pour vous aider à améliorer votre stratégie :

* [Adobe Experience League](https://experienceleague.adobe.com/?lang=fr#home) - Contient des tutoriels, des vidéos, de la documentation et des forums de la communauté.
* [Adobe de groupes d’utilisateurs](https://analytics-augs.adobe.com/) - Un hub d’événements gérés par la communauté pour aider les utilisateurs à se connecter les uns aux autres et améliorer leurs mises en oeuvre. Ces événements étant basés sur un fuseau horaire spécifique, il est préférable de vérifier également quelles autres régions sont exécutées.
* [Canal YouTube des groupes d’utilisateurs Adobe Analytics](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA) - Impossible de créer une session de groupe d’utilisateurs Adobe Analytics ? Regardez les précédentes sessions de groupes d’utilisateurs à travers le monde pour en savoir plus sur l’utilisation de l’outil par vos pairs.
* [Mesurer le canal du Slack de conversation](https://www.measure.chat/) - Connectez-vous avec les utilisateurs d’Adobe Analytics à travers le monde et partagez les leçons du secteur, posez des questions à vos pairs et rejoignez des groupes d’intérêt axés sur les mesures.
* et plus encore !

## Auteur

Ce document a été rédigé par :

![Jennifer Dungan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dungan, responsable de l’optimisation chez Torstar

Champion Adobe Analytics

