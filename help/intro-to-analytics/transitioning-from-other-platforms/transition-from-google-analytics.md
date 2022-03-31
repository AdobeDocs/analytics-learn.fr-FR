---
title: Guide complet de transition vers Adobe Analytics à partir de Google Analytics
description: L’un des plus grands défis de la transition entre des outils est d’apprendre où trouver des fonctionnalités équivalentes et à les utiliser efficacement. Cette discussion s’inscrit dans un guide plus étendu destiné à aider les utilisateurs à passer plus facilement à Adobe Analytics.
feature: Third-party Integration
role: User
level: Beginner
doc-type: feature video
thumbnail: 34749.jpg
kt: 9830
exl-id: b2be6081-a1c0-4435-affb-454ed5a74662
source-git-commit: de78868e07b0fa59a7babc092c463bbe4d8e2da7
workflow-type: ht
source-wordcount: '3690'
ht-degree: 100%

---

# Guide complet de transition vers Adobe Analytics à partir de Google Analytics

## 1. Introduction

L’un des plus grands défis de la transition entre des outils est d’apprendre où trouver des fonctionnalités équivalentes et à les utiliser efficacement. Cette discussion fait partie d’un guide plus étendu destiné à aider les utilisateurs à passer plus facilement à Adobe Analytics (en tant que nouvel utilisateur ou en tant qu’utilisateur Google Analytics). Une comparaison approfondie avec Google Analytics, qui est l’outil comparatif que la plupart des utilisateurs connaîtront, est fournie pour aider les utilisateurs à mettre en relation les connaissances existantes avec le nouvel ensemble d’outils. Bien que rien ne puisse remplacer la pratique, cela vous aidera à vous lancer et à réduire les frustrations que vous pourriez rencontrer pendant cette période. Cela peut également vous rafraîchir la mémoire une fois que vous vous êtes lancé.

Nous devons aussi effectuer une rapide comparaison terminologique :

| **Description** | **Adobe Analytics** | **Google Analytics** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| Mesure d’événement représentant une page (ou un écran sur une application) vue. | Page vue | Pageview |
| Mesure représentant un groupe d’interactions sur votre site web ou votre application qui ont lieu au cours de la même période. | Visite | Session |
| Mesure définissant un appareil identifié (en fonction de plusieurs critères, y compris des cookies et d’autres modèles de comportement, pour regrouper les informations sur l’utilisateur). | Visiteur unique | Utilisateur |

## 2. Les interfaces

Une des choses que je vois le plus souvent quand les gens comparent Adobe Analytics et Google Analytics, c’est qu’Adobe contient beaucoup de choses et que cela peut impressionner. C’est vrai, mais c’est également une force, pas une faiblesse. Adobe propose un large éventail d’outils et de flexibilité dans votre visualisation de données, ce qui vous offre plus de liberté pour créer ce dont vous avez besoin.

Commençons par examiner le compte rendu des performances « sur site ».

### 2.1. Compte rendu des performances sur site

#### 2.1.1. Écran d’accueil

Adobe Analytics et Google Analytics permettent de personnaliser la première vue qu’un utilisateur voit lorsqu’il se connecte.

##### 2.1.1.1. Espace de travail/Configuration personnalisée de l’écran d’accueil (Adobe Analytics)

Adobe Analytics ne présuppose pas la création d’un rapport prédéfini que tous les utilisateurs pourront afficher lors de leur connexion. La page d’accueil par défaut permet à l’utilisateur d’accéder à l’écran de destination de l’espace de travail, qui affiche pour chaque utilisateur tous les rapports de l’espace de travail qu’il a créés ou qui ont été partagés avec lui. En outre, chaque utilisateur peut définir l’un de ces rapports comme écran d’accueil s’il le souhaite.

![image1](assets/ga-to-aa_1.png)

Vous trouverez plus de détails ci-dessous concernant l’espace de travail plus loin dans ce guide. Voir Section 2.1.2.1

>[!TIP]
>
>Créez et partagez des rapports standard pour votre entreprise afin que tout le monde dispose d’un point de départ pour afficher les informations sans avoir à créer immédiatement ses propres rapports.



##### 2.1.1.2. Insights sur l’écran d’accueil (Google Analytics)

* L’écran d’accueil de Google Analytics contient des visualisations préconfigurées.  Elles couvrent des éléments tels que :
* Utilisateurs, sessions, taux de rebond et durée de session au cours des 7 derniers jours.
* Utilisateurs par heure de la journée au cours des 30 derniers jours.
* Utilisateurs actuels en ce moment et principales pages actives.
* Canal de trafic, source/média et références au cours des 7 derniers jours.
* Sessions par pays au cours des 7 derniers jours.
* Pages les plus consultées au cours 7 derniers jours
* Tendance des utilisateurs actifs au cours des 30 derniers jours
* etc.

Dans GA4, les utilisateurs ont plus d’options pour personnaliser et ajouter leurs propres rapports à l’écran d’accueil.

![image2](assets/ga-to-aa_2.png)

C&#39;est probablement la chose qui vous manquera le plus en arrivant chez Adobe ; ils n’ont pas d’écran d’accueil préconfiguré pour vous, mais vous pouvez facilement configurer un espace de travail personnalisé pour répliquer ce dont vous avez besoin à partir de ce qui précède et, si vous le souhaitez, le définir comme votre écran d’entrée. Nous y reviendrons plus tard (ou consultez la section 2.1.2.1 Espace de travail Adobe).

#### 2.1.2. Report Builders sur site

En plus des rapports simples fournis par les outils d’analyse, chaque outil fournit également des outils plus puissants pour créer vos propres rapports personnalisés.

##### 2.1.2.1. Adobe Analytics Workspace

C’est le moteur d’Adobe Analytics. Depuis son lancement en 2017, il est devenu l’outil incontournable pour l’analyse Analytics et la principale raison pour laquelle la section Rapports va bientôt disparaître.

Cet outil vous permet de créer des rapports avec une liberté presque totale.

Le rapport peut être divisé en panneaux, qui peuvent contenir un nombre illimité de visualisations. Les panneaux peuvent contenir des informations communes, telles quʼune période et des filtres de segments communs.

Les panneaux et les visualisations qu’ils contiennent peuvent être redimensionnés et déplacés pour afficher les éléments côte à côte ou empilés. Si vous souhaitez comparer deux suites de données différentes côte à côte, vous pouvez créer des panneaux divisés en deux parties égales, montrant les deux sites côte à côte pour faciliter la comparaison.

Les utilisateurs ont accès à un grand nombre de visualisations :

* Tableau à structure libre
* Tableau de cohortes
* Abandon
* Flux
* Graphiques
   * Aires (empilées et non empilées)
   * Ligne
   * Nuage de points
   * Barres (empilées et non empilées)
   * Puce
   * Anneau
   * Histogramme
   * Barres horizontales (empilées et non empilées)
* Carte
* Synthèse des blocs
   * Synthèse des modifications
   * Synthèse du texte
   * Texte (champ de texte libre permettant de saisir des informations supplémentaires pour fournir un contexte)
* Venn

Chaque panneau et visualisation peut recevoir un titre et une description, afin de fournir un contexte aux informations qui y sont répertoriées.
Dans Adobe, les segments (essentiellement des filtres pour les données) s’appliquent rétroactivement. Ils peuvent être intégrés dans les colonnes des tableaux à structure libre et permettent de comparer les données côte à côte. Par exemple, si un utilisateur souhaite comparer le trafic de deux catégories différentes sur son site, il peut créer un segment pour la « Catégorie A » et un autre pour la « Catégorie B ».

![image3](assets/ga-to-aa_3.png)

Les tableaux à structure libre permettent de disposer de plusieurs colonnes et dʼeffectuer la segmentation nécessaire pour visualiser les données comme vous le souhaitez.

En continuant lʼexemple ci-dessus, que pensez-vous de lʼapplication dʼune ventilation par date ? Rien de plus facile : faites glisser et déposez une autre dimension ou segment pour visualiser les données sous un autre angle. Par exemple, utilisez les segments Type dʼappareil, puis ajoutez une ventilation par système d’exploitation pour vos utilisateurs dʼappareils mobiles/tablettes :

![image3](assets/ga-to-aa_4.png)

Grâce à Espace de travail, votre créativité nʼest plus bridée, car vous nʼêtes pas limité aux ventilations « standard ». Vous pouvez créer les visualisations dont vous avez besoin pour analyser avec moult détails les comparaisons.

>[!TIP]
>
>Jonglez sans crainte entre les différentes visualisations, donnez libre cours à votre créativité et montrez ce que vous savez faire ! Faites tout de même attention à ce que vos créations reflètent bien ce que vous souhaitez montrer. Une expérience solide dans ce domaine vous sera dʼun atout précieux !

Vous pouvez même créer des mesures calculées ou des segments à la volée qui ne figurent quʼà lʼintérieur du rapport (ce qui évite d’inonder votre référentiel de segments et de calculs, mais vous permet également de créer des éléments ciblés nécessaires à des rapports spécifiques, sans gêner votre organisation avec des éléments qui ne sont pas très pertinents dans dʼautres contextes).

Cette discussion n’est qu’une introduction à cet outil. Il y aura d’autres guides plus complets pour vous aider à commencer. Une fois que vous l’aurez fait, vous pourrez créer des rapports complets, tels que :

![image3](assets/ga-to-aa_5.png)

Notez également que les espaces de travail n’effectuent pas df&#39;enregistrements automatiques. Il est donc plus facile d’effectuer un rapport ad hoc unique sans encombrer votre référentiel de rapports.

L’autre fonctionnalité puissante des espaces de travail est la possibilité d’appliquer des modificateurs interactifs à vos rapports sous la forme de listes déroulantes. Bien que ces listes déroulantes ne fonctionnent pas sur les fichiers CSV ou PDF exportés de vos rapports, elles vous permettent, dans le rapport dynamique, de mettre à jour toutes les visualisations d’un panneau afin d’afficher le même rapport sous différentes conditions. Plusieurs listes déroulantes peuvent être utilisées. Tant que les options ne s’excluent pas mutuellement, les éléments sélectionnés s’empilent pour permettre une présentation claire des informations.

>[!IMPORTANT]
>
>Pour en savoir plus sur l’utilisation des listes déroulantes et des ventilations à structure libre, voir <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680>.

##### 2.1.2.2. Google Analytics : tableaux de bord, rapports personnalisés et rapports enregistrés

Google dispose de quelques outils pour créer des rapports dans l’interface, mais ils suivent toujours l’affichage et les limites de la section des rapports.

En lisant ceci, ceux qui connaissent Google Analytics pourraient se dire : « Attendez une seconde, est-ce que Google Data Studio n’est pas un meilleur équivalent de l’espace de travail d’Adobe ? » Ils auraient raison. Mais comme Data Studio ne fait pas techniquement partie de l’outil Analytics et permet de se connecter à différentes sources de données, cet outil est traité plus loin dans la section « Accès aux rapports étendus » de cette discussion (et en particulier dans la section 2.2.3).

Les tableaux de bord Google et les rapports personnalisés vous permettent d’extraire plusieurs visualisations en un seul rapport. Cependant, contrairement à Espace de travail, vous n’avez accès qu’à des corrélations simples et ne décidez pas de quelles données placer dans quelles colonnes.

Dans les rapports personnalisés, l’un des plus grands défis réside dans le fait que, lorsque vous créez un filtre, il s’applique à tous les onglets du rapport... Il n’est pas possible de comparer deux filtres différents au sein d’un même rapport.

Pour les comparaisons de surface, cela fonctionne. Elles sont toutes similaires aux tableaux de bord, aux rapports personnalisés et aux signets hérités d’Adobe. Outils de base fournis pour répondre à vos besoins, qui se trouvent dans la suite de rapports.

#### 2.1.3. Rapports

Google et Adobe contiennent tous deux des rapports navigables qui sont des tableaux préconfigurés et des graphiques chronologiques de base basés sur une dimension.

##### 2.1.3.1. Rapports Adobe Analytics

Adobe Analytics dispose également d’une section Rapports, bien que celle-ci soit supprimée progressivement au profit d’Analysis Workspace (de ce fait, la fin de vie de cette interface a été annoncée puisque Espace de travail [Section 2.1.2.1] est un outil beaucoup plus puissant), où la plupart des tableaux peuvent être créés et modifiés plus facilement. Les sections d’Adobe sont beaucoup plus fragmentées, ce qui peut être décourageant :

![image3](assets/ga-to-aa_6.png)

Comme la plupart des éléments ci-dessus sont accessibles via les espaces de travail, je vais vous donner un bref aperçu de ces sections et de leur relation avec Google Analytics. Je présenterai ici les rapports qui sont toujours pertinents.

Les Mesures de site sont ce que leur nom indique : elles couvrent les mesures standard (pages vues, visiteurs uniques, visites, ainsi que les événements personnalisés que vous avez configurés). Ceci est similaire au rapport de comportement de Google Analytics, mais cela inclut également certaines mesures trouvées dans Audience (puisqu’Adobe ne divise pas les types de mesures).

Vous y trouverez également des rapports « Robots ». Le trafic provenant des robots est exclu de tous vos rapports standard. Toutefois, deux rapports vous permettent d’avoir des informations sur ce qui se passe et sur les robots qui se rendent sur votre site. Cela est particulièrement utile si vous configurez des règles de robots personnalisées pour exclure les robots spammeurs connus qui visitent fréquemment votre site. Vous pouvez avoir un aperçu de ce que ces robots font sans que vos principaux rapports ne soient inondés par ce trafic. Les rapports de robots sont actuellement indisponibles via Espace de travail (mais de nouvelles fonctionnalités de création de rapports vont bientôt permettre aux utilisateurs d’obtenir ces informations).

Le Contenu du site est un groupe de dimensions standard Adobe : nom de page, sections du site (canaux), hiérarchies (moyen de créer des rapports d’analyse personnalisés de l’entreprise dans votre site web), serveurs (cela s’avère particulièrement utile si votre site comporte plusieurs sous-domaines, ou si vous balisez plusieurs sites ensemble dans une seule suite de tracking), etc. Tout cela est disponible dans Espace de travail.

Mobile est un groupe de données spécifiques à l’équipement mobile, telles que les appareils, les types d’appareils, etc. Tout cela est disponible dans Espace de travail.

Parcours est un autre de ces éléments « pas tout à fait disponibles dans Espace de travail ». Même si Espace de travail comporte un diagramme Flux, vous ne pouvez afficher que les flux d’entrée et de sortie pour une seule page/valeur, tandis que Parcours vous permet de voir les parcours les plus courants utilisés dans votre site web. Par défaut, Pages est le premier rapport de parcours configuré, mais vous pouvez l’activer pour les props personnalisées (par exemple si vous deviez effectuer le suivi d’une valeur « Type de page », vous pourriez examiner le cheminement dans les types de page. L’autre chose que j’aime à propos de Parcours est la façon simple dont les informations sont présentées. On peut vite être dépassé par le diagramme de flux dans l’espace de travail selon ce que l’on veut voir. Je vous recommande d’essayer les deux. Ils ont chacun un usage et une valeur spécifiques en fonction de ce que vous essayez de réaliser. N’importe quelle dimension peut être utilisée dans Flux, tandis que le cheminement doit être configuré sur une prop dans le panneau d’administration.

Les rapports Sources de trafic, Campagnes et Canaux marketing sont tous similaires au rapport Acquisition de Google. Le rapport Sources de trafic se concentre sur les référents réels, Campagnes se concentre sur vos codes de campagne et Canaux marketing se concentre également sur les codes de campagne, mais applique également une logique supplémentaire, que vous déterminez, sur la manière de traiter les informations. Je trouve qu’Adobe offre beaucoup plus de liberté sur la façon de configurer vos règles, alors que Google fait beaucoup de choses pour vous. Cela va constituer un changement dans la façon de penser. Il faut également noter que, par défaut, l’attribution Google sur les codes de campagne est de 6 mois, alors qu’elle est définie sur 1 semaine pour Adobe. Cette mesure peut être modifiée dans vos paramètres d’administration, mais dans Espace de travail, vous pouvez appliquer une attribution personnalisée en plus de n’importe quelle dimension, ce qui vous offre une flexibilité à la volée bien plus grande.

Les rapports Rétention des visiteurs et Profil des visiteurs sont similaires aux rapports Audience dans Google Analytics. Le rapport Rétention est davantage axé sur la fréquence des retours, tandis que le rapport Profil des visiteurs est davantage axé sur la géographie et la technologie des utilisateurs.

Les rapports Conversion personnalisée et Trafic personnalisé sont tous deux des rapports de dimension personnalisés. Les conversions sont vos eVars dans lesquelles vous pouvez définir une expiration personnalisée pour la valeur, c’est-à-dire l’accès, la visite, le mois, l’année, etc. Cette valeur restera pour cet utilisateur pendant la période spécifiée, sauf si elle a été remplacée. Les variables de trafic sont vos props, mais vous pouvez également les configurer pour les rapports de cheminement ou sous la forme d’éléments de liste (qui divisent plusieurs valeurs en fonction d’un délimiteur de votre choix).

Le rapport Médias est destiné aux fichiers vidéo ou audio dans lesquels vous avez configuré un suivi spécial des médias.

Rapports personnalisés est une section dans laquelle un utilisateur peut personnaliser les colonnes et les ventilations qu’il a créées dans l’interface des rapports et les enregistrer en tant que rapport personnalisé. Cependant, comme nous l’avons mentionné ci-dessus, Espace de travail permet des ventilations et des corrélations beaucoup plus puissantes. Tout ce qui est personnalisé devrait simplement y être fait là. C’était une bonne solution avant l’existence de Espace de travail.

La section Signets est similaire aux rapports personnalisés, où les rapports fréquemment utilisés pouvaient être marqués d’un signet dans l’interface des rapports afin de faciliter leur recherche.

Le tableau de bord était un produit hérité qui permettait aux utilisateurs de combiner des petits rapports de données en une seule visualisation. Toutefois, la fonctionnalité de l’espace de travail (section 2.1.2.1) est bien plus facile à utiliser, si bien que cela n’existe qu’en tant que point d’accès aux rapports hérités qui doivent être recréés avant l’expiration de cette fonctionnalité.

Cibles est une zone de rapports spéciale qui permet aux utilisateurs de créer un rapport basé sur une cible pendant une période définie. Les équipes peuvent ainsi surveiller des éléments comme les campagnes afin de déterminer s’ils étaient sur la bonne voie pour atteindre leurs cibles de trafic.

Tous les rapports disponibles ici pouvaient avoir plusieurs colonnes de mesures et ventilations de dimensions. Toutefois, la simplicité des visualisations et une partie de la logique derrière les éléments pouvant être corrélés pouvaient s’avérer frustrantes.

##### 2.1.3.2. Rapports Google Analytics

Google Analytics divise ces rapports en plusieurs sections, qui sont les suivantes : Temps réel, Audience, Acquisition, Comportement et conversations (dans GA3), ainsi que Cycle de vie (avec les sous-sections Acquisition, Engagement, Monétisation, Conservation) et Utilisateur (avec les sous-sections Données démographiques et Technologie).

![image3](assets/ga-to-aa_7.png)

Vous pouvez apporter des ajustements mineurs à ces visualisations, ajouter une ventilation de dimension secondaire, modifier la visualisation, créer un filtre sur les données, etc. Vous pouvez enregistrer vos personnalisations en tant que rapport enregistré.

Vous obtenez ainsi des insights rapides et faciles sur vos données. Cependant, vous ne pouvez pas comparer des éléments comme Utilisateurs aux Pages vues pour une page dans le même tableau. Vous ne pouvez pas non plus ajouter plusieurs dimensions supplémentaires pour afficher des données supplémentaires.

Elles sont utiles pour des données analytiques rapides, mais si vous devez vraiment creuser profondément, il y a des limitations.

### 2.2. Accès aux rapports étendu

Outre le « compte rendu des performances sur site », la plupart des outils offrent des fonctionnalités étendues qui vous permettent de sortir votre analyse des outils et de créer quelque chose d’un peu plus personnalisé.

#### 2.2.1. Report Builder d’Adobe Analytics (extension Microsoft Excel)

L’espace de travail est un excellent outil, mais il est parfois nécessaire d’intégrer vos données dans une feuille de calcul personnalisée, éventuellement pour pouvoir assembler plusieurs sources de données. C’est là que Report Builder entre en jeu.

Report Builder est un plug-in de Microsoft Excel qui vous permet de créer des connexions à vos données Adobe Analytics afin d’extraire des données tabulaires que vous pouvez manipuler dans Excel. En règle générale, pour utiliser cette fonctionnalité efficacement, vous devez extraire les données dans certains onglets de données brutes, puis utiliser les références de cellule Excel pour extraire les données de ces onglets dans un seul rapport consolidé, et enfin créer des graphiques et des visualisations.

>[!NOTE]
>
>Report Builder dispose d’une autorisation spéciale qui doit être appliquée à vos utilisateurs pour qu’ils puissent accéder à ce plug-in. Cela ne devrait être accordé qu’aux utilisateurs qui ont appris à utiliser l’outil correctement.

#### 2.2.2. Connexion à l’API Adobe Analytics

Si vous avez besoin qu’Adobe Analytics soit assimilé par autre chose qu’Excel, mais que vous souhaitez toujours bénéficier des avantages des données traitées (y compris les exclusions de règles de robots), vous pouvez utiliser l’API d’Adobe pour extraire directement les données, puis les traiter via un script ou les ajouter à une base de données en vue de les utiliser avec un autre système.

Notez que l’API extrait toujours les données de corrélation en appliquant les ventilations et les segments comme indiqué dans la requête d’extraction.

L’espace de travail d’Adobe (section 2.1.2.1) utilise en fait l’API pour créer tous les rapports. Si vous activez le mode de débogage dans l’espace de travail, les appels d’API exacts utilisés sont affichés. Il s’agit d’une méthode rapide pour créer vos appels d’API à l’aide de l’espace de travail afin de créer et valider les données que vous souhaitez extraire, puis d’utiliser ces appels d’API pour extraire les données vers votre propre traitement.


#### 2.2.3. Data Studio de Google Analytics

Si vous avez tout lu, vous savez que j’ai mentionné Data Studio comme étant un équivalent de l’espace de travail d’Adobe. Data Studio vous permet d’extraire des données Google Analytics, mais aussi des données provenant d’autres sources. C’est très pratique si vous souhaitez consolider vos données Analytics avec d’autres données collectées. Mais en ce qui concerne Google Analytics, j’ai rencontré le même type de limitations de visualisation que celles présentes dans Google Analytics. La façon dont les lignes et les colonnes sont formées reste très limitée dans ce qui peut être fait.

Cela reste un outil puissant, et je ne dissuaderais pas les gens de l’utiliser. Mais après avoir utilisé l’espace de travail pendant si longtemps, je trouve que le comportement rigide est assez restrictif.


#### 2.2.4. Extension Google Sheets

En ce qui concerne mon propre usage, lorsque je dois extraire des données de manière prolongée de Google Analytics, mon outil préféré est l’extension Google Sheets. Bien sûr, je dois établir plusieurs connexions avec mes tableaux Google Analytics, mais comme avec Report Builder d’Adobe, je peux référencer les cellules des données brutes et créer les rapports dont j’ai besoin, puis les visualiser à l’aide des fonctionnalités de représentation de Google Sheets.


## 3. Exportations de données brutes

Quand vous avez vraiment besoin de données brutes, Adobe et Google vous offrent la possibilité d’extraire des informations de cette manière.

### 3.1. Flux de données d’Adobe

Dans la section 2.2.2, j’ai mentionné que l’API Adobe Analytics effectuait des extractions de « données traitées ». Le flux de données brutes continue à extraire les données traitées par les « règles de traitement » configurées dans le panneau d’administration (assurez-vous que vos données brutes sont retardées afin que toutes ces règles soient terminées au moment où le flux de données brutes est extrait), mais ces données brutes incluent toutes les données exclues partout ailleurs.

Cela signifie que toutes vos exclusions de robots, vos données internes filtrées par IP, etc. sont incluses dans les flux de données brutes. Il existe des indicateurs pour identifier ces données. Ainsi, si vous créez un lac de données, votre équipe d’ingénieurs peut créer une logique pour traiter ces données en conséquence.

Les flux de données brutes peuvent être personnalisés pour envoyer toutes les colonnes de données ou uniquement des colonnes spécifiques si vous avez besoin d’un flux plus ciblé.

Les flux peuvent être envoyés directement vers FTP, SFTP, S3, etc.


### 3.2. Google Big Query

Malheureusement, il s’agit d’un outil Google que je n’ai jamais utilisé. En théorie, il doit être similaire au flux de données d’Adobe, ce qui permet à votre équipe d’ingénieurs d’accéder aux données brutes de votre compte Google Analytics.

Cependant, il me semble qu’au lieu d’un vidage complet de données brutes, cela permet à vos ingénieurs d’accéder aux données via des requêtes SQL, afin d’extraire soit des données brutes ciblées, soit toutes les colonnes de données brutes à ingérer dans un lac de données.

## 4. Conclusion

Comme tout système, il faut de la pratique pour s’y habituer, mais j’espère que ce guide vous permettra de démarrer, ou vous donnera des conseils pour améliorer votre utilisation d’Adobe Analytics si vous n’avez fait qu’effleurer le sujet.

Je tiens toutefois à souligner que je vous recommande d’utiliser à la fois Adobe Analytics et Google Analytics dans votre stratégie d’implémentation (même si vous n’avez que la version gratuite de Google Analytics). Cela vous permet d’avoir un système de sauvegarde pour vous assurer que vous avez des données, car aucun système n’est infaillible.

Au-delà de ce guide, vous disposez de nombreuses ressources qui peuvent vous aider à améliorer votre stratégie :

* [Adobe Experience League](https://experienceleague.adobe.com/?lang=fr#home) : contient des tutoriels, des vidéos, de la documentation et des forums de la communauté.
* [Groupes d’utilisateurs Adobe](https://analytics-augs.adobe.com/) : il s’agit d’un centre d’événements gérés par la communauté pour aider les utilisateurs à entrer en contact les uns avec les autres et à améliorer leurs implémentations. Comme ils sont basés dans un certain fuseau horaire, il est préférable de vérifier ce qui se passe dans les autres régions.
* [Chaîne YouTube des groupes d’utilisateurs Adobe Analytics](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA) : vous avez manqué une session des groupes d’utilisateurs Adobe Analytics ? Regardez à nouveau les sessions précédentes des groupes dʼutilisateurs à travers le monde pour en savoir plus sur la façon dont vos pairs utilisent lʼoutil.
* [Canal Slack de Measure Chat](https://www.measure.chat/) : entrez en contact avec les utilisateurs Adobe Analytics du monde entier et partagez des enseignements du secteur, posez des questions à vos pairs et rejoignez des groupes d’intérêt axés sur les mesures.
* Et bien plus encore !

## Auteur

Ce document a été rédigé par :

![Jennifer Dungan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dungan, responsable de l’optimisation des analyses chez Torstar

Adobe Analytics Champion

