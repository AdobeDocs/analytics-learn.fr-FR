---
title: Utilisation d’une couche de données pour définir le nom de page et d’autres variables en Adobe Analytics par lancement
description: L’utilisation d’une couche de données pour Analytics et d’autres solutions Experience Cloud est considérée comme une bonne pratique. Dans cette vidéo, vous allez découvrir comment extraire vos valeurs de la couche de données et les utiliser dans Lancer pour renseigner des variables en Adobe Analytics.
feature: Lancement de l’implémentation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
role: '"Développeur, ingénieur de données"'
level: Début
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 4%

---


# Utilisation d&#39;une couche de données pour définir le nom de page et d&#39;autres variables via [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

L’utilisation d’une couche de données pour [!DNL Analytics] et d’autres solutions Experience Cloud est considérée comme une bonne pratique. Dans cette vidéo, vous allez découvrir comment extraire vos valeurs de la couche de données et les utiliser dans [!DNL Experience Platform Launch] pour renseigner des variables en Adobe Analytics.

## Calques de données {#data-layers}

Il est recommandé d’utiliser une couche de données lors de l’utilisation de données sur votre site et de solutions Adobe Experience Cloud, en particulier avec Adobe Analytics. Une _couche de données_ est une structure d’objets JavaScript que les développeurs insèrent sur les pages. Les couches de données peuvent être utilisées par des outils de suivi (y compris des systèmes de gestion des balises tels que [!DNL Experience Platform Launch]) pour renseigner les rapports. Vous trouverez des informations supplémentaires sur les couches de données dans la [documentation Experience Cloud](https://marketing.adobe.com/resources/help/en_US/sc/implement/ref-data-layer.html) ou sur le [site W3C](https://www.w3.org/).

Consultez également le blog [Data Layers : De Buzzword à Best Practice,](https://theblog.adobe.com/data-layers-buzzword-best-practice/), qui vous donne de superbes informations sur les couches de données, ainsi que quelques exemples.

## Calques de données, [!DNL Experience Platform Launch] et Adobe Analytics (oh mon ?){#data-layers-launch-and-adobe-analytics-oh-my}

1. Créez une norme de couche de données à utiliser sur votre site, qui peut être référencée par [!DNL Experience Platform Launch].

   1. Placez cette couche de données aussi haut que possible dans l’en-tête de la page, avant l’appel à [!DNL Experience Platform Launch], de sorte que les valeurs puissent être utilisées immédiatement par [!DNL Launch] et par les solutions d’Adobe qui doivent se trouver en haut de la page, comme Adobe Target.

1. Renseignez les données de la couche de données.
1. Dans [!DNL Experience Platform Launch], créez &quot;[!UICONTROL éléments de données]&quot; qui référencent les points de données dans la couche de données et qui peuvent être utilisés dans [!DNL Experience Platform Launch] dans [!UICONTROL règles], [!UICONTROL extensions], etc.
1. Utilisez les [!UICONTROL éléments de données] dans les variables globales de l&#39;extension [!DNL Analytics] ou dans une règle, en affectant les valeurs dans [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] ou d&#39;autres variables [!DNL Analytics].
1. Déclenchez une balise qui envoie les données dans [!DNL Analytics].

La vidéo suivante vous guide tout au long du processus.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
