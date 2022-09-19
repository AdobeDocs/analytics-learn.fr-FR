---
title: Télécharger le guide d’implémentation d’Adobe Analytics
description: Le document des exigences commerciales (communément appelé BRD) revêt un caractère essentiel. Les principaux intervenants, les utilisateurs professionnels et techniques participent d’ordinaire à son élaboration. Il vous permet de documenter tous les KPI souhaités, les exigences en matière de création de rapports et tout point de données que vous souhaitez observer une fois l’implémentation d’Adobe Analytics terminée.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10530.jpg
kt: 10530
exl-id: aab53a12-3f11-49c9-aba4-dc926bcf776b
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: tm+mt
source-wordcount: '1805'
ht-degree: 100%

---

# Télécharger le guide d’implémentation d’Adobe Analytics

Avant de commencer, [téléchargez le guide](assets/aa-implementation-playbook.xlsx).

## Onglet Exigences commerciales

**QUOI :** le document sur les exigences commerciales (communément appelé BRD) revêt un caractère essentiel. Les principaux intervenants, les utilisateurs professionnels et techniques participent d’ordinaire à son élaboration. Il vous permet de documenter tous les KPI souhaités, les exigences en matière de création de rapports et tout point de données que vous souhaitez observer une fois l’implémentation d’Adobe Analytics terminée.

**POURQUOI :** ce document sert de point de départ pour la documentation qui suit (SDR, spécification technique, etc.) et constitue une source commune de vérité d’un état final convenu d’Adobe Analytics. Ce document rassemble les réflexions des différentes équipes au sein de l’organisation afin d’établir une ligne directrice en vue de votre implémentation ou de son amélioration.

**COMMENT :** les utilisateurs professionnels finaux d’Adobe Analytics se chargent généralement de documenter les exigences commerciales. Toutefois, il est important d’obtenir des commentaires de la part des utilisateurs techniques, car des défis techniques peuvent se présenter et certains points de données peuvent demander plus d’efforts que d’autres, ce qui permet d’établir des priorités.

Demandez-vous ceci : « Quels indicateurs voulons-nous suivre sur notre site ? », « Quels points de données priment pour moi à des fins de création de rapports ? » et, plus important encore, « Comment ces points de données vont-ils me permettre de prendre des décisions éclairées ? ». Il est important de s’assurer que chaque exigences commerciale de votre entreprise possède un point de données correspondant. Ainsi, vous pouvez prendre des décisions commerciales éclairées. Par exemple, il peut être tentant de vouloir suivre chaque clic sur votre site, mais au bout du compte, les insights que vous en tirez sont-ils réellement instructifs ?

Commencez par remplir la colonne C de la copie d’écran ci-dessous (Exigences commerciales). Il devrait s’agir de quelque chose comme « Nombre de recherches internes effectuées sur notre site » ou « Quel spot de campagne interne est le plus efficace en termes d’impressions ». Ensuite, revenez en arrière remplissez la colonne B (Catégorie) et regroupez les besoins dans des catégories telles que « Recherche » ou « Promotion interne ». Celles-ci doivent correspondre parfaitement à vos sections de spécifications techniques.

Vous devez également indiquer si vous pensez que l’utilisation d’une eVar, d’un événement, d’une prop ou d’une combinaison de ceux-ci pour assurer le suivi vous permettra d’obtenir les résultats escomptés.

Enfin, la colonne Statut de l’implémentation servira à vérifier le statut d’avancement des ajouts à votre site.

![Document des exigences commerciales](assets/brd-template.png)

## Onglet Carte des variables (document de balisage/SDR)

**QUOI :** un document de balisage (communément appelé SDR) est un document de prime importance pour les utilisateurs techniques et professionnels d’Adobe Analytics. Il répertorie toutes les variables utilisées par les suites de rapports, ainsi que tous les détails pertinents concernant les paramètres de la variable, sa méthode d’implémentation et sa finalité dans les rapports. À l’instar de votre document sur les propriétés, ce document Excel doit être régulièrement mis à jour et bien ordonné. Une personne dédiée doit se charger de le tenir à jour au fur et à mesure des améliorations apportées au balisage ou des changements d’implémentation.

**POURQUOI :** ce document servira à plusieurs fins, mais il se destine principalement à :

* Aider toute personne qui découvre votre implémentation (nouvel employé, propriétaire d’entreprise cherchant à mieux comprendre les rapports disponibles, etc.). Celle-ci disposera d’un panorama complet de toutes les variables implémentées et de leur finalité. Ainsi, chacun peut se familiariser avec votre configuration d’Adobe Analytics à son gré et selon ses besoins.
* Pour le propriétaire du produit Adobe Analytics ou l’utilisateur technique, ce document sert de rappel de la manière dont les autres variables sont configurées et des variables disponibles pour l’ajout d’une nouvelle dimension.

**COMMENT :** commencez par répertorier dans un document Excel toutes les variables Adobe prêtes à l’emploi (page, produit, zone géographique, etc.), ainsi que les eVars, props, événements et variables de liste. Celui-ci doit comporter un onglet par site/suite de rapports.
Pour chacune de ces dimensions, j’ajoute les colonnes suivantes :
* **Nom :** donnez un nom simple et court, qui décrit bien sa finalité. Le nom de la variable doit être suffisamment explicite pour qu’un nouvel utilisateur puisse comprendre directement ce qu’elle cherche à accomplir.
* **Description :** fournit plus de détails sur la finalité de la variable et les données qu’elle suit. Personnellement, je n’attache guère d’importance à ce champ. Je me contente de le faire correspondre à la description utilisée dans l’interface. J’essaie d’éviter au maximum que mes utilisateurs aient à consulter le document de balisage. À cette fin, lorsqu’une nouvelle dimension est configurée sur le serveur principal de l’administrateur, j’ajoute la même description à cet endroit. De cette façon, l’utilisateur peut cliquer sur l’icône d’information directement dans Workspace pour comprendre ce qu’est une dimension. Nul besoin de lui sortir un document Excel !

![URL de page simplifiée](assets/page-url-simplified.png)

* **Code :** code du serveur principal qui définit la valeur. Il peut s’agir du champ de la couche de données de la page ou vous pouvez indiquer que cette opération est effectuée par une règle Launch, une règle de traitement, etc.
* **Rapports de classification :** signalez tout rapport de classification en cours de réalisation avec l’importateur de classifications ou le créateur de règles de classification.
* **Portée de la solution :** il peut être utile de répertorier toutes les propriétés (du moins celles qui utilisent plus que des variables standard) en petites colonnes et d’ajouter une coche pour chaque dimension configurée sur cette propriété. Vous pouvez ainsi filtrer facilement une propriété spécifique et visualiser en un clin d’œil où une dimension particulière est configurée.
* **Configuration :** paramètres de l’interface d’administration pour chaque variable (par exemple, pour les eVars : expiration, attribution, marchandisage, etc.)

Copie d’écran d’un exemple de document SDR :
![Exemple de document SDR](assets/sample-sdr.png)

Il est également recommandé d’utiliser ce document de balisage pour garder une trace de toutes les variables libres et de celles qui sont « inutiles ». Lorsqu’une dimension n’est plus utile, le développeur a généralement besoin d’un certain temps pour la supprimer. Même après sa suppression, un caching peut se produire. Vous pouvez également réaliser que la dimension était définie ailleurs. Nettoyer les dimensions n’est pas facile et nécessite souvent de la patience. Voici quelques conseils pour garder tout ce qui est inutile caché afin que vos utilisateurs ne soient pas perdus tout en faisant le suivi.

* Toutes les dimensions/événements non utilisés sont « libres » ou « en cours de suppression ».
   * Si la dimension contient des valeurs indésirables au cours des 90 derniers jours, elle est « en cours de suppression ».
   * Si la dimension est libre et quitte de tout problème pendant au moins les 90 derniers jours, elle est « libre ».
   * Marquez-les comme telles sous « Nom » dans le document de balisage, afin de pouvoir facilement les filtrer. Je ne les coche pas dans le document de balisage (filtre de données Excel) afin que les utilisateurs ne les voient pas.
   * Marquez-les comme nom d’eVar dans l’interface afin que les utilisateurs ne les trouvent pas dans une recherche (par exemple « (v6) ») et supprimez la description dans l’interface.
* Ainsi, lorsqu’une nouvelle dimension est nécessaire, vous pouvez facilement utiliser le filtre « libre » dans la colonne « Nom » pour trouver une dimension adaptée.
* Pour les dimensions et événements « en cours de suppression », je vous recommande de suivre ceux-ci à l’aide de Workspace :
   * Créez un projet visible par les administrateurs uniquement avec 3 tableaux : eVars, props et événements. J’utilise « instances » pour les eVars spécifiques, et pour les props, je crée des segments d’accès avec « prop5 existe », par exemple.
   * Définir la date sur Les 90 derniers jours
   * Utilisez les lignes ci-dessus comme lignes dans les 3 tableaux, ainsi que des occurrences.
   * Dès que quelque chose atteint « 0 », je le marque comme « libre » dans le document de balisage et je le supprime du projet Workspace.

De cette façon, vos données sont toujours propres et vous avez une idée claire de ce qui est inutilisable.

![Aperçu des variables et événements](assets/variables-and-events-overview.png)

## Onglet Propriétés

**QUOI :** un document de propriétés doit répertorier toutes vos propriétés numériques (sites web, applications mobiles, autres outils (chat, commentaires, etc.)), que ces propriétés soient balisées ou non avec Adobe Analytics. Cela doit servir de document dynamique et centralisé pour les utilisateurs professionnels et technologiques.

**POURQUOI :** vous obtenez ainsi une vue claire du parcours de votre utilisateur sur toutes vos propriétés numériques, ainsi que de ce qu’Adobe Analytics couvre et ne couvre pas afin que vous puissiez commencer à donner la priorité à l’ajout de balisage à toutes les propriétés qui en sont dépourvues. En exposant ainsi votre écosystème numérique, vous pouvez identifier les opportunités potentielles dans la stratégie de balisage pour obtenir une vue complète du parcours de votre utilisateur. Par exemple : avez-vous besoin d’une suite de rapports globale pour effectuer le suivi sur plusieurs domaines/sites ? Une remise d’identifiant visiteur est-elle nécessaire entre les domaines ou l’application vers une expérience hybride ? Les filtres URL internes doivent-ils être mis à jour pour le suivi inter-domaines ?

**COMMENT :** identifiez le propriétaire du document afin de fournir la gouvernance et une source unique de responsabilité pour la gestion des mises à jour.
Dans l’onglet Propriétés, répertoriez les éléments suivants :
* **Nom de la propriété :** il peut s’agir d’un domaine, d’un sous-domaine, d’un nom d’application, etc. Même dans le même domaine, si certaines parties de celui-ci sont gérées séparément (comme par une autre équipe ou une technologie différente), elles doivent être séparées.
* **Lien (URL)** vers la propriété lorsque disponible.
* **Propriétaire et contacts :** répertoriez le ou les contacts principaux de la propriété.
* **Méthode de balise :** nombre d’entre nous avons différentes méthodes de code et implémentations en place (Launch, fichiers JS, AEP, etc.). Si nécessaire, vous pouvez ventiler cette opération davantage (par exemple par version de code ou système de gestion des balises), mais cette opération a pour but de suivre toutes vos méthodes et versions de code, où le code doit être mis à jour et comment il doit être géré. Si vous utilisez Adobe Launch, indiquez le nom de la propriété Launch.

N’oubliez pas d’inclure toutes les propriétés numériques, même si elles ne sont pas balisées avec Adobe Analytics. Cela vous aidera à comprendre votre paysage numérique et la manière dont vos utilisateurs interagissent avec toutes vos propriétés.

Il est recommandé de garder ce document aussi simple que possible et de ne pas y ajouter trop d’informations afin qu’il reste facile à interpréter par les différentes parties de l’organisation. Les équipes d’analyse connaissent souvent mieux le paysage numérique que n’importe quelle autre équipe. Par conséquent, ce document est souvent utilisé par d’autres équipes et cadres pour obtenir une vue d’ensemble approfondie.

>[!TIP]
>
>Créez une dimension de nom/propriété de site dans Adobe Analytics. Avoir une dimension dédiée (généralement une eVar) dans Adobe Analytics qui identifie le nom du site/de l’application permet de segmenter, de résoudre les problèmes, de créer des suites de rapports virtuelles, etc. Les avantages sont infinis, en particulier lorsque vous combinez plusieurs sites dans une seule suite de rapports (globale). La clé consiste à s’assurer que vos équipes de développement définissent toujours cette valeur dans la dimension des propriétés, y compris tous les chargements de page (s.t calls/trackState) et tous les événements personnalisés (s.tl calls/trackAction). Les règles de traitement peuvent s’avérer un outil précieux pour vous aider à définir correctement et de manière cohérente ces valeurs.

[Regardez cette vidéo de Doug Moore](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=fr){target=&quot;_blank&quot;} pour plus d’informations sur le remplissage du guide d’implémentation.

## Auteurs

Ce document a été rédigé par :

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, responsable de la plateforme Digital Analytics chez NortonLifeLock
Adobe Analytics Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, conseillère principale chez Adobe
