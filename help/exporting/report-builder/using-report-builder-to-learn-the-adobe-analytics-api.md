---
title: Utilisation de Report Builder pour apprendre à utiliser l’API Adobe Analytics
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
TQID: https://experienceleague.adobe.com/CnzT7nd58cibYkdt7hfAwgMF4kJR3clcTZYbditrsaM
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 279
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
