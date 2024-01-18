---
title: Utilisation d’une couche de données pour définir des variables Analytics dans Experience Platform [!DNL tags]
description: Découvrez comment utiliser une couche de données pour sources des données Analytics et d’autres solutions Experience Cloud.
feature: Tags
topics: Development
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: a45667a8d7ccb46b9e33bd11a78fac9714a61df5
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 50%

---

# Utilisation d’une couche de données pour définir des variables Analytics dans Experience Platform [!DNL tags]

L’utilisation d’une couche de données pour [!DNL Analytics] et d’autres solutions Experience Cloud est une bonne pratique. Dans cette vidéo, découvrez comment extraire des valeurs de la couche de données et les utiliser dans Experience Platform [!DNL tags] pour renseigner des variables dans Adobe Analytics.

## Couches de données

Une _couche de données_ est une structure d’objets JavaScript que les développeurs insèrent sur les pages Web numériques. Les solutions Analytics utilisent finalement la couche de données pour remplir les rapports. Systèmes de gestion des balises, y compris les Experience Platform [!DNL tags]) sont les intermédiaires qui lisent la couche de données, mettent en correspondance les valeurs avec les variables et envoient ces données aux solutions d’expérience numérique.

Consultez des informations supplémentaires sur les couches de données dans la variable [Documentation Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=fr).

## Couches de données, Experience Platform [!DNL tags], et Adobe Analytics

1. Définissez ou identifiez une norme de couche de données à utiliser sur votre site.

   1. Positionnez la couche de données aussi haut que possible dans la section head de la page et avant l’appel à Experience Platform [!DNL tags]. Cela permet à [!DNL tags] d’accéder immédiatement aux valeurs, ainsi qu’aux solutions Adobe qui doivent figurer en haut de la page, comme Adobe Target.

1. Renseignez les données de la couche de données.
1. Dans Experience Platform [!DNL tags], créez &quot;[!UICONTROL éléments de données]&quot; qui mappe les points de données dans la couche de données. Ces éléments de données sont utilisés dans tous les Experience Platform [!DNL tags] in [!UICONTROL rules] et [!UICONTROL extensions].
1. Dans la section des variables globales de l’extension [!DNL Analytics] ou dans une [!DNL Tags rule], affectez les valeurs dans les [!UICONTROL éléments de données] aux variables [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] et autres variables [!DNL Analytics].
1. Déclenchez une balise qui envoie les données dans [!DNL Analytics].

La vidéo suivante vous guide tout au long du processus.

>[!NOTE]
>
> Launch est maintenant **[!DNL tags]**

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12&learn=on)

>[!NOTE]
>
>La couche de données spécifique utilisée dans cette vidéo peut ne pas être considérée comme une « bonne pratique » pour votre entreprise. Le concept qui consiste à utiliser une couche de données pour extraire des données importantes vers vos solutions de marketing numérique est considéré comme une bonne pratique.
