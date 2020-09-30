---
title: Actions de suivi (liens personnalisés AKA) dans une application mobile avec le SDK Experience Platform
description: 'Les actions sont des événements qui se produisent dans votre application mobile. Dans cette vidéo, découvrez comment utiliser l’API trackAction pour effectuer le suivi et mesurer une action. '
feature: mobile sdk
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
translation-type: tm+mt
source-git-commit: a42658cfd4bae7b077ddd48b4cf5c7db54e35c98
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# Actions de suivi (liens personnalisés AKA) dans une application mobile avec le SDK Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Les actions sont des événements qui se produisent dans votre application mobile. Dans cette vidéo, découvrez comment utiliser l’API trackAction pour effectuer le suivi et mesurer une action.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

Il s’agit de l’API que vous devez utiliser pour effectuer le suivi de toutes les actions sans chargement d’écran sur votre site. Si l’écran s’affiche, utilisez trackState, qui déclenche un accès à la vue de page. Sinon, utilisez trackAction pour envoyer des variables associées à l&#39;action en cours.

Ces données se présentent sous la forme `contextData`, ce qui signifie également que vous devrez ensuite utiliser des règles [!UICONTROL de] traitement pour extraire les données mobiles de ces `contextData` variables et les mettre en correspondance dans [!DNL eVars], [!DNL Props], Événements, etc. dans Adobe Analytics.

Pour plus d&#39;informations sur trackAction, consultez la [documentation](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference).
