---
title: Création de segments de parcours client - deuxième partie
description: Dans la deuxième partie, découvrez comment créer des segments d’intention de visite d’achat et de rétention pour comprendre le parcours d’achat des clients et clientes et personnaliser le contenu. Grâce à des signaux tels que les clics ou les connexions « Réservez maintenant », nous identifions l'intention d'achat et de conservation pour une analyse efficace et un marketing ciblé.
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

Dans la deuxième partie, découvrez comment créer des segments d’intention de visite d’achat et de rétention pour comprendre le parcours d’achat des clients et clientes et personnaliser le contenu. Grâce à des signaux tels que les clics ou les connexions « Réservez maintenant », nous identifions l&#39;intention d&#39;achat et de conservation pour une analyse efficace et un marketing ciblé.

## Créer des segments d’intention de visite d’achat et de rétention

Dans notre dernier article, nous avons décrit le processus de création des segments d’intention de visite et créé notre premier segment d’intention de visite, One Hit Wonders. Aujourd’hui, nous allons créer nos segments d’achat et de rétention. Nous avons segmenté environ 23 % de nos visites et nous avons créé nos espaces réservés pour les segments Visite intentionnelle restants.

![Image 1](assets/Image-1.png)

Les segments d’intention de visite que nous créons actuellement sont la base de la création de segments de parcours client basés sur les visiteurs. Nous créerons ces segments de parcours basés sur les visiteurs après avoir créé nos segments d’intention de visite.

Rappelez-vous que la création de segments d’intention de visite est un processus d’élimination. Nous ne créons donc pas ces segments dans l’ordre chronologique. Nous créons nos segments d’intention de visite dans l’ordre de ceux qui sont les plus faciles à définir et de ceux qui le sont le plus :

1. Intention : 0 - Un Accès Aux Merveilles
1. Intention : 3 - Achat
1. Intention : 4 - Rétention
1. Intention : 2 - Considération
1. Intention : 1 - Sensibilisation

Dans notre dernier billet, j&#39;ai appelé le segment « Achat » « Réservation » puisque je suis dans le secteur du voyage. Mais à l’avenir, nous l’appellerons le segment Achat pour qu’il soit plus facile de l’appliquer à plusieurs industries.

Plus le signal est clair, plus il est facile de créer le segment. Dans notre dernier article, nous avons créé notre segment des merveilles à un accès, qui était le plus facile à définir puisqu’il s’agissait uniquement de trafic rebond. Vous constaterez que les segments d’intention d’achat et de conservation sont également très faciles à définir, car ils sont basés sur des signaux très clairs.

## Le Parcours client est différent de la propension à acheter

Lorsque nous envisageons de créer notre segment intention d’achat, il est important de se rappeler que l’identification de l’emplacement d’un client dans son parcours est différente de la propension. Vous disposez peut-être de modèles de propension à l’achat qui évaluent les visiteurs et visiteuses web afin de prédire leur probabilité d’effectuer un achat. Ces modèles sont très utiles, mais ils sont différents du segment Intention d’achat que nous allons créer aujourd’hui.

Tandis qu’un modèle de propension cherche à prédire si un visiteur effectuera un achat, nos segments d’intention de visite cherchent à déterminer où une personne se trouve dans son parcours d’achat. L’utilisation des segments d’intention pour comprendre l’état d’esprit d’un client nous aide à personnaliser le contenu et à adapter le marketing afin de générer le trafic approprié pour alimenter notre pipeline de vente. Ainsi, notre segment Mode d’achat recherche des signaux comportementaux explicites qui indiquent qu’un visiteur souhaite effectuer un achat.

## Création du segment d’intention de visite d’achat

Le segment Intention de visite d’achat est facile à définir. Dans mon cas, quiconque clique sur le bouton « Réserver maintenant » indique une sorte d&#39;intention de réserver une croisière. Cela revient à cliquer sur « Passer en caisse » pour un retailer en ligne ou sur un lien « S’abonner » dans un contexte multimédia.

Vous devrez faire preuve de jugement lorsque vous déciderez du signal à utiliser pour déduire l&#39;intention d&#39;achat. Nous voulons que notre segment Mode d’achat contienne tous les achats, mais le taux de conversion ne doit pas être de 100 %. Nous ne voulons donc pas utiliser la page de confirmation d’achat ou de remerciement pour ce segment.

De même, la page Vérifier votre achat (ou toute autre page juste avant la confirmation d’achat) est probablement trop éloignée de funnel pour être utile à l’analyse et au ciblage.

Plus vous montez dans le funnel, plus il devient difficile de déterminer si le signal est utile ou non pour indiquer qu’un client a l’intention d’effectuer un achat. Dans mon cas, « Réserver maintenant » est similaire à un lien « Passage en caisse » de vente au détail, et c&#39;est le signal que j&#39;ai utilisé. Cependant, dans un contexte de vente au détail, Passer en caisse peut toujours être trop éloigné du funnel et Afficher le panier ou même Ajouter au panier peut être préférable.

On peut considérer cela comme quelque chose comme une épicerie. Si quelqu&#39;un achète un produit sur le marché, cela ne veut pas dire qu&#39;il a l&#39;intention de l&#39;acheter. Même s&#39;ils le mettent dans leur panier, ils pourraient le remettre immédiatement sur les tablettes. Mais s&#39;ils mettent le produit dans leur panier et commencent à se promener avec, il y a de bonnes chances qu&#39;ils veuillent l&#39;acheter. Et s&#39;ils passent à la caisse avec ce produit, c&#39;est un bon pari qu&#39;ils vont acheter.

Je suggère d’utiliser les pages visitées ou d’autres signaux explicites d’intention d’achat et d’éviter d’autres signaux moins directs pour identifier l’intention d’achat. Par exemple, je n’utiliserais pas le nombre de sessions ou le nombre de pages dans une session ou un élément similaire. Ces signaux indirects indiquent la contrepartie, et non l’intention d’achat. N’oubliez pas que l’objectif de ce segment est de déduire l’intention du visiteur pour la visite, et non sa propension.

### Utilisation d’Analytics Workspace pour identifier les signaux de intention d’achat

Le rapport sur les abandons est très utile pour identifier un bon signal qui indique l’intention d’achat. Cherchez un endroit qui indique logiquement l&#39;intention. Vous pouvez confirmer que l’étape indique l’intention lorsque vous constatez un abandon notable allant à cette étape, souvent suivi d’un abandon moins important pour l’étape immédiatement après.

![Image 2](assets/Image-2.png)

Il est également utile d’examiner les taux de conversion associés aux différentes pages de votre site. Cela s’avère particulièrement utile pour identifier les pages qui indiquent l’intention d’achat, mais qui peuvent ne pas être nécessaires pour effectuer un achat (telles que les pages de financement, les pages de configuration des achats, etc.).

![Image 3](assets/Image-3.png)

Enfin, il est important d’inclure toutes les pages entre le début de l’achat et la confirmation d’achat dans votre segment. Les visiteurs peuvent rebondir et rejoindre à nouveau votre flux d’achats à différents moments.

### Exclusion d’autres segments

Rappelez-vous de notre premier article que nos segments d’intention de visite doivent s’exclure mutuellement et être complètement exhaustifs. C&#39;est un refrain que vous entendrez beaucoup dans cette série.

Assurez-vous que votre segment intention d’achat exclut les segments Un et Terminé . Il vous suffit d’exclure les segments Un et Terminé , car les signaux que nous utilisons pour le mode d’achat sont très spécifiques.

Notez que l’exclusion des segments Une et Terminé peut exclure une personne qui accède à nouveau à votre site sur une page de passage en caisse. Ceci est normal. La définition même de Un et Terminé est une page vue, ce qui signifie que même si un visiteur accède à une page de passage en caisse ou l’actualise, sa visite n’a pas progressé, et il n’y a donc aucune expression d’intention d’achat.

### Segment de intention d’achat dans le créateur de segments

La définition de segment pour le mode d’achat est très simple.

À l’aide du conteneur de visites, incluez les pages ou autres actions qui indiquent explicitement une intention d’effectuer un achat. Si vous disposez de plusieurs conditions d’inclusion, veillez à les placer dans un conteneur joint par la condition « Et ».

Ajoutez un conteneur Exclure au segment joint par la condition « Et ». Ajoutez votre définition de segment Merveilles à un accès (Pages vues est égal à 1) au conteneur Exclure .

![Image 4](assets/Image-4.png)

En règle générale, veillez à étiqueter vos conteneurs. Vous serez heureux de l’avoir fait, d’autant plus que nos définitions de segment deviennent plus complexes.

Maintenant que nous avons créé le segment intention d’achat, nous pouvons utiliser le Workspace Qualité des données des intentions de visite pour vérifier que notre segment intention d’achat s’exclut mutuellement avec notre segment Une et Terminé .

![Image 5](assets/Image-5.png)

## Création du segment d’intention de visite de rétention

Dans le secteur des croisières, de nombreux clients viennent sur notre site Web pour gérer une réservation, mais pas nécessairement pour faire un achat. Ils peuvent se rendre sur le site pour entrer des informations de voyage, revoir leur itinéraire, faire des réservations pour le dîner, ou un certain nombre d&#39;autres choses, sans magasiner pour une croisière. Nos clients peuvent également acheter des excursions à terre ou d&#39;autres améliorations à leur expérience. Nous considérons ces améliorations comme faisant partie de la rétention, nous les séparons donc de notre segment Réservation (que nous appelons « Achat » dans cette série de blogs).

Les clients au détail peuvent être en mesure de générer des retours ou de gérer leur programme de fidélité. Les abonnés aux médias ou à la technologie peuvent utiliser le produit. Si votre invité est sur votre site Web pour gérer sa relation avec vous, il s&#39;agit d&#39;une visite de rétention et nous devrions examiner ces signaux. Et si vous fournissez un produit en ligne, comme Médias, Technologie, Services bancaires en ligne ou autres, il existe probablement de nombreux autres types de segments d’intention de visite dont nous ne parlerons pas dans cette série.

Comme pour le segment des intentions d’achat, nous recherchons des indications d’intention très explicites. Pour moi, nous avons toute une section du site consacrée à la gestion d&#39;une croisière, donc il est facile d&#39;identifier ces pages. Cela pourrait être plus complexe pour d&#39;autres entreprises. Recherchez des signaux tels que les connexions, la gestion de compte, les visites des pages d’assistance, etc.

Je dois noter que « Rétention » est un nom un peu bizarre pour cette intention de visite, puisque le visiteur n’est pas sur notre site, « afin que je puisse être retenu en tant que client. » Le maintien en poste est notre intention pour cette visite. Souvenez-vous simplement d’être empathique avec nos clients et de garder une priorité sur le client !

### Utilisation d’Analytics Workspace pour identifier les signaux de intention de rétention

Là encore, Analytics Workspace nous aide à identifier l’intention de rétention. Vous pouvez utiliser les dimensions de pages, de section de site ou de segment personnalisé pour classer vos pages. Recherchez les pages avec des taux de conversion d’achat faibles. Dans notre cas, nous constatons que les pages Enregistrement en ligne et Excursion à terre (Shorex) ont des taux de conversion relativement plus faibles que les autres pages qui sont plus logiquement associées aux achats et aux achats.

![Image 6](assets/Image-6.png)

Il est également recommandé de rechercher des pages à trafic élevé dans Workspace. Analysez la liste des pages à trafic élevé et décidez si elles indiquent une intention de rétention.

## Exclusion d’autres segments

Encore une fois, nos segments d’intention de visite doivent s’exclure mutuellement et être complètement exhaustifs. Si vous n&#39;êtes pas encore fatigué de lire ceci, vous le serez ! Pour notre segment intention de rétention, il est extrêmement important d’exclure les comportements d’intention d’achat.

Pour la plupart d’entre nous, l’intention d’achat et l’intention de conservation ne sont pas des comportements mutuellement exclusifs. Nous avons des invités qui viennent sur le site pour gérer leur prochaine croisière, mais aussi pour réserver leur prochain voyage (merci !). Si vous êtes un restaurant, un visiteur peut vérifier ses points de fidélité puis passer une commande en ligne.

Même si le comportement ne s’exclut pas mutuellement, nos segments doivent être destinés à l’analyse du Parcours client. Nous pouvons créer d’autres segments très intéressants pour analyser le chevauchement entre les comportements d’achat et de fidélité. Mais pour nos besoins actuels, nous avons besoin que ces segments s’excluent mutuellement.

La génération de la demande étant l’un des principaux objectifs du marketing, notre segment Intention de conservation exclura l’intention d’achat. En d’autres termes, si quelqu’un se rend sur notre site pour gérer une croisière, mais indique également son intention de réserver une nouvelle croisière, cette visite ira dans le segment Intention d’achat .

### Segment d’intention de rétention dans le créateur de segments

Nos définitions de segment se font de plus en plus claires. Incluez les visites dans votre segment. Ajoutez vos signaux d’intention de rétention. Pour moi, c&#39;était simple. Si le nom de la page commence par « bge: » (nos pages réservées aux invités), vous êtes dans le segment. J’ai ajouté que le nombre de pages vues est supérieur à un pour une mesure supplémentaire (mais nous exclurons toujours une des merveilles d’accès ci-dessous).

Ajoutez ensuite des conteneurs d’exclusion pour vos visites Guides d’un accès et intention d’achat . Assurez-vous que vos conteneurs sont joints avec la condition « Et ».

![Image 7](assets/Image-7.png)

Une fois de plus, examinez votre Workspace de qualité des données sur les intentions de visite pour vous assurer que vos segments s’excluent mutuellement. Nos segments d’intention de visite prennent joliment forme !

![Image 8](assets/Image-8.png)

À ce stade, nous avons configuré trois de nos cinq segments d’intention de visite. Nous constatons que ces segments s’excluent mutuellement. Dans notre prochain article, nous allons créer les derniers segments sur l’intention de visite, la considération et la sensibilisation, et nos segments seront tous complètement exhaustifs. Une fois nos segments d’intention de visite configurés, nous les rassemblons en segments basés sur les visiteurs que vous trouverez très utiles pour l’analyse et la personnalisation.

## Auteur

Ce document a été rédigé par :

![Aaron Fossum ](assets/aaron-headshot.png)

**Aaron Fossum**, directeur, Analytique numérique

Adobe Analytics Champion
