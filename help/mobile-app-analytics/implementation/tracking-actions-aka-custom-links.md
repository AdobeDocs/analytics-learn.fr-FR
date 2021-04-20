---
title: Suivi des actions (liens personnalisés) dans une application mobile avec le SDK Experience Platform
description: 'Les actions désignent des événements qui se produisent dans votre application mobile. Dans cette vidéo, découvrez comment utiliser l’API trackAction afin de suivre et mesurer une action. '
feature: Mobile SDK
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
topic: Mobile
role: "Developer, Data Engineer"
level: Experienced
translation-type: ht
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: ht
source-wordcount: '181'
ht-degree: 100%

---


# Suivi des actions (liens personnalisés) dans une application mobile avec le SDK Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Les actions désignent des événements qui se produisent dans votre application mobile. Dans cette vidéo, découvrez comment utiliser l’API trackAction afin de suivre et mesurer une action.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

Il s’agit de l’API à utiliser pour effectuer le suivi de toutes les actions sans chargement d’écran sur votre site. Si l’écran apparaît, utilisez trackState pour déclencher un accès de page vue. Sinon, utilisez trackAction pour envoyer des variables associées à l’action en cours.

Ces données sont fournies sous forme de `contextData`, ce qui signifie par ailleurs que vous devrez ensuite utiliser des [!UICONTROL règles de traitement] pour extraire les données mobiles de ces variables `contextData` et les mapper en [!DNL eVars], [!DNL Props], Événements, etc. dans Adobe Analytics.

Pour plus d’informations sur trackAction, consultez la [documentation](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference).
