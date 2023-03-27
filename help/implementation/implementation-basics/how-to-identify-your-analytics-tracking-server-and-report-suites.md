---
title: Comment identifier votre serveur de suivi et vos suites de rapports Analytics
description: Lors de la configuration dʼAdobe Analytics ou de son référencement dans dʼautres solutions Experience Cloud, il est souvent utile ou même nécessaire de connaître le « serveur de suivi » Analytics que vous utilisez, ainsi que la « suite de rapports » dans laquelle vous envoyez des données. Cette vidéo vous montre comment localiser les deux valeurs, que vous ayez ou non déjà mis en œuvre Adobe Analytics.
feature: Implementation Basics
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer, Data Engineer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
source-git-commit: 8fc641743bc9e07b838a22ca64ccc15344d52764
workflow-type: ht
source-wordcount: '303'
ht-degree: 100%

---

# Comment identifier votre serveur Analytics [!DNL Tracking Server] et vos [!UICONTROL suites de rapports] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Lors de la configuration dʼAdobe Analytics ou de son référencement dans dʼautres solutions Experience Cloud, il est souvent utile ou même nécessaire de connaître le [!DNL Analytics] « [!DNL Tracking Server] » que vous utilisez ainsi que la « [!UICONTROL suite de rapports] » vers laquelle vous envoyez des données. Cette vidéo vous montre comment localiser les deux valeurs, que vous ayez ou non déjà mis en œuvre Adobe Analytics.

## Après la mise en œuvre {#after-implementation}

Après la mise en œuvre [!DNL Analytics] sur un site, vous pouvez trouver le [!DNL tracking server] et le [!DNL report suite ID] directement dans la balise de suivi. Le [!DNL tracking server] est le nom dʼhôte dans la balise afin de le trouver facilement. Les [!UICONTROL identifiants des suite de rapports] sont une liste séparée par des virgules juste après « /b/ss/ » dans le nom de chemin dʼaccès de la balise.

Pour afficher la balise ainsi que toutes les autres informations relatives à [!DNL Analytics] et aux autres solutions Experience Cloud, installez lʼ[extension Chrome « Experience Cloud Debugger »](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=fr).

## Avant la mise en œuvre {#before-implementation}

**[!DNL Tracking Server]** - Si vous nʼavez pas encore commencé votre mise en œuvre dʼAdobe Analytics, vous choisirez un sous-domaine pour le fichier « .sc.omtrdc.net » [!DNL tracking server]. Par exemple, supposons que jʼai un magasin de chapeaux en ligne appelé « Jimʼs Brims ». Je peux simplement définir mon [!DNL tracking server] sur :

« jimsbrims.sc.omtrdc.net ».

**[!UICONTROL Suite de rapports]** - Pour trouver une liste de vos [!UICONTROL suites de rapports] qui ont été créées, connectez-vous à [!DNL Analytics] et accédez à [!UICONTROL Admin] > [!UICONTROL Suites de rapports] dans le menu supérieur pour afficher une liste de [!UICONTROL suites de rapports], y compris leur identifiant et leur titre.

Regardez la vidéo ci-dessous pour plus dʼinformations.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12&learn=on)
