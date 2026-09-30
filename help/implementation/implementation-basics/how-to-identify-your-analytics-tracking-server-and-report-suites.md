---
title: Identification de votre serveur de suivi et de votre identifiant de suite de rapports Analytics
description: Lors de la configuration dʼAdobe Analytics ou de son référencement dans dʼautres solutions Experience Cloud, il est souvent utile ou même nécessaire de connaître le « serveur de suivi » Analytics que vous utilisez, ainsi que la « suite de rapports » dans laquelle vous envoyez des données. Cette vidéo vous montre comment localiser les deux valeurs, que vous ayez ou non déjà mis en œuvre Adobe Analytics.
feature: Implementation Basics
topics:
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
TQID: 'https://experienceleague.adobe.com/DRy-lxNuEQR9Tb-nIoev0Mu1OzSiCcLcqve1eDf7p6Q'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 3e00cf9416ba2c6886e5a7efb952cac8ce370930
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 100%
---
# Comment identifier votre [!DNL tracking server] et votre [!UICONTROL identifiant de suite de rapports] Analytics. {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Lors de la configuration dʼAdobe Analytics ou de son référencement dans dʼautres solutions Experience Cloud, il est souvent utile ou même nécessaire de connaître le « serveur de suivi » Analytics que vous utilisez, ainsi que la « [!UICONTROL suite de rapports] » dans laquelle vous envoyez des données. Cette vidéo vous montre comment localiser les deux valeurs, que vous ayez ou non déjà mis en œuvre Adobe Analytics.

>[!IMPORTANT]
>
>Cet article et cette vidéo s’appliquent à une mise en œuvre « AppMeasurement » d’Adobe Analytics et non à une mise en œuvre utilisant le SDK Web.

## Après la mise en œuvre {#after-implementation}

Après la mise en œuvre d’Analytics sur un site, vous pouvez trouver le [!DNL tracking server] et l’[!DNL report suite ID] directement dans la balise de suivi. Le [!DNL tracking server] est le nom dʼhôte dans la balise. Il est donc facile à trouver. Les identifiants des [!UICONTROL suites de rapports] sont une liste séparée par des virgules juste après « /b/ss/ » dans le nom de chemin dʼaccès de la balise.

Pour afficher la balise ainsi que toutes les autres informations relatives à Analytics et aux autres solutions Experience Cloud, installez lʼ[extension Chrome « Experience Cloud Debugger »](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=fr).

## Avant la mise en œuvre {#before-implementation}

**[!DNL Tracking server]** : si vous nʼavez pas encore commencé votre mise en œuvre dʼAdobe Analytics, choisissez un sous-domaine pour le [!DNL tracking server] « .sc.omtrdc.net ». Imaginons que je possède une boutique de chapeaux en ligne appelée « Jim’s Brims ». Je peux simplement définir mon [!DNL tracking server] sur :

« jimsbrims.sc.omtrdc.net ».

**[!UICONTROL Suite de rapports]** : pour trouver une liste de vos [!UICONTROL suites de rapports] qui ont été créées, connectez-vous à [!DNL Analytics] et accédez à [!UICONTROL Admin] > [!UICONTROL Suites de rapports] dans le menu supérieur pour afficher une liste de [!UICONTROL suites de rapports], y compris leur identifiant et leur titre.

Regardez la vidéo ci-dessous pour plus dʼinformations.

>[!VIDEO](https://video.tv.adobe.com/v/40894/?captions=fre_fr&quality=12&learn=on)
