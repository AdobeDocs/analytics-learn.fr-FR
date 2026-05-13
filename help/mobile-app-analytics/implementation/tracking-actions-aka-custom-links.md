---
title: Suivi des actions (liens personnalisés) dans une application mobile avec le SDK Experience Platform
description: Les actions désignent des événements qui se produisent dans votre application mobile. Dans cette vidéo, découvrez comment utiliser l’API trackAction afin de suivre et mesurer une action.
feature: Mobile SDK
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
topic: Mobile
role: Developer
level: Experienced
exl-id: 541c51b8-638e-43b4-90ac-0ce94290a141
TQID: https://experienceleague.adobe.com/msvft7mQiNGjLqGEezPIbwruvSbsunPGUIFF1q7vlT0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 73%

---

# Suivi des actions (liens personnalisés) dans une application mobile avec le SDK Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Les actions désignent des événements qui se produisent dans votre application mobile. Dans cette vidéo, découvrez comment utiliser l’API trackAction afin de suivre et mesurer une action.

>[!VIDEO](https://video.tv.adobe.com/v/328312/?captions=fre_fr&quality=12&learn=on)

Il s’agit de l’API à utiliser pour effectuer le suivi de toutes les actions sans chargement d’écran sur votre site. Si l’écran apparaît, utilisez trackState pour déclencher un accès de page vue. Sinon, utilisez trackAction pour envoyer des variables associées à l’action en cours.

Ces données sont fournies en tant que `contextData`, ce qui signifie également que vous devrez utiliser les [!UICONTROL &#x200B; règles de traitement &#x200B;] pour prendre les données mobiles de ces variables de `contextData` et les mapper dans des [!DNL eVars], des [!DNL Props], des événements, etc. dans Adobe Analytics.

Pour plus d’informations sur trackAction, consultez la [documentation](https://developer.adobe.com/client-sdks/documentation/getting-started/track-events/#track-user-actions-for-adobe-analytics).
