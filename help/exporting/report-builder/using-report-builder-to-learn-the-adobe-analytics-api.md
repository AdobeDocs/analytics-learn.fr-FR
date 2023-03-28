---
title: Utilisation de Report Builder pour apprendre à utiliser l’API Adobe Analytics
description: Report Builder est un outil que nous connaissons et apprécions tous. Et si je vous disais que vous pouviez utiliser ce que vous savez de Report Builder pour améliorer encore vos compétences Adobe Analytics ? Dans cette vidéo, nous allons découvrir comment traiter les demandes de débogage de Report Builder et les utiliser pour apprendre à concevoir vos propres requêtes d’API Analytics.
feature: Report Builder
topics: null
activity: use
doc-type: feature video
team: Technical Marketing
kt: 2345
role: User
level: Intermediate
exl-id: 8b8e0dac-2498-4fba-ba4b-585b309ae1fd
source-git-commit: 8fc641743bc9e07b838a22ca64ccc15344d52764
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 100%

---

# Utilisation de [!UICONTROL Report Builder] pour apprendre à utiliser l’API Adobe Analytics {#using-report-builder-to-learn-the-adobe-analytics-api}

[!UICONTROL Report Builder] est un outil que nous connaissons et apprécions tous. Et si je vous disais que vous pouviez utiliser ce que vous savez de [!UICONTROL Report Builder] pour améliorer encore vos compétences Adobe Analytics ? Dans cette vidéo, nous allons découvrir comment traiter les demandes de débogage de [!UICONTROL Report Builder] et les utiliser pour apprendre à concevoir vos propres requêtes d’API [!DNL Analytics].

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12&learn=on)

**MISE À JOUR** : [!UICONTROL Report Builder] a légèrement mis à jour la manière dont il demande les données. Vous pouvez toujours utiliser l’approche de cette vidéo, mais les informations seront légèrement différentes dans un débogueur.

Dans un débogueur :

1 - Recherchez api5.omniture.com. Le nombre peut varier de 1 à 5 selon votre centre de données.

2 - Accédez à l’onglet [!UICONTROL Requête].

3 - Recherchez « [!DNL Report.Queue] » dans la requête.

Il existe également une autre méthode pour déboguer les requêtes de ce type, qui fonctionne tout aussi bien. Vous pouvez activer la journalisation de [!UICONTROL Report Builder] à partir du menu [!UICONTROL Options]. Les mêmes informations que celles d’un débogueur seront alors enregistrées. Les journaux se trouvent sous [!UICONTROL Documents] > [!UICONTROL ReportBuilderLogs], et sont organisés par jour. Vous pouvez rechercher « Report.Queue » dans le fichier pour trouver chacune de vos requêtes. Les journaux vous aident également à résoudre les problèmes éventuels.

Pour plus dʼinformations sur cette fonctionnalité, consultez la [documentation](https://www.adobe.io/).
