---
title: Suivi de liens personnalisés sans gestionnaire de balises
description: Pour de nombreuses actions sur la page, le suivi ne doit pas être traité comme une vue de page. Dans cette vidéo, vous apprendrez comment coder une balise de suivi des liens à Analytics, si vous n’utilisez pas de gestionnaire de balises (comme un Experience Platform Launch). Consultez le code et apprenez un conseil important.
feature: Implémentation d’AppMeasurement
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
role: '"Développeur, ingénieur de données"'
level: Intermédiaire
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 4%

---


# Suivi des liens personnalisés sans gestionnaire de balises {#custom-link-tracking-without-a-tag-manager}

Pour de nombreuses actions sur la page, le suivi ne doit pas être traité comme une vue de page. Dans cette vidéo, vous apprendrez comment coder une balise de suivi des liens à Analytics, si vous n’utilisez pas de gestionnaire de balises (tel que Adobe [!DNL Experience Platform Launch]). Consultez le code et apprenez un conseil important.

## Envoi d&#39;une balise s.tl() {#sending-an-s-tl-beacon}

Deux fonctions permettent d’envoyer des données en Adobe Analytics :

1. s.t() - Balise &quot;track&quot;, qui correspond à un accès à la vue de page, qui incrémente les vues de page pour le nom de page donné, ainsi que la définition d’autres variables.
1. s.tl() : balise de &quot;suivi du lien&quot;, souvent appelée &quot;lien personnalisé&quot; accès/balise, qui n’incrémente pas les vues de page et ignore la variable pageName. Il est généralement utilisé pour effectuer le suivi des actions plus petites sur la page qui ne chargent pas de nouvelle page/écran ou d’autres actions qui n’entraînent pas de nouveau chargement de page.

>[!NOTE]
>
>Dans cette vidéo, nous vous montrons comment coder un accès au lien personnalisé lorsque vous n’utilisez PAS un gestionnaire de balises tel que Adobe [!DNL Experience Platform Launch]. Nous vous recommandons d’utiliser [!DNL Experience Platform Launch], notre recommandation de bonne pratique pour la mise en oeuvre. Cependant, si vous devez coder dans un `s.tl()`, voici comment le faire.

>[!VIDEO](https://video.tv.adobe.com/v/25832/?quality=12)

## Exemple de code {#sample-code}

Voici l’exemple de code utilisé sur le lien personnalisé de la vidéo :

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

Pour plus d&#39;informations sur les liens personnalisés, consultez la [documentation](https://marketing.adobe.com/resources/help/fr_FR/sc/implement/function_tl.html).