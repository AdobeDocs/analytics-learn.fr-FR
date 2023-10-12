---
title: Comment identifier votre serveur de suivi Analytics et votre identifiant de suite de rapports
description: Lors de la configuration d’Adobe Analytics ou de son référencement dans d’autres solutions Experience Cloud, il est souvent utile ou même nécessaire de connaître le "serveur de suivi" Analytics que vous utilisez, ou également la "suite de rapports" dans laquelle vous envoyez des données. Cette vidéo vous montre comment localiser les deux valeurs, que vous ayez ou non déjà mis en œuvre Adobe Analytics.
feature: Implementation Basics
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer, Data Engineer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
source-git-commit: 42bf16df9585d1f41206b81bf509a72c10f1d7f2
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 17%

---

# Comment identifier vos analyses [!DNL tracking server] et [!UICONTROL identifiant de suite de rapports] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Lors de la configuration d’Adobe Analytics ou de son référencement dans d’autres solutions Experience Cloud, il est souvent utile ou même nécessaire de connaître le &quot;serveur de suivi&quot; Analytics que vous utilisez, ou également le &quot;serveur de suivi&quot;[!UICONTROL suite de rapports]&quot; dans lequel vous envoyez des données. Cette vidéo vous montre comment localiser les deux valeurs, que vous ayez ou non déjà mis en œuvre Adobe Analytics.

>[!IMPORTANT]
>
>Cet article et cette vidéo s’appliquent à une mise en oeuvre &quot;AppMeasurement&quot; d’Adobe Analytics, et non à une mise en oeuvre utilisant le SDK Web.

## Après la mise en oeuvre {#after-implementation}

Après avoir implémenté Analytics sur un site, vous pouvez trouver la variable [!DNL tracking server] et la variable [!DNL report suite ID] directement dans la balise de suivi. La variable [!DNL tracking server] est le nom d’hôte dans la balise, il est donc facile de le trouver. La variable [!UICONTROL suite de rapports] Les identifiants sont une liste séparée par des virgules juste après &quot;/b/ss/&quot; dans le nom de chemin d’accès de la balise.

Pour afficher la balise, ainsi que toutes les autres informations provenant d’Analytics et d’autres solutions Experience Cloud, installez la variable [Extension Chrome &quot;Experience Cloud Debugger&quot;](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=fr).

## Avant la mise en œuvre {#before-implementation}

**[!DNL Tracking server]** - Si vous n’avez pas encore commencé avec votre implémentation Adobe Analytics, vous choisirez un sous-domaine pour le fichier &quot;.sc.omtrdc.net&quot;. [!DNL tracking server]. Par exemple, supposons que j&#39;ai une boutique en ligne appelée &quot;Jim&#39;s Brims&quot;. Je peux simplement définir mon [!DNL tracking server] sur :

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Suite de rapports]** - Pour trouver une liste de vos [!UICONTROL suites de rapports] créés, connectez-vous [!DNL Analytics] et accédez à [!UICONTROL Administration] > [!UICONTROL Suites de rapports] dans le menu supérieur pour afficher une liste de [!UICONTROL suites de rapports], y compris leur identifiant et leur titre.

Regardez la vidéo ci-dessous pour plus dʼinformations.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12&learn=on)
