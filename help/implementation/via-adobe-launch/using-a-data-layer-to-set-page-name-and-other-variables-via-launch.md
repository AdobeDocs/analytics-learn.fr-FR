---
title: Utilisation dʼune couche de données pour définir le nom de page et dʼautres variables dans Adobe Analytics via Launch
description: L’utilisation d’une couche de données pour Analytics et d’autres solutions Experience Cloud est considérée comme une bonne pratique. Dans cette vidéo, vous allez découvrir comment extraire vos valeurs de la couche de données et les utiliser dans Launch pour renseigner les variables dans Adobe Analytics.
feature: Launch Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
role: Developer, Data Engineer
level: Beginner
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: fe861dfd541c1b9cb3b233fa3f56d55054305fd9
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 100%

---

# Utilisation d’une couche de données pour définir le nom de page et d’autres variables via [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

L’utilisation d’une couche de données pour [!DNL Analytics] et d’autres solutions Experience Cloud est considérée comme une bonne pratique. Dans cette vidéo, vous allez découvrir comment extraire vos valeurs de la couche de données et les utiliser dans [!DNL Experience Platform Launch] pour renseigner les variables dans Adobe Analytics.

## Couches de données {#data-layers}

Une bonne pratique consiste à utiliser une couche de données lorsque vous utilisez des données sur votre site et les solutions Adobe Experience Cloud, en particulier avec Adobe Analytics. Une _couche de données_ est une structure d’objets JavaScript que les développeurs insèrent sur les pages. Les couches de données peuvent être utilisées par les outils de suivi (y compris les systèmes de Tag Management comme [!DNL Experience Platform Launch]) afin de renseigner des rapports. En savoir plus sur les couches de données dans la [documentation d’Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=fr) ou sur le [site W3C](https://www.w3.org/).

Consultez également le billet de blog [Couches de données : de l’expression à la mode à la bonne pratique](https://theblog.adobe.com/data-layers-buzzword-best-practice/), qui fournit de précieuses informations sur les couches de données ainsi que quelques exemples.

## Couches de données, [!DNL Experience Platform Launch] et Adobe Analytics (rien que ça !) {#data-layers-launch-and-adobe-analytics-oh-my}

1. Créez une couche de données standard à utiliser sur votre site, qui peut être référencée par [!DNL Experience Platform Launch].

   1. Insérez cette couche de données aussi haut que possible dans l’en-tête de la page, avant l’appel à [!DNL Experience Platform Launch], de sorte que les valeurs puissent être utilisées immédiatement par [!DNL Launch] et par les solutions d’Adobe qui doivent être élevées sur la page, comme Adobe Target.

1. Renseignez les données de la couche de données.
1. Dans [!DNL Experience Platform Launch], créez des « [!UICONTROL éléments de données] » qui référencent les points de données dans la couche de données et qui peuvent être utilisés dans [!DNL Experience Platform Launch], dans les [!UICONTROL règles], les [!UICONTROL extensions], etc.
1. Utilisez les [!UICONTROL éléments de données] dans les variables globales de l’extension [!DNL Analytics] ou dans une règle, en attribuant les valeurs dans [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] ou d’autres variables [!DNL Analytics].
1. Déclenchez une balise qui envoie les données dans [!DNL Analytics].

La vidéo suivante vous guide tout au long du processus.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
