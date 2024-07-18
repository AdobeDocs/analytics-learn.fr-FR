---
title: Création de segments de parcours client - deuxième partie
description: Dans la deuxième partie, découvrez comment créer des segments d’intention de visite d’achat et de rétention pour comprendre le parcours d’achat des clients et personnaliser le contenu. En utilisant des signaux tels que des clics ou des connexions "Réserver maintenant", nous identifions l’intention d’achat et de rétention pour une analyse efficace et un marketing ciblé.
feature: Segmentation
role: User
level: Experienced
last-substantial-update: 2023-07-21T00:00:00Z
jira: KT-13476
thumbnail: KT-13476.jpeg
exl-id: 2db73010-5cd0-4454-a4ba-fc1667a50cba
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1997'
ht-degree: 0%

---

# Création de segments de parcours client - deuxième partie

Dans la deuxième partie, découvrez comment créer des segments d’intention de visite d’achat et de rétention pour comprendre le parcours d’achat des clients et personnaliser le contenu. En utilisant des signaux tels que des clics ou des connexions &quot;Réserver maintenant&quot;, nous identifions l’intention d’achat et de rétention pour une analyse efficace et un marketing ciblé.

## Création de segments d’intention de visite d’achat et de rétention

Dans notre dernier billet, nous avons décrit le processus de création de segments d’intention de visite et créé notre premier segment d’intention de visite, One Hit Wonders (L’unique accès se pose la question). Aujourd’hui, nous allons créer nos segments Achat et Rétention . Nous avions segmenté environ 23 % de nos visites et créé nos espaces réservés pour les segments d’intention de visite restants.

![Image 1](assets/Image-1.png)

Les segments d’intention de visite que nous sommes en train de créer constituent la base de la création de segments de parcours client basés sur les visiteurs. Nous allons créer ces segments de parcours basés sur les visiteurs une fois que nous aurons créé nos segments d’intention de visite.

Rappelez-vous que la création de segments d’intention de visite est un processus d’élimination. Donc, nous ne construisons pas ces segments dans l&#39;ordre chronologique. Nous créons nos segments d’intention de visite afin de les définir plus facilement pour les rendre plus difficiles à définir :

1. Intention : 0 - Une question se pose :
1. Intention : 3 - Achat
1. Intention : 4 - Rétention
1. Intention : 2 - Considération
1. Intention : 1 - Sensibilisation

Dans notre dernier billet, j&#39;ai appelé le segment &quot;Achat&quot; &quot;Réservation&quot; puisque je suis dans le secteur des voyages. Mais à l’avenir, nous l’appellerons le segment Achat pour faciliter son application à plusieurs secteurs.

Plus le signal est clair, plus il est facile de créer le segment. Dans notre dernier billet, nous avons créé notre segment One Hit Wonders (Les merveilles de l’accès), qui était le plus facile à définir car il s’agissait simplement d’un trafic de rebond. Vous constaterez que les segments d’intention d’achat et de rétention sont également très faciles à définir, puisqu’ils sont basés sur des signaux très clairs.

## Le Parcours client est différent de la propension à acheter

Lorsque nous étudions la création de notre segment d’intention d’achat, il est important de se rappeler que l’identification de l’emplacement d’un client dans son parcours diffère de la propension. Certains modèles de propension à l’achat peuvent noter les visiteurs web afin de prédire la probabilité qu’ils effectuent un achat. Ces modèles sont très utiles, mais ils sont différents du segment d’intention d’achat que nous allons créer aujourd’hui.

Bien qu’un modèle de propension cherche à prédire si un visiteur achètera, nos segments d’intention de visite cherchent à comprendre où se trouve une personne dans son parcours d’achat. L’utilisation de segments d’intention pour comprendre l’état d’esprit d’un client nous aide à personnaliser le contenu et le marketing personnalisé pour générer le trafic approprié pour alimenter notre pipeline de ventes. Ainsi, notre segment d’intention d’achat recherche des signaux comportementaux explicites qui indiquent qu’un visiteur cherche à effectuer un achat.

## Création du segment d’intention de visite d’achat

Le segment Intention de visite d’achat est facile à définir. Dans mon cas, quiconque clique sur le bouton &quot;Réserver maintenant&quot; indique une sorte d&#39;intention de réserver une croisière. Cela revient à cliquer sur &quot;Passage en caisse&quot; pour un détaillant en ligne ou sur un lien &quot;S’abonner&quot; dans un contexte multimédia.

Vous devez faire preuve de jugement lorsque vous décidez quel signal utiliser pour indiquer le mode d’achat. Nous voulons que notre segment d’intention d’achat contienne tous les achats, mais le taux de conversion ne doit pas être de 100 %. Par conséquent, nous ne voulons pas utiliser la page Confirmation d’achat ou Remerciements pour ce segment.

De même, la page Passez en revue votre achat (ou tout ce qui se trouve immédiatement avant la confirmation d’achat) est probablement trop éloignée de l’entonnoir pour être utile pour l’analyse et le ciblage.

À mesure que vous remontez l’entonnoir, il devient moins évident que le signal soit utile ou non pour indiquer qu’un client a l’intention d’effectuer un achat. Dans mon cas, &quot;Réserver maintenant&quot; est similaire à un lien de vente au détail &quot;Passage en caisse&quot;, et c&#39;est le signal que j&#39;ai utilisé. Mais dans un contexte de vente au détail, le passage en caisse peut encore être trop éloigné de l’entonnoir et l’option Afficher le panier ou même Ajouter au panier peut être préférable.

On peut voir ça comme une épicerie. Si quelqu&#39;un ramasse un produit sur l&#39;étagère qui ne veut pas dire qu&#39;il a l&#39;intention de l&#39;acheter. Même s&#39;ils le mettent dans leur panier, ils pourraient le remettre immédiatement sur l&#39;étagère. Mais s&#39;ils mettent le produit dans leur panier et commencent à le parcourir, il y a de grandes chances qu&#39;ils veuillent l&#39;acheter. Et s&#39;ils entrent dans la file d&#39;attente avec ce produit, c&#39;est un très bon pari qu&#39;ils achèteront.

Je suggère d’utiliser des pages visitées ou d’autres signaux explicites d’intention d’achat et d’éviter d’autres signaux moins directs pour identifier l’intention d’achat. Par exemple, je n’utiliserai pas le nombre de sessions ou le nombre de pages dans une session ou une session similaire. Ces signaux indirects indiquent la Considération et non l’intention d’achat. Souvenez-vous que l’objectif de ce segment est de déduire l’intention du visiteur pour la visite, et non sa propension.

### Utilisation d’Analytics Workspace pour identifier les signaux d’intention d’achat

Le rapport sur les abandons est très utile pour identifier un bon signal qui indique l’intention d’achat. Recherchez un endroit qui indique logiquement l’intention. Vous pouvez confirmer que l’étape indique l’intention lorsque vous constatez qu’un abandon notable se dirige vers cette étape, souvent suivi d’un abandon plus petit pour l’étape immédiatement après.

![Image 2](assets/Image-2.png)

Il est également utile de consulter les taux de conversion associés aux différentes pages de votre site. Cela s’avère particulièrement utile pour identifier les pages qui indiquent le mode d’achat, mais qui peuvent ne pas être nécessaires pour effectuer un achat (telles que les pages de financement, les pages de configuration des achats, etc.).

![Image 3](assets/Image-3.png)

Enfin, il est important d’inclure toutes les pages entre le début de l’achat et la confirmation d’achat dans votre segment. Les visiteurs peuvent rebondir et reprendre votre flux d’achat à différents points.

### Exclusion d’autres segments

N’oubliez pas, dans notre premier billet, que les segments d’ intention de visite doivent être mutuellement exclusifs et complètement exhaustifs. C&#39;est un refrain que vous entendrez beaucoup dans cette série.

Veillez à ce que votre segment d’intention d’achat exclut les segments Un et Terminé . Il vous suffit d’exclure les segments Une et Terminé , car les signaux que nous utilisons pour l’intention d’achat sont très spécifiques.

Notez que l’exclusion du segment Un et Terminé peut exclure une personne qui accède de nouveau à votre site sur une page de passage en caisse. Ceci est normal. La définition même de &quot;Un et terminé&quot; est une page vue, ce qui signifie que même si un visiteur accède ou actualise une page de passage en caisse, sa visite n’a pas progressé. Par conséquent, il n’y a aucune expression d’intention d’achat.

### Segment d’intention d’achat dans le créateur de segments

La définition de segment pour l’intention d’achat est très simple.

À l’aide du conteneur de visites, incluez les pages ou autres actions qui indiquent explicitement une intention d’effectuer un achat. Si vous avez plusieurs conditions d’inclusion, veillez à les placer dans un conteneur joint par la condition &quot;Et&quot;.

Ajoutez un conteneur Exclure au segment joint par la condition &quot;Et&quot;. Ajoutez la définition de segment One Hit Wonders (Pages vues égale à 1) au conteneur Exclure .

![Image 4](assets/Image-4.png)

Il est recommandé d’étiqueter les conteneurs. Vous serez heureux de l’avoir fait, d’autant plus que nos définitions de segment deviennent plus complexes.

Maintenant que nous avons créé le segment Intention d’achat, nous pouvons utiliser le Workspace de qualité des données d’intention de visite pour nous assurer que notre segment Intention d’achat s’exclut mutuellement de notre segment Un et Terminé.

![Image 5](assets/Image-5.png)

## Création du segment d’intention de visite de rétention

Dans le secteur des croisières, de nombreux invités se rendent sur notre site web pour gérer une réservation, mais pas nécessairement pour faire un achat. Ils peuvent se rendre sur le site pour y trouver des informations sur les voyages, revoir leur itinéraire, faire des réservations de repas ou bien d&#39;autres choses, sans faire de courses pour une croisière. Nos invités peuvent également acheter des excursions à la côte ou d’autres améliorations de leur expérience. Nous considérons que ces améliorations font partie de la rétention. Nous les conservons donc à l’écart de notre segment de réservation (que nous appelons &quot;Achat&quot; dans cette série de blogs).

Les clients de vente au détail peuvent être en mesure d’effectuer des retours ou de gérer leur programme de fidélité. Les abonnés aux médias ou aux technologies peuvent utiliser le produit. Si votre invité se trouve sur votre site web pour gérer sa relation avec vous, il s’agit d’une visite de rétention et nous devons examiner ces signaux. Et si vous fournissez un produit en ligne, comme Media, Tech, Online Banking, ou d&#39;autres, il y a probablement beaucoup d&#39;autres types de segments d&#39;intention de visite que nous ne discuterons pas dans cette série.

Comme pour le segment Intention d’achat , nous recherchons des indications d’intention très explicites. Pour moi, nous avons une section entière du site dédiée à la gestion d&#39;une croisière afin qu&#39;il soit facile d&#39;identifier ces pages. Cela peut être plus complexe pour d’autres entreprises. Recherchez des signaux tels que les connexions, la gestion de compte, les visites de pages de prise en charge, etc.

Je dois noter que &quot;Rétention&quot; est un nom un peu gênant pour cette intention de visite, puisque le visiteur ne se trouve pas sur notre site, &quot;afin de pouvoir être conservé en tant que client&quot;. La rétention est notre intention pour cette visite. Souvenez-vous simplement d’être empathique envers nos clients et de rester concentré sur le client avant tout !

### Utilisation d’Analytics Workspace pour identifier les signaux d’intention de rétention

Encore une fois, Analytics Workspace nous aide à identifier le mode de rétention. Vous pouvez utiliser les dimensions de page, de section de site ou de segment personnalisé pour classer vos pages par catégorie. Recherchez des pages présentant de faibles taux de conversion d’achats. Dans notre cas, nous constatons que les pages d’archivage et d’extraction en ligne (Shorex) ont des taux de conversion relativement plus faibles que les autres pages qui sont plus logiquement associées aux achats.

![Image 6](assets/Image-6.png)

Il est également conseillé de rechercher des pages à trafic élevé dans Workspace. Analysez la liste des pages à trafic élevé et décidez s’elles indiquent une intention de rétention.

## Exclusion d’autres segments

Encore une fois, nos segments d’intention de visite doivent être mutuellement exclusifs et complètement exhaustifs. Si tu n&#39;en as pas encore assez de lire ça, tu le seras ! Pour notre segment d’intention de rétention, il est absolument important d’exclure les comportements d’intention d’achat.

Pour la plupart d’entre nous, l’intention d’achat et l’intention de rétention ne sont pas des comportements mutuellement exclusifs. Nous avons des invités qui viennent sur le site web pour gérer leur croisière à venir, mais aussi pour réserver leur prochain voyage (merci !). Si vous êtes un restaurant, un visiteur peut vérifier ses points de fidélité, puis passer une commande en ligne.

Même si le comportement n’est pas mutuellement exclusif, nos segments doivent être réservés à l’analyse de Parcours client. Nous pouvons créer d’autres segments très intéressants pour analyser le chevauchement entre les comportements d’achat et de fidélité. Mais à nos fins actuelles, ces segments doivent s’exclure mutuellement.

La génération de la demande étant l’un des principaux objectifs du marketing, notre segment d’intention de rétention exclura l’intention d’achat. En d’autres termes, si un visiteur se rend sur notre site pour gérer une croisière, mais indique également son intention de réserver une nouvelle croisière, cette visite sera effectuée dans le segment de l’intention d’achat.

### Segment d’intention de rétention dans le créateur de segments

Nos définitions de segment deviennent un peu plus tendres. Inclure les visites dans votre segment. Ajoutez vos signaux d’intention de rétention. Pour moi, c&#39;était simple. Si le nom de la page commence par &quot;bge:&quot; (nos pages d’invités réservées), vous êtes dans le segment. J’ai ajouté que le nombre de pages vues est supérieur à un pour une mesure supplémentaire (mais nous excluons toujours les questions d’accès ci-dessous).

Ajoutez ensuite des conteneurs d’exclusion pour vos visites One Hit Wonders et Purchase Intent. Assurez-vous que vos conteneurs sont unis par la condition &quot;Et&quot;.

![Image 7](assets/Image-7.png)

Une fois de plus, consultez votre Workspace de qualité des données d’intention de visite pour vous assurer que vos segments s’excluent mutuellement. Nos segments d’intention de visite prennent parfaitement forme !

![Image 8](assets/Image-8.png)

À ce stade, nous avons configuré trois de nos cinq segments d’intention de visite. Ces segments s’excluent mutuellement. Dans notre prochain billet, nous créerons les derniers segments sur l’intention de la visite, les considérations et la prise de conscience, et nos segments seront tous complètement exhaustifs. Une fois nos segments d’intention de visite configurés, nous les rassemblerons dans des segments basés sur les visiteurs que vous trouverez très utiles pour l’analyse et la personnalisation.

## Auteur

Ce document a été rédigé par :

![Aaron Fossum](assets/aaron-headshot.png)

**Aaron Fossum**, Director, Digital Analytics

Adobe Analytics Champion
