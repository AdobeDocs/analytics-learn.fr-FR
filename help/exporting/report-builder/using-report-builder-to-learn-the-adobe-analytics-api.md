---
title: Utilisation du Report Builder pour apprendre l’API Adobe Analytics
description: Le Report Builder est quelque chose que nous connaissons et aimons tous. Et si je vous disais que vous pourriez utiliser ce que vous savez sur le Report Builder pour faire avancer encore plus votre skillset Adobe Analytics ? Dans cette vidéo, nous allons découvrir comment traiter les demandes de Report Builder de débogage et les utiliser pour apprendre à créer vos propres requêtes d’API Analytics.
feature: report builder
topics: null
audience: analyst
activity: use
doc-type: feature video
team: Technical Marketing
kt: 2345
translation-type: tm+mt
source-git-commit: 24ad92b0ccdf1112e3ed4a0968cd47db757598c3
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---


# Utilisation du [!UICONTROL Report Builder] pour apprendre l’API Adobe Analytics {#using-report-builder-to-learn-the-adobe-analytics-api}

[!UICONTROL Le Report Builder] est quelque chose que nous connaissons et aimons tous. Et si je vous disais que vous pourriez utiliser ce que vous savez sur le [!UICONTROL Report Builder] pour faire avancer encore plus votre skillset Adobe Analytics ? Dans cette vidéo, nous allons découvrir comment traiter les demandes de [!UICONTROL Report Builder] de débogage et les utiliser pour apprendre à créer vos propres requêtes [!DNL Analytics] API.

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12)

**MISE À JOUR**: [!UICONTROL Report Builder] a mis à jour la manière dont il demande légèrement les données. Vous pouvez toujours utiliser l&#39;approche de cette vidéo, mais les informations seront légèrement différentes dans un débogueur.

Dans un débogueur :

1 - Recherchez api5.omniture.com. Le nombre peut varier de 1 à 5 selon votre centre de données.

2 - Go to the [!UICONTROL Request] tab

3 - Recherchez &quot;[!DNL Report.Queue]&quot; dans la requête.

Il existe également une autre méthode pour déboguer des requêtes de ce type, et elle fonctionne également. Vous pouvez activer la journalisation du [!UICONTROL Report Builder] à partir du menu [!UICONTROL Options] et enregistrer les mêmes informations qu’un débogueur. Les journaux se trouvent sous [!UICONTROL Documents] > [!UICONTROL ReportBuilderLogs]et sont organisés par jour. Vous pouvez rechercher dans le fichier &quot;Report.Queue&quot; pour rechercher chacune de vos requêtes. Les journaux aident également à résoudre les problèmes éventuels.

Pour plus d’informations sur cette fonctionnalité, consultez la [documentation](https://www.adobe.io/).
