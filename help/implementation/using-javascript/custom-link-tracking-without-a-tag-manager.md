---
title: Suivi des liens personnalisés sans gestionnaire de balises
description: Pour de nombreuses actions sur la page, le suivi ne doit pas être traité comme une page vue. Dans cette vidéo, vous apprendrez à coder une balise de suivi des liens vers Analytics si vous n’utilisez pas de gestionnaire de balises (comme Experience Platform Launch). Consultez le code et découvrez un conseil important.
feature: Appmeasurement Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
role: Developer
level: Intermediate
exl-id: e4567b1c-414e-44ad-982f-52b0150e7eda
source-git-commit: 474e68e2937c82efa459b6ed8048a4abd2753285
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Suivi des liens personnalisés sans gestionnaire de balises {#custom-link-tracking-without-a-tag-manager}

Pour de nombreuses actions sur la page, le suivi ne doit pas être traité comme une page vue. Dans cette vidéo, vous apprendrez à coder une balise de suivi des liens vers Analytics si vous n’utilisez pas de gestionnaire de balises (comme Adobe [!DNL Experience Platform Launch]). Consultez le code et découvrez un conseil important.

## Envoi d’une balise s.tl() {#sending-an-s-tl-beacon}

Deux fonctions envoient des données dans Adobe Analytics :

1. s.t() - Une balise de « suivi », qui est un accès à la page vue, qui incrémente les pages vues pour le nom de page donné, ainsi que la définition d’autres variables.
1. s.tl() - Une balise « lien de suivi », souvent appelée accès/balise « lien personnalisé », qui n’incrémente pas les pages vues et ignore la variable pageName. Elle est généralement utilisée pour effectuer le suivi des actions plus petites sur la page qui ne chargent pas de nouvelle page/nouvel écran, ou d’autres actions qui n’entraînent pas de nouveau chargement de page.

>[!NOTE]
>
>Dans cette vidéo, nous vous montrons comment coder un accès à un lien personnalisé lorsque vous n’utilisez PAS un gestionnaire de balises comme Adobe [!DNL Experience Platform Launch]. Nous vous recommandons d’utiliser [!DNL Experience Platform Launch], notre recommandation de bonne pratique pour l’implémentation. Cependant, si vous devez coder dans une balise `s.tl()`, voici comment procéder.

>[!VIDEO](https://video.tv.adobe.com/v/34476/?captions=fre_fr&quality=12&learn=on)

## Exemple de code {#sample-code}

Voici l’exemple de code utilisé sur le lien personnalisé dans la vidéo :

```JavaScript
<a href="#" onclick="
    s.linkTrackVars='events,eVar2,prop2';
    s.linkTrackEvents=s.events='event2';
    s.eVar2='facebook share';
    s.prop2='facebook share';
    s.tl(this,'o','Social Share');
    s.manageVars('clearVars',s.linkTrackVars,1);">
    Click here to share on FaceBook
</a>
```
