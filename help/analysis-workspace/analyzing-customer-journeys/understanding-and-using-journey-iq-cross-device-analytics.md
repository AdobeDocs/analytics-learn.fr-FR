---
title: Compréhension et utilisation de Parcours IQ - Analyses entre appareils
description: Lorsque les utilisateurs interagissent avec votre marque, ils le font de différentes manières et sur plusieurs appareils. Analytics sur l’ensemble des appareils s’intègre au service Adobe Experience Platform Identity pour identifier la manière dont les appareils sont associés aux personnes. Il tire ensuite parti de cette intelligence pour créer une vue multi-appareils du comportement de l’utilisateur. Cela permet d’analyser les personnes, et non les appareils.
feature: CDA
topics: null
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
role: User
level: Intermediate
exl-id: 3748d5d7-d250-4057-8131-afdc66c80200
source-git-commit: fe861dfd541c1b9cb3b233fa3f56d55054305fd9
workflow-type: tm+mt
source-wordcount: '1641'
ht-degree: 4%

---

# Compréhension et utilisation de [!DNL Journey IQ] - Analyses entre appareils

Lorsque les utilisateurs interagissent avec votre marque, ils le font de différentes manières et sur plusieurs appareils. Les analyses entre appareils s’intègrent à la fonction [!DNL Adobe Experience Platform Identity Service] pour identifier la manière dont les appareils sont associés aux personnes. Il tire ensuite parti de cette intelligence pour créer une vue multi-appareils du comportement de l’utilisateur. Cela permet d’analyser les personnes, et non les appareils.

## Présentation des analyses entre appareils

### Je ne suis pas mes appareils

Lorsque les utilisateurs interagissent avec votre marque, ils le font de nombreuses façons et sur plusieurs &quot;surfaces&quot; ou &quot;appareils&quot;. Ils peuvent utiliser un navigateur web sur un ordinateur ou un appareil mobile, ou une application mobile. Dans les analyses numériques traditionnelles, qui ont grandi dans la collecte de données basée sur des cookies, chacune de ces surfaces est représentée sous la forme d’un &quot;visiteur&quot; unique. Cela signifie que chacun de vos utilisateurs humains est représenté sous la forme de plusieurs visiteurs uniques.

Voici un exemple. Supposons qu’Isabelle interagisse avec votre marque de la manière suivante :

*Isabelle est le Parcours Analytics traditionnel de trois*
![visiteurs](assets/cda-isabelle-journey-traditional-analytics.png)

En utilisant l&#39;analyse traditionnelle, le parcours d&#39;Isabelle se divise en trois parties. Elle est représentée par trois visiteurs uniques, qui ont chacun utilisé un appareil différent pour effectuer des tâches isolées. Ce qu&#39;il faut, c&#39;est une vision unifiée et multi-appareils des interactions d&#39;Isabelle. [!DNL Journey IQ: Cross-Device Analytics] fournit cette vue.

*Isabelle est un Parcours Analytics*
![multi-appareils](assets/cda-isabelle-journey-cross-device-analytics.png)

### Une Vue Sur Plusieurs Appareils Fournit De Meilleures Analyses

Avoir une vue personnelle et multi-appareils du comportement d&#39;Isabelle peut faire une différence significative dans votre analyse. Par exemple, l’approche traditionnelle basée sur les visiteurs ne donne pas une vue d’ensemble complète de l’efficacité des canaux marketing. Examinons à nouveau le parcours d&#39;Isabelle, en se concentrant sur la chaîne qui reçoit du crédit pour sa consultation de produit et pour son achat. Nous utiliserons l’attribution [!UICONTROL last-touch] pour plus de simplicité, mais le même problème se produit avec n’importe quel modèle d’attribution lorsque vous divisez le comportement d’Isabelle en visiteurs distincts. L&#39;utilisation de la vision traditionnelle du monde basée sur les visiteurs donne des résultats très différents, voire trompeurs :

*Attribution Analytics traditionnelle et*
![Analytics sur l’ensemble des appareils](assets/channel-attribution.png)

Notez qu’avec la vue multi-appareils, le canal email reçoit du crédit à la fois pour la vue de produit et l’achat, ce qui représente plus précisément l’expérience réelle d’Isabelle.

Continuez à lire pour en savoir plus sur :

* Fonctionnement de [!DNL Cross-Device Analytics]
* Conditions Préalables Pour [!DNL Cross-Device Analytics]
* Interprétation des données entre appareils
* Analyse des données entre appareils dans Analysis Workspace

## Fonctionnement de [!DNL Cross-Device Analytics]

[!DNL Journey IQ: Cross-Device Analytics (CDA)] s’intègre à  [!DNL Adobe Experience Platform Identity Service], en utilisant le  [[!DNL Co-op Graph]](https://experienceleague.adobe.com/docs/device-co-op/using/home.html?lang=fr) ou  [!DNL Private Graph] pour identifier la manière dont les périphériques sont mappés aux personnes. Il tire ensuite parti de cette intelligence pour créer une vue multi-appareils du comportement de l’utilisateur. Les analyses entre appareils disposent de fonctionnalités et d’outils inégalés pour aider votre entreprise à comprendre l’utilisation de plusieurs appareils et l’expérience client sur ces appareils dans leurs interactions avec votre marque. Il se trouve sous la forme d’une couche d’Analysis Workspace pour fournir des informations détaillées sur l’analyse de l’audience basée sur la personne et l’attribution, la segmentation et l’analyse de parcours sur plusieurs appareils à l’aide d’outils puissants tels que [!UICONTROL Abandon], [!DNL Flow], [!DNL Cohort], [!DNL Segment IQ] et [!DNL Attribution IQ].

### Le  [!DNL Cross-Device Virtual Report Suite]

Les analyses entre appareils sont présentées par l’intermédiaire d’un type spécial de [[!UICONTROL suite de rapports virtuelle]](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-about.html). Cela vous permet de continuer à utiliser la suite de rapports d’origine basée sur les appareils lorsque vous introduisez les analyses entre appareils dans votre entreprise. La configuration d’une suite de rapports virtuelle d’analyses entre appareils est facile.

Dans la première étape du créateur de suites de rapports virtuelles, sélectionnez la [!UICONTROL suite de rapports] qui a été configurée par Adobe comme étant compatible avec les analyses entre appareils :

*Choisissez une base de  [!UICONTROL rapports compatible avec les analyses entre appareils (source)]*
![[!UICONTROL suite de rapports] Suite de rapports virtuelleÉtape 1](assets/cda-vrs-step-one.png)

Ensuite, activez [!UICONTROL Traitement de la période de rapport] et activez [!UICONTROL groupement entre appareils] :

*Activation du  [!UICONTROL traitement de la période de ] rapport et de l’ [!UICONTROL assemblage de rapports]*
![[!UICONTROL sur plusieurs appareils ] Suite de rapports virtuelle Étape 2](assets/cda-vrs-step-two.png)

Terminez la configuration des suites de rapports virtuelles et enregistrez-la. La suite de rapports virtuelle des analyses entre appareils s’affiche dans Analysis Workspace avec une icône spéciale en regard de celle-ci, comme illustré ci-dessous :

*Sélectionnez la suite de rapports virtuelle des analyses entre appareils dans Analysis*
![[!UICONTROL Workspace ] Suite de rapports virtuelle Étape 3](assets/cda-vrs-step-three.png)

>[!TIP]
>
>Vous pouvez créer autant de [!UICONTROL suites de rapports virtuelles ] d’analyses entre appareils que vous le souhaitez par rapport à la base [!UICONTROL de rapports ] activée pour les analyses entre appareils.

### Redémarrage de l’historique

Parfois, il faut un certain temps à vos utilisateurs pour se connecter et à [!DNL Co-op Graph] ou [!DNL Private Graph] pour les identifier et les mapper ensemble à leurs appareils. Les analyses entre appareils utilisent une période de recherche arrière de 30 jours, ce qui leur permet de redéfinir un visiteur précédemment non identifié en tant que personne jusqu’à 30 jours auparavant.

Comment cela aide-t-il ? Rappelez-vous le parcours d&#39;utilisateur d&#39;Isabelle de la discussion ci-dessus :

![[!DNL Cross-Device Analytics] Parcours](assets/cda-isabelle-journey-cross-device-analytics.png)

Il est possible qu’Isabelle ne se soit pas connectée avant d’effectuer l’achat, et que [!DNL Co-op Graph] ou [!DNL Private Graph] n’aient pas mappé les appareils d’Isabelle avant un certain temps après son achat. Mais la recherche en amont de 30 jours des Analyses entre appareils permet aux Analyses entre appareils de redéfinir le comportement passé d’Isabelle au niveau de la personne, ce qui vous permet d’avoir une vue d’ensemble de son parcours dont vous avez besoin.

>[!NOTE]
>
>Puisque l’historique peut être redémarré, cela signifie que vos données peuvent changer au fil du temps dans une [!UICONTROL suite de rapports virtuelle ] compatible avec les analyses entre appareils. Gardez cela à l’esprit lorsque vous communiquez des informations à partir d’une analyse basée sur les analyses entre appareils.

## Conditions Préalables Pour [!UICONTROL Analyses Entre Appareils]

Les analyses entre appareils sont incluses avec [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html). À compter de septembre 2019, les clients [!DNL Analytics Ultimate] qui remplissent les conditions préalables répertoriées ci-dessous peuvent utiliser les analyses entre appareils. Les conditions préalables pour les analyses entre appareils sont les suivantes :

* Votre société doit être membre de [!DNL Adobe Experience Platform Identity Service] [[!DNL Co-op Graph]](https://experienceleague.adobe.com/docs/device-co-op/using/home.html) ou utiliser une balise [!DNL Adobe Experience Platform Identity Service Private Graph].
* Vous devez mettre en oeuvre tous les éléments requis pour [!DNL Co-op Graph] ou [!DNL Private Graph], y compris [ID Experience Cloud (ECID)](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=fr) et synchronisation des identifiants avec le graphique. Veuillez noter qu’en plus des exigences techniques, le [!DNL Co-op Graph] a d’autres exigences légales et contractuelles.
* Il n’est actuellement pas possible d’utiliser deux organisations IMS avec une seule [!DNL Private Graph]. Vous devez donc effectuer une normalisation sur une seule organisation IMS. Dans certains cas, il est possible pour un client avec plusieurs organisations IMS d’utiliser [!DNL Co-op Graph] conjointement avec les analyses entre appareils.
* [!DNL Co-op graph] et [!DNL Private Graph], ainsi que certains composants des Analyses entre appareils, sont hébergés à [!DNL Microsoft Azure]. Cela signifie que [!DNL Analytics] les données sont copiées entre le centre de traitement des données de l’Adobe et la présence de l’Adobe dans [!DNL Microsoft Azure]. Certaines [!DNL Analytics] données seront stockées dans [!DNL Azure]. Votre entreprise doit accepter cet arrangement.
* Les analyses entre appareils nécessitent une [!UICONTROL suite de rapports] &quot;multi-appareils&quot;. En d’autres termes, la [!UICONTROL suite de rapports] que vous utilisez pour les analyses entre appareils doit inclure des données provenant de plusieurs types d’appareils ou &quot;surfaces&quot; différents, tels que le web pour ordinateur de bureau, le web mobile et l’application mobile. Depuis septembre 2019, le volume des appels au serveur pour cette [!UICONTROL suite de rapports] doit être de 100 millions d’appels au serveur par jour ou moins. (Les limites du volume des appels au serveur augmenteront au cours des prochains mois.)
* Depuis septembre 2019, les [!DNL Co-op Graph] et [!DNL Private Graph] ne sont disponibles qu&#39;en Amérique du Nord. La planification de la présence graphique dans les zones EMEA et APAC sera annoncée ultérieurement. Si vous vous trouvez dans ces régions, nous vous encourageons à commencer à examiner ces conditions préalables afin que vous soyez prêt à partir du moment où le graphique sera disponible.

## Interprétation des données entre appareils

### Personnes hors visiteurs

Dans les Analyses entre appareils [!UICONTROL suite de rapports virtuelle], quelques modifications s’affichent. Par exemple, la mesure [!UICONTROL Visiteurs uniques] est remplacée par deux nouvelles mesures : [!UICONTROL Personnes] et [!UICONTROL Appareils uniques]. Ces nouvelles mesures vous donnent un meilleur aperçu de la taille de l’audience.

*Mesure Personnes et*
![appareils uniquesCDA  [!UICONTROL Personnes]](assets/cda-people-metric.png)

Dans le [[!UICONTROL créateur de segments]](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=fr), le conteneur de segments [!UICONTROL Visiteur] a été remplacé par un conteneur de segments [!UICONTROL Personne]. À l’aide d’une suite de rapports virtuelle CDA, vous pouvez créer des segments interpériphériques tels que :

* Personnes qui utilisent plusieurs appareils
* Personnes qui commencent leur parcours sur un appareil mobile, puis effectuent un achat sur un ordinateur de bureau
* Visites où des personnes utilisent plusieurs appareils pour accomplir une tâche

*Segments*
![[!DNL Segment Builder]  au niveau de la personnePersonContainer](assets/cda-segment-builder-person-container.png)

### Persistance des Dimensions

Dans une suite de rapports virtuelle CDA, des dimensions telles que [!DNL eVars] persistent désormais automatiquement sur tous les appareils. Par exemple, un [!DNL eVar] configuré comme suit :

* Attribution : Le plus récent (Dernier)
* Expire après : Achat

persistera désormais automatiquement d’un appareil à un autre jusqu’à ce que l’événement Achat soit déclenché.

## Analyse des données entre appareils dans Analysis Workspace

### Analyse de l’audience basée sur une personne

Vous êtes-vous déjà demandé combien de personnes interagissent avec votre marque ? Avez-vous voulu comprendre combien et quel type d’appareils ils utilisent ? Comment leur utilisation se superpose-t-elle ? À l’aide d’une suite de rapports virtuelle CDA, vous pouvez créer des [diagrammes de Venn](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/venn.html?lang=fr) et des [histogrammes ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/histogram.html?lang=fr) inter-appareils.

**
![Analyse de l’audience basée sur une personneVenn et Histogramme](assets/cda-venn-and-histogram.png)

### Multi-appareils [!DNL Flow]

Avec les analyses entre appareils et Analysis Workspace, vous pouvez visualiser la manière dont les personnes passent d’un appareil à un autre au fil du temps dans la balise [[!DNL Flow visualization]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/flow/flow.html). Vous pouvez voir où ils abandonnent dans leur parcours, et où ils continuent.

*[!DNL Flow]avec CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Multi-appareils [!DNL Fallout]

Vous utilisez probablement plusieurs [[!DNL Fallout visualizations]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html?lang=fr) pour analyser la façon dont les utilisateurs réussissent à passer par une série donnée d’étapes avant d’atteindre le succès. Saviez-vous que votre vue de ces [!DNL Fallout visualizations] est limitée lors de l’utilisation d’analyses traditionnelles basées sur les appareils ? Pour réussir une &quot;chute&quot;, l’étape suivante doit se produire dans le même navigateur ou la même application que l’étape précédente. Dans les analyses basées sur un appareil, vous ne connaissez pas les personnes qui ont réussi l’étape suivante sur un autre appareil.

Pour ne pas vous inquiéter, CDA vous a couvert. Les analyses entre appareils créent une vue multi-appareils qui rend [!DNL Fallout visualizations] beaucoup plus utile. Après tout, ce qui compte vraiment, c&#39;est de savoir si la personne a finalement réussi quelque part dans sa tâche.

*[!DNL Fallout]avec CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Comme les analyses entre appareils créent une couche de données multi-appareils sous Analysis Workspace, toutes vos analyses seront adaptées aux différents appareils. [[!DNL Attribution IQ]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution/attribution.html) est un exemple puissant. [!DNL Attribution IQ] dans Analysis Workspace, vous permet de comparer plusieurs modèles d’attribution côte à côte. Grâce à cette fonctionnalité, vous pouvez désormais comparer la contribution de différents appareils à la réussite.

Supposons, par exemple, que vous souhaitiez comprendre à quelle fréquence un téléphone mobile est le premier appareil utilisé dans une interaction qui, finalement, mène au succès. Ceci représente le &quot;taux d’acquisition&quot; du téléphone mobile. CDA + [!DNL Attribution IQ] permet d’effectuer cette analyse :

*[!DNL Attribution IQ]avec CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

Pour plus d’informations, voir la [[!DNL Cross-Device Analytics] documentation d’aide](https://experienceleague.adobe.com/docs/analytics/components/cda/cda-home.html).
