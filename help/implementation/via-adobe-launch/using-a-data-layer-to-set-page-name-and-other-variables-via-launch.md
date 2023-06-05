---
title: Utiliser une couche de données pour définir des variables Analytics via des balises
description: Découvrez l’utilisation d’une couche de données pour l’approvisionnement de données Analytics et d’autres solutions Experience Cloud.
feature: Launch Implementation
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: 7224af1bd798d447f1b14c61e836f8e5c8af7ea4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 96%

---

# Utiliser une couche de données pour définir des variables Analytics via [!DNL Tags] {#use-a-data-layer-to-set-analytics-variables-in-adobe-analytics-via-tags}

L’utilisation d’une couche de données pour [!DNL Analytics] et d’autres solutions Experience Cloud est une bonne pratique. Dans cette vidéo, vous allez découvrir comment extraire vos valeurs de la couche de données et les utiliser dans [!DNL Experience Platform Tags] pour renseigner les variables dans Adobe Analytics.

## Couches de données {#data-layers}

Une _couche de données_ est une structure d’objets JavaScript que les développeurs insèrent sur les pages Web numériques. Les solutions Analytics utilisent finalement la couche de données pour remplir les rapports. Les systèmes de gestion des balises, notamment [!DNL Experience Platform Tags]) sont les intermédiaires qui lisent la couche de données, mappent les valeurs sur les variables et envoient ces données aux solutions d’expérience digitale.

Consultez des informations supplémentaires sur les couches de données dans la variable [Documentation Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=fr).

## Couches de données, [!DNL Experience Platform Tags], et Adobe Analytics{#data-layers-launch-and-adobe-analytics}

1. Définissez ou identifiez une norme de couche de données à utiliser sur votre site.

   1. Positionnez la couche de données aussi haut que possible dans la section d’ancre de la page et avant l’appel à [!DNL Experience Platform Tags]. Cela permet à [!DNL Tags] d’accéder immédiatement aux valeurs, ainsi qu’aux solutions Adobe qui doivent figurer en haut de la page, comme Adobe Target.

1. Renseignez les données de la couche de données.
1. Dans [!DNL Experience Platform Tags], créez les « [!UICONTROL éléments de données] » qui mappent les points de données dans la couche de données. Ces éléments de données sont utilisés dans l’ensemble des [!DNL Experience Platform Tags] dans les [!UICONTROL règles] et les [!UICONTROL extensions].
1. Dans la section des variables globales de l’extension [!DNL Analytics] ou dans une [!DNL Tags rule], affectez les valeurs dans les [!UICONTROL éléments de données] aux variables [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] et autres variables [!DNL Analytics].
1. Déclenchez une balise qui envoie les données dans [!DNL Analytics].

La vidéo suivante vous guide tout au long du processus.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12&learn=on)

>[!NOTE]
>
>La couche de données spécifique utilisée dans cette vidéo peut ne pas être considérée comme une « bonne pratique » pour votre entreprise. Le concept qui consiste à utiliser une couche de données pour extraire des données importantes vers vos solutions de marketing numérique est considéré comme une bonne pratique.