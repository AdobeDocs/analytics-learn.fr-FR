---
title: Comment identifier votre serveur de suivi Analytics et vos suites de rapports
description: Lors de la configuration d’Adobe Analytics ou de son référencement dans d’autres solutions Experience Cloud, il est souvent utile ou même nécessaire de connaître le "serveur de suivi" Analytics que vous utilisez, ou également la "suite de rapports" dans laquelle vous envoyez des données. Cette vidéo vous montre comment localiser les deux valeurs, que vous ayez ou non déjà implémenté Adobe Analytics.
feature: implementation basics
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
translation-type: tm+mt
source-git-commit: 60f4ce4f563a990576b3331b01cd87c29d424f43
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 2%

---


# Comment identifier vos suites de rapports [!DNL Tracking Server] [!UICONTROL et d’analyses] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Lors de la configuration d’Adobe Analytics ou de son référencement dans d’autres solutions Experience Cloud, il est souvent utile ou même nécessaire de connaître le [!DNL Analytics] &quot;[!DNL Tracking Server]&quot; que vous utilisez, ou également la &quot;Suite[!UICONTROL de]rapports&quot; dans laquelle vous envoyez des données. Cette vidéo vous montre comment localiser les deux valeurs, que vous ayez ou non déjà implémenté Adobe Analytics.

## Après la mise en oeuvre {#after-implementation}

Une fois la mise en oeuvre effectuée [!DNL Analytics] sur un site, vous pouvez trouver le [!DNL tracking server] et la [!DNL report suite ID] droite dans la balise de suivi. Le nom d’hôte [!DNL tracking server] est celui de la balise, ce qui est facile à trouver. Les identifiants de suite [!UICONTROL de] rapports sont une liste séparée par des virgules juste après &quot;/b/ss/&quot; dans le nom de chemin d’accès de la balise.

Pour afficher la balise, ainsi que toutes les autres informations relatives aux solutions [!DNL Analytics] et autres Experience Cloud, installez l’extension [Chrome](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=fr)&quot;Experience Cloud Debugger&quot;.

## Avant l’implémentation {#before-implementation}

**[!DNL Tracking Server]** - Si vous n’avez pas encore commencé votre mise en oeuvre Adobe Analytics, vous choisirez un sous-domaine pour le fichier &quot;.sc.omtrdc.net&quot; [!DNL tracking server]. Par exemple, supposons que j’ai un magasin de chapeaux en ligne appelé &quot;Jim’s Brims&quot;. Je peux simplement définir ma [!DNL tracking server] valeur sur :

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Report Suite]** - Pour trouver une liste de vos suites [!UICONTROL de] rapports qui ont été créées, connectez-vous [!DNL Analytics] et accédez à [!UICONTROL Admin] > [!UICONTROL Report Suites dans le menu supérieur pour afficher une liste de Report Suites, y compris leur identifiant et leur titre.]

Voir la vidéo ci-dessous pour en savoir plus.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)
