---
title: Présentation et utilisation du QI du Parcours - Analyses sur plusieurs périphériques
description: Lorsque les utilisateurs interagissent avec votre marque, ils le font de nombreuses manières et sur plusieurs périphériques. Analytics sur plusieurs périphériques s’intègre au service d’identité Adobe Experience Platform afin d’identifier comment les périphériques correspondent aux personnes. Il utilise ensuite cette intelligence pour créer une vue inter-périphériques du comportement des utilisateurs. Cela se traduit par la possibilité de faire analyse sur les gens, pas sur les appareils.
feature: CDA
topics: null
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
role: Business Practitioner
level: Intermediate
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '1667'
ht-degree: 6%

---


# Compréhension et utilisation de [!DNL Journey IQ] - Analyses sur plusieurs périphériques

Lorsque les utilisateurs interagissent avec votre marque, ils le font de nombreuses manières et sur plusieurs périphériques. Analytics sur plusieurs périphériques s’intègre à l’[!DNL Adobe Experience Platform Identity Service] pour identifier comment les périphériques correspondent aux personnes. Il utilise ensuite cette intelligence pour créer une vue inter-périphériques du comportement des utilisateurs. Cela se traduit par la possibilité de faire analyse sur les gens, pas sur les appareils.

## Présentation des analyses sur plusieurs périphériques

### Je ne suis pas mes appareils

Lorsque les utilisateurs interagissent avec votre marque, ils le font de nombreuses manières et sur plusieurs &quot;surfaces&quot; ou &quot;périphériques&quot;. Ils peuvent utiliser un navigateur Web sur un ordinateur ou un périphérique mobile, ou ils peuvent utiliser une application mobile. Dans les analyses numériques traditionnelles, qui ont grandi dans la collecte de données basée sur des cookies, chacune de ces surfaces est représentée par un &quot;visiteur&quot; unique. Cela signifie que chacun de vos utilisateurs humains est représenté sous la forme de plusieurs visiteurs uniques.

Voici un exemple. Supposons qu’Isabelle ait interagi avec votre marque de la manière suivante :

*Isabelle est trois*
![visiteursParcours Analyses traditionnelles](assets/cda-isabelle-journey-traditional-analytics.png)

En utilisant les analyses traditionnelles, le parcours d&#39;Isabelle se divise en trois parties. Elle est représentée en tant que trois visiteurs uniques, dont chacun a utilisé un dispositif différent pour effectuer des tâches isolées. Il faut une vue unifiée et transversal des interactions d&#39;Isabelle. [!DNL Journey IQ: Cross-Device Analytics] fournit cette vue.

*Isabelle est un Parcours d’analyses*
![sur plusieurs périphériques](assets/cda-isabelle-journey-cross-device-analytics.png)

### Une Vue Sur Plusieurs Périphériques Offre De Meilleures Analyses

Avoir une vue du comportement d&#39;Isabelle centrée sur la personne et sur plusieurs périphériques peut faire une différence significative dans votre analyse. Par exemple, l’approche traditionnelle fondée sur le visiteur ne vous donne pas une vue complète de l’efficacité du canal marketing. Regardons de nouveau le parcours d&#39;Isabelle, en nous concentrant sur quel canal reçoit du crédit pour sa vue de produits et pour son achat. Nous utiliserons l&#39;attribution [!UICONTROL last-touch] pour la simplicité, mais le même problème survient en utilisant n&#39;importe quel modèle d&#39;attribution lorsque vous divisez le comportement d&#39;Isabelle en visiteurs distincts. L&#39;utilisation de la vue traditionnelle du monde basée sur les visiteurs donne des résultats très différents, voire trompeurs :

*Attribution des canaux Analytics traditionnels par rapport aux canaux*
![Analytics sur plusieurs périphériques](assets/channel-attribution.png)

Notez qu&#39;avec la vue sur plusieurs périphériques, le canal électronique reçoit du crédit à la fois pour la vue du produit et pour l&#39;achat, ce qui représente plus précisément l&#39;expérience réelle d&#39;Isabelle.

Continuez à lire pour en savoir plus sur :

* Fonctionnement de [!DNL Cross-Device Analytics]
* Conditions préalables pour [!DNL Cross-Device Analytics]
* Interprétation des données sur plusieurs périphériques
* Analyse des données sur plusieurs périphériques en Analysis Workspace

## Fonctionnement de [!DNL Cross-Device Analytics]

[!DNL Journey IQ: Cross-Device Analytics (CDA)] s&#39;intègre à la  [!DNL Adobe Experience Platform Identity Service], en utilisant soit le  [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/fr-FR/device-co-op/using/home.html) ou  [!DNL Private Graph] pour identifier comment les périphériques correspondent aux personnes. Il utilise ensuite cette intelligence pour créer une vue inter-périphériques du comportement des utilisateurs. CDA comprend des fonctionnalités et des outils inégalés pour aider votre entreprise à comprendre l&#39;utilisation de plusieurs périphériques et l&#39;expérience client de ces périphériques dans leurs interactions avec votre marque. Il est situé sous Analysis Workspace pour fournir des informations détaillées sur l&#39;analyse d&#39;audience basée sur la personne et l&#39;attribution, la segmentation et l&#39;analyse des parcours sur plusieurs périphériques à l&#39;aide d&#39;outils puissants tels que [!UICONTROL Abandon], [!DNL Flow], [!DNL Cohort], [!DNL Segment IQ] et [!DNL Attribution IQ].

### Le [!DNL Cross-Device Virtual Report Suite]

L&#39;ADC est présenté au moyen d&#39;un type spécial de suite de rapports multipériphériques [[!UICONTROL virtuelle]](https://docs.adobe.com/content/help/fr-FR/analytics/components/virtual-report-suites/vrs-about.html). Cela vous permet de continuer à utiliser la suite de rapports d’origine basée sur les périphériques lorsque vous introduisez les analyses inter-périphériques dans votre entreprise. La mise en place d&#39;une SRC CDA est facile.

Dans l’étape 1 du créateur de suites de rapports virtuelles, sélectionnez la [!UICONTROL suite de rapports] qui a été configurée par Adobe comme étant activée pour CDA :

*Choisir une base de  [!UICONTROL rapports (source) compatible CDA]*
![[!UICONTROL Suite de rapports virtuelle ] Suite de rapportsPremière étape](assets/cda-vrs-step-one.png)

Ensuite, activez [!UICONTROL Traitement du temps des rapports] et activez [!UICONTROL l&#39;assemblage sur plusieurs périphériques] :

*Activer le  [!UICONTROL traitement ] des rapports et l&#39; [!UICONTROL assemblage sur plusieurs périphériquesSuite de rapports virtuelle]*
![ Étape 2](assets/cda-vrs-step-two.png)

Terminez la configuration de la suite de rapports virtuelle et enregistrez-la. La suite de rapports virtuelle CDA s’affiche en Analysis Workspace avec une icône spéciale en regard de celle-ci, comme illustré ci-dessous :

*Sélectionnez la suite de rapports virtuelle CDA dans Analyse*
![[!UICONTROL Workspace] Suite de rapports virtuelleEtape 3](assets/cda-vrs-step-three.png)

>[!TIP]
>
>Vous pouvez créer autant de suites de rapports virtuelles [!UICONTROL CDA ] que vous le souhaitez en plus de la base de rapports [!UICONTROL activée par CDA ].

### Redémarrage de l&#39;historique

Il peut parfois s’écouler un certain temps avant que vos utilisateurs se connectent et que [!DNL Co-op Graph] ou [!DNL Private Graph] ne les identifient et mappent leurs périphériques. L&#39;ADC utilise une fenêtre de recherche en amont de 30 jours, ce qui lui permet de retraiter un visiteur précédemment non identifié comme une personne jusqu&#39;à 30 jours dans le passé.

Comment cela aide-t-il ? Rappelez-vous le parcours d&#39;utilisateur d&#39;Isabelle de la discussion ci-dessus :

![[!DNL Cross-Device Analytics] Parcours](assets/cda-isabelle-journey-cross-device-analytics.png)

Il est possible qu&#39;Isabelle n&#39;ait pas ouvert de session avant de faire l&#39;achat, et que les [!DNL Co-op Graph] ou [!DNL Private Graph] n&#39;aient pas cartographié les appareils d&#39;Isabelle avant un certain temps après son achat. Mais le retour en arrière de 30 jours de l&#39;ADC permet à l&#39;ADC de reproduire le comportement passé d&#39;Isabelle au niveau de la personne, en vous fournissant la vue inter-périphériques de son parcours dont vous avez besoin.

>[!NOTE]
>
>Comme l&#39;historique peut être redémarré, cela signifie que vos données peuvent changer au fil du temps dans une [!UICONTROL suite de rapports virtuelle ] activée par CDA. Gardez cela à l’esprit lorsque vous communiquez des renseignements provenant d’une analyse fondée sur l’ADC.

## Conditions préalables pour [!UICONTROL Analyses sur plusieurs périphériques]

L&#39;ADC est inclus avec [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html). À compter de septembre 2019, les clients [!DNL Analytics Ultimate] qui remplissent les conditions énumérées ci-dessous peuvent utiliser l&#39;ADC. Les conditions préalables à l&#39;ADC sont les suivantes :

* Votre société doit être membre de [!DNL Adobe Experience Platform Identity Service] [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) ou utiliser [!DNL Adobe Experience Platform Identity Service Private Graph].
* Vous devez implémenter tout ce qui est requis pour [!DNL Co-op Graph] ou [!DNL Private Graph], y compris [ID Experience Cloud (ECID)](https://docs.adobe.com/content/help/fr-FR/id-service/using/home.html) et ID synchronisés avec le graphique. Veuillez noter qu&#39;outre les exigences techniques, le [!DNL Co-op Graph] a d&#39;autres exigences juridiques et contractuelles.
* Il n&#39;est actuellement pas possible d&#39;utiliser deux organisations IMS avec un seul [!DNL Private Graph], vous devez donc normaliser sur une seule organisation IMS. Dans certains cas, il est possible pour un client disposant de plusieurs services IMS d&#39;utiliser le [!DNL Co-op Graph] conjointement avec l&#39;ADC.
* Les [!DNL Co-op graph] et [!DNL Private Graph], ainsi que certains composants de l&#39;ADC, sont hébergés dans [!DNL Microsoft Azure]. Cela signifie que les données [!DNL Analytics] sont copiées entre le centre de traitement des données de l’Adobe et la présence de l’Adobe dans [!DNL Microsoft Azure]. Certaines données [!DNL Analytics] seront stockées dans [!DNL Azure]. Votre société doit accepter cet arrangement.
* L’ADC requiert une suite de rapports [!UICONTROL inter-périphériques]. En d’autres termes, la [!UICONTROL suite de rapports] que vous utilisez pour CDA doit inclure des données provenant de plusieurs types de périphériques ou de &quot;surfaces&quot; différents, tels que le web pour ordinateur de bureau, le web mobile et l’application mobile. À compter de septembre 2019, le volume des appels serveur pour cette [!UICONTROL suite de rapports] doit être de 100 millions d&#39;appels serveur par jour ou moins. (Les limites de volume des appels du serveur augmenteront au cours des prochains mois.)
* Depuis septembre 2019, les [!DNL Co-op Graph] et [!DNL Private Graph] ne sont disponibles qu&#39;en Amérique du Nord. Le calendrier de la présence des graphiques dans la zone EMEA et l&#39;APAC sera annoncé à une date ultérieure. Si vous êtes dans ces régions, nous vous encourageons à début d&#39;examiner ces conditions préalables dès maintenant afin que vous soyez prêt à y aller lorsque le graphique sera disponible.

## Interprétation des données sur plusieurs périphériques

### Personnes non Visiteuses

Dans la suite de rapports virtuelle [!UICONTROL Virtual Report Suite] de l’ADC, vous verrez quelques modifications. Par exemple, la mesure [!UICONTROL Visiteurs uniques] est remplacée par deux nouvelles mesures : [!UICONTROL Personnes] et [!UICONTROL Périphériques uniques]. Ces nouvelles mesures vous permettent de mieux comprendre la taille des audiences.

*Mesure Personnes et*
![périphériques uniques [!UICONTROL Personnes CDA]](assets/cda-people-metric.png)

Dans le [[!UICONTROL Créateur de segments]](https://docs.adobe.com/content/help/fr-FR/analytics/components/segmentation/segmentation-workflow/seg-build.html), le conteneur de segments [!UICONTROL Visiteur] a été remplacé par un conteneur de segments [!UICONTROL Personne]. A l’aide d’une suite de rapports virtuelle CDA, vous pouvez créer des segments interpériphériques tels que :

* Personnes qui utilisent plusieurs périphériques
* Personnes qui commencent leur parcours sur un périphérique mobile puis effectuent un achat ultérieur sur un périphérique de bureau
* Visites où des personnes utilisent plusieurs appareils pour accomplir une tâche

*Segments de niveau personne*
![[!DNL Segment Builder]  PersonneContainer](assets/cda-segment-builder-person-container.png)

### Persistance de la Dimension

Dans une suite de rapports virtuelle CDA, les dimensions telles que [!DNL eVars] persistent désormais automatiquement sur tous les périphériques. Par exemple, un [!DNL eVar] configuré comme suit :

* Affectation : Le plus récent (Dernier)
* Expire après : Achat

persistera désormais automatiquement d’un périphérique à l’autre jusqu’à ce que le événement d’achat soit déclenché.

## Analyse des données sur plusieurs périphériques en Analysis Workspace

### Analyse d&#39;Audience basée sur la personne

Vous êtes-vous déjà demandé combien de personnes interagissent avec votre marque ? Avez-vous voulu comprendre combien et quel type d&#39;appareils ils utilisent ? Comment leur utilisation se recoupe-t-elle ? A l’aide d’une suite de rapports virtuelle CDA, vous pouvez créer des diagrammes [Venn](https://docs.adobe.com/content/help/fr-FR/analytics/analyze/analysis-workspace/visualizations/venn.html) interpériphériques et des histogrammes [par personne](https://docs.adobe.com/content/help/fr-FR/analytics/analyze/analysis-workspace/visualizations/histogram.html).

**
![Analyse des audiences basée sur la personneVenn et Histogramme](assets/cda-venn-and-histogram.png)

### Multi-appareils [!DNL Flow]

Avec CDA et Analysis Workspace, vous pouvez visualiser comment les gens passent d&#39;un appareil à l&#39;autre au fil du temps dans le [[!DNL Flow visualization]](https://docs.adobe.com/content/help/fr-FR/analytics/analyze/analysis-workspace/visualizations/flow/flow.html). Vous pouvez voir où ils abandonnent dans leur parcours, et où ils continuent.

*[!DNL Flow]avec CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Multi-appareils [!DNL Fallout]

Vous utilisez probablement plusieurs [[!DNL Fallout visualizations]](https://docs.adobe.com/content/help/fr-FR/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html) pour analyser comment les utilisateurs réussissent au cours d’une série d’étapes donnée avant d’atteindre le succès. Saviez-vous que votre vue de ces [!DNL Fallout visualizations] est limitée lors de l&#39;utilisation d&#39;analyses traditionnelles basées sur des dispositifs ? Pour que les &quot;abandons&quot; réussissent, l’étape suivante doit se produire dans le même navigateur ou application que l’étape précédente. Dans les analyses basées sur un périphérique, vous n’êtes pas conscient des personnes qui effectuent l’étape suivante sur un autre périphérique.

Pas d&#39;inquiétude, l&#39;ADC vous a couvert. L&#39;ADC crée la vue multipériphériques qui rend [!DNL Fallout visualizations] beaucoup plus utile. Après tout, ce qui compte vraiment, c&#39;est si la personne a finalement réussi quelque part dans sa tâche.

*[!DNL Fallout]avec CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Etant donné que l’ADC crée une couche de données inter-périphériques sous Analysis Workspace, toute votre analyse sera parfumée dans une perspective inter-périphériques. Un exemple puissant est le [[!DNL Attribution IQ]](https://docs.adobe.com/content/help/fr-FR/analytics/analyze/analysis-workspace/attribution/models.html). [!DNL Attribution IQ] en Analysis Workspace vous permet de comparer plusieurs modèles d’attribution côte à côte. Grâce à cette fonctionnalité, vous pouvez maintenant comparer comment différents périphériques contribuent à la réussite.

Supposons, par exemple, que vous souhaitiez comprendre à quelle fréquence un téléphone portable est le premier appareil utilisé dans une interaction qui conduit finalement à la réussite. Ceci représente le &quot;taux d&#39;acquisition&quot; du téléphone mobile. CDA + [!DNL Attribution IQ] vous permet de faire cette analyse :

*[!DNL Attribution IQ]avec CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

Pour plus d&#39;informations, consultez la [[!DNL Cross-Device Analytics] documentation d&#39;aide](https://docs.adobe.com/content/help/fr-FR/analytics/components/cda/cda-home.html).
