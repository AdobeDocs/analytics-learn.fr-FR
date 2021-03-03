---
title: Comment identifier votre serveur de suivi Analytics et vos suites de rapports
description: Lors de la configuration d’Adobe Analytics ou de son référencement dans d’autres solutions Experience Cloud, il est souvent utile ou même nécessaire de connaître le "serveur de suivi" Analytics que vous utilisez, ou également la "suite de rapports" dans laquelle vous envoyez des données. Cette vidéo vous montre comment localiser les deux valeurs, que vous ayez ou non déjà implémenté Adobe Analytics.
feature: Concepts de base de l’implémentation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: '"Développeur, ingénieur de données"'
level: Début
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 2%

---


# Comment identifier vos suites de rapports Analytics [!DNL Tracking Server] et  {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Lors de la configuration d’Adobe Analytics, ou lors de sa référence dans d’autres solutions Experience Cloud, il est souvent utile ou même nécessaire de connaître la [!DNL Analytics] &quot;[!DNL Tracking Server]&quot; que vous utilisez, ou aussi la &quot;[!UICONTROL Report Suite]&quot; dans laquelle vous envoyez des données. Cette vidéo vous montre comment localiser les deux valeurs, que vous ayez ou non déjà implémenté Adobe Analytics.

## Après la mise en oeuvre {#after-implementation}

Après avoir implémenté [!DNL Analytics] sur un site, vous pouvez trouver [!DNL tracking server] et [!DNL report suite ID] à droite dans la balise de suivi. [!DNL tracking server] est le nom d’hôte de la balise, ce qui est facile à trouver. Les [!UICONTROL identifiants de suite de rapports] sont une liste séparée par des virgules juste après &quot;/b/ss/&quot; dans le nom de chemin d’accès de la balise.

Pour afficher la balise, ainsi que toutes les autres informations relatives à [!DNL Analytics] et aux autres solutions Experience Cloud, installez [&quot;Experience Cloud Debugger&quot; Chrome Extension](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=fr).

## Avant l&#39;implémentation {#before-implementation}

**[!DNL Tracking Server]** - Si vous n’avez pas encore commencé votre mise en oeuvre Adobe Analytics, vous choisirez un sous-domaine pour le fichier &quot;.sc.omtrdc.net&quot;  [!DNL tracking server]. Par exemple, supposons que j’ai un magasin de chapeaux en ligne appelé &quot;Jim’s Brims&quot;. Je peux simplement définir ma [!DNL tracking server] sur :

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Report Suite]**  - Pour trouver une liste de vos  [!UICONTROL suites de ] rapports qui ont été créées, connectez-vous  [!DNL Analytics] et accédez à  [!UICONTROL Admin] >  [!UICONTROL Report Suites dans le menu supérieur pour afficher une liste de Report Suites, y compris leur identifiant et leur titre.]

Voir la vidéo ci-dessous pour en savoir plus.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)
