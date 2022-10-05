---
title: Utilisation d’une couche de données pour définir des variables Analytics via des balises
description: Découvrez l’utilisation d’une couche de données pour l’approvisionnement de données Analytics et d’autres solutions Experience Cloud.
feature: Launch Implementation
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 9%

---

# Utilisez une couche de données pour définir des variables Analytics via [!DNL Tags] {#use-a-data-layer-to-set-analytics-variables-in-adobe-analytics-via-tags}

Utilisation d’une couche de données pour [!DNL Analytics] et d’autres solutions Experience Cloud sont une bonne pratique. Dans cette vidéo, découvrez comment extraire des valeurs de la couche de données et les utiliser dans [!DNL Experience Platform Tags] pour renseigner des variables dans Adobe Analytics.

## Couches de données {#data-layers}

A _couche de données_ est une structure d’objets JavaScript que les développeurs ajoutent aux pages web numériques. Les solutions Analytics utilisent finalement la couche de données pour remplir les rapports. Systèmes de gestion des balises, notamment [!DNL Experience Platform Tags]) sont les intermédiaires qui lisent la couche de données, mettent en correspondance les valeurs avec les variables et envoient ces données aux solutions d’expérience numérique.

Consultez des informations supplémentaires sur les couches de données dans la variable [Documentation Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=fr) et le blog [Couches de données : De Buzzword à la bonne pratique](https://blog.adobe.com/en/2014/03/13/data-layers-buzzword-best-practice).

## Couches de données, [!DNL Experience Platform Tags], et Adobe Analytics{#data-layers-launch-and-adobe-analytics}

1. Définissez ou identifiez une norme de couche de données à utiliser sur votre site.

   1. Positionnez la couche de données aussi haut que possible dans la section head de la page et avant l’appel à [!DNL Experience Platform Tags]. Cela permet d’accéder immédiatement aux valeurs par [!DNL Tags] et par Adobe des solutions qui doivent figurer en haut de la page, comme Adobe Target.

1. Renseignez les données de la couche de données.
1. Dans [!DNL Experience Platform Tags], créez &quot;[!UICONTROL éléments de données]&quot; qui mappent les points de données dans la couche de données. Ces éléments de données sont utilisés dans l’ensemble des [!DNL Experience Platform Tags] in [!UICONTROL rules] et [!UICONTROL extensions].
1. Dans le [!DNL Analytics] section des variables globales de l’extension ou dans une [!DNL Tags rule], affectez les valeurs dans [!UICONTROL éléments de données] to [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName], etc. [!DNL Analytics] .
1. Déclenchez une balise qui envoie les données dans [!DNL Analytics].

La vidéo suivante vous guide tout au long du processus.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)

>[!NOTE]
>
>La couche de données spécifique utilisée dans cette vidéo peut ne pas être considérée comme une &quot;bonne pratique&quot; pour votre entreprise. Il est recommandé d’utiliser une couche de données pour exporter des données importantes vers vos solutions de marketing numérique.