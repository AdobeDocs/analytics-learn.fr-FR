---
title: Téléchargement du manuel de mise en oeuvre Adobe Analytics
description: Un document sur les exigences de l’entreprise (communément appelé BRD) est un élément de documentation très important sur lequel les principaux intervenants, les utilisateurs professionnels et les utilisateurs techniques voudront collaborer. Il permet de documenter tous les indicateurs clés de performance souhaités, les exigences de création de rapports et tout point de données que vous souhaitez voir une fois votre mise en oeuvre AA terminée.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10530.jpg
kt: 10530
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '1805'
ht-degree: 0%

---


# Téléchargement du manuel de mise en oeuvre Adobe Analytics

Avant de commencer, [télécharger le playbook](assets/aa-implementation-playbook.xlsx).

## Onglet Exigences métier

**QUOI :** Un document sur les exigences de l’entreprise (communément appelé BRD) est un élément de documentation très important sur lequel les principaux intervenants, les utilisateurs professionnels et les utilisateurs techniques voudront collaborer. Il vous permet de documenter tous les indicateurs clés de performance souhaités, les exigences en matière de création de rapports et tout point de données que vous souhaitez voir une fois votre mise en oeuvre Adobe Analytics (AA) terminée.

**POURQUOI :** Cela sert de point de départ pour la documentation qui suit (DTS, spécification technique, etc.) et est une source commune de vérité pour un état final convenu de AA. Ce document organise les réflexions des équipes au sein de l’organisation afin de former une orientation pour aller de l’avant avec la création ou l’amélioration de votre mise en oeuvre.

**COMMENT :** La documentation des besoins de l’entreprise est généralement réalisée par les utilisateurs finaux d’AA, mais il est important d’obtenir des commentaires des utilisateurs techniques, car il peut y avoir des problèmes techniques à noter et certains points de données peuvent nécessiter plus d’efforts que d’autres, ce qui contribue à la définition des priorités.

Demandez-vous, &quot;quelles sont les choses que nous voulons suivre sur notre site&quot;, &quot;quels points de données seront importants pour moi dans le cadre de la création de rapports&quot; et, plus important encore, &quot;comment ces points de données vont-ils influencer les décisions&quot;. Il est important de s’assurer que chacun de vos besoins commerciaux correspond à un point de données qui peut être utilisé pour informer les décisions commerciales. Par exemple, il peut être tentant de suivre chaque clic sur votre site, mais en fin de compte, quelles sont les informations que vous obtenez de ces rapports ?

Renseignez tout d’abord la colonne C de la capture d’écran ci-dessous (Exigences de l’entreprise). Il doit s’agir par exemple du &quot;Nombre de recherches internes effectuées sur notre site&quot; ou de &quot;Quel emplacement de campagne interne est le plus efficace en termes d’impressions&quot;. Après avoir renseigné ce niveau de détail, vous pouvez revenir en arrière et remplir la colonne B (Catégorie) et regrouper les exigences en catégories telles que &quot;Recherche&quot; ou &quot;Promotion interne&quot; qui devraient correspondre parfaitement avec vos sections de spécification technique.

Vous indiquez également si vous pensez que l’utilisation d’un eVar, d’un événement, d’une prop ou d’une combinaison permettra d’atteindre ce dont vous souhaitez effectuer le suivi.

Enfin, la colonne État de l’implémentation servira de vérification d’état lorsque vous commencez à ajouter des éléments à votre site.

![Document des besoins de l’entreprise](assets/brd-template.png)

## Onglet Carte des variables (balisage de document/SDR)

**QUOI :** Un document de balisage (communément appelé DTS) est une documentation essentielle qui est utile pour les utilisateurs techniques et professionnels d’AA. Elle répertorie toutes les variables utilisées par les suites de rapports, ainsi que tous les détails pertinents pour les paramètres de variable, la manière dont la variable est implémentée et son objectif dans les rapports. Tout comme votre document de propriétés, il doit s’agir d’un document Excel vivant et bien géré, dont le responsable est de le tenir à jour au fur et à mesure de l’introduction d’améliorations du balisage ou de modifications de mise en oeuvre.

**POURQUOI :** Ce document aura de nombreux usages, mais les plus importants sont les suivants :

* Pour toute personne qui découvre votre implémentation (nouvelle embauche, propriétaire d’entreprise cherchant à mieux comprendre les rapports disponibles, etc.) ce document donne une vue d’ensemble optimale de toutes les variables implémentées et de leur objectif afin que les individus puissent se servir eux-mêmes en termes d’apprentissage de votre configuration AA.
* Pour le propriétaire/l’utilisateur technologique d’un produit AA, ce document servira de rappel de la configuration d’autres variables et des variables disponibles lors de l’ajout d’une nouvelle dimension.

**COMMENT :** Commencez par répertorier dans un document Excel toutes les variables d’Adobe d’usine (page, produit, zone géographique, etc.), ainsi que les eVars, props, événements et variables de liste. Celui-ci doit comporter un onglet par site/suite de rapports.
Pour chacune de ces dimensions, j’ajoute les colonnes suivantes :
* **Nom :** Donnez un nom simple et court qui peut être compris par la plupart des utilisateurs. Cela doit être suffisamment intuitif pour qu’un nouvel utilisateur puisse le sélectionner et comprendre la variable à capturer.
* **Description :** Plus de détails sur la variable utilisée et les données suivies. Je garde ce court et simple et je le fais correspondre à la description utilisée dans l&#39;interface. Idéalement, je ne veux pas que mes utilisateurs aient besoin de consulter le document de balisage. Ainsi, lorsqu’une nouvelle dimension est configurée sur le serveur principal d’administration, j’y ajoute la même description. Ainsi, l’utilisateur peut appuyer directement sur l’icône d’information dans Workspace pour comprendre ce qu’est une dimension. Il n’est pas nécessaire d’extraire un document Excel.

![URL de page simplifiée](assets/page-url-simplified.png)

* **Code :** Le code du serveur principal qui définit la valeur. Il peut s’agir du champ de la couche de données de la page ou vous pouvez signaler que cette opération s’effectue avec une règle Launch, une règle de traitement, etc.
* **Rapports de classification :** Appeler tout rapport de classification réalisé avec l’importateur de classifications ou le créateur de règles de classification
* **Portée de la solution :** Je trouve utile de répertorier toutes les propriétés (au moins celles qui utilisent plus que les variables standard) dans de petites colonnes et d’ajouter une coche pour chaque dimension définie sur cette propriété. Cela vous permet de filtrer facilement une propriété spécifique et de voir rapidement où une dimension particulière est définie.
* **Configuration :** Paramètres de l’interface utilisateur d’administration pour chaque variable (c’est-à-dire pour les eVars - expiration, attribution, marchandisage, etc.)

Capture d&#39;écran d&#39;un exemple de DTS :
![Exemple de SDR](assets/sample-sdr.png)

Il est également recommandé d’utiliser ce document de balisage pour effectuer le suivi des variables libres et des variables &quot;indésirables&quot;. Lorsqu’une dimension n’est plus utile, le développement a généralement besoin de temps pour la supprimer. Même après cela, la mise en cache peut se produire, ou vous pouvez réaliser que la dimension était également définie ailleurs. Nettoyer les dimensions n&#39;est pas facile, et nécessite souvent de la patience. Voici quelques conseils pour garder votre malbouc caché sous le lit afin que vos utilisateurs ne se perdent pas tout en en suivant les traces.

* Toutes les dimensions/événements non utilisés sont &quot;libres&quot; ou &quot;en cours de suppression&quot;
   * Si la dimension contient des valeurs &quot;indésirables&quot; au cours des 90 derniers jours, elle est &quot;en cours de suppression&quot;.
   * Si la dimension est libre et claire pendant au moins les 90 derniers jours, elle est &quot;libre&quot;
   * Marquez-les comme telles sous &quot;Nom&quot; dans le document de balisage, afin de pouvoir facilement les filtrer. Je ne les coche pas dans le document de balisage (filtre de données Excel) afin que les utilisateurs ne les voient pas.
   * Marquez-les comme nom d’eVar dans l’interface afin que les utilisateurs ne les trouvent pas dans une recherche (c.-à-d. &#39;(v6)&#39;) et supprimez la description dans l’interface
* Ainsi, lorsqu’une nouvelle dimension est nécessaire, vous pouvez facilement filtrer &quot;gratuit&quot; dans la colonne &quot;Nom&quot; pour trouver une dimension propre à utiliser.
* Pour les dimensions et événements &quot;en cours de suppression&quot;, je vous recommande de suivre ceux-ci à l’aide de Workspace :
   * Créez un projet visible par les administrateurs uniquement avec 3 tableaux : eVars, props et événements. J’utilise &quot;instances&quot; pour les eVars spécifiques, et pour les props, je crée des segments d’accès avec &quot;prop5 exists&quot;, par exemple.
   * Définir la date sur les 90 derniers jours
   * Utilisez les lignes ci-dessus comme lignes dans les 3 tableaux, ainsi que des occurrences
   * Dès que quelque chose atteint &quot;0&quot;, je le marque comme &quot;gratuit&quot; dans le document de balisage et je le supprime du projet Workspace.

De cette façon, vos données sont toujours propres, et vous avez une idée claire de votre pourri.

![Variables et événements - Aperçu](assets/variables-and-events-overview.png)

## Onglet Propriétés

**QUOI :** Un document de propriétés doit répertorier toutes vos propriétés numériques (sites web, applications mobiles, autres outils (chat, commentaires, etc.), que ces propriétés soient balisées ou non avec Adobe Analytics. Cela devrait servir de document vivant et centralisé pour les utilisateurs professionnels et technologiques.

**POURQUOI :** Vous obtiendrez ainsi une vue claire de l’parcours de votre utilisateur sur toutes vos propriétés numériques, ainsi que de ce qu’Adobe Analytics fait et ne couvre pas afin que vous puissiez commencer à donner la priorité à l’ajout de balisage à toutes les propriétés où il manque. En exposant ainsi votre écosystème numérique, vous pouvez identifier les opportunités potentielles dans la stratégie de balisage pour obtenir une vue complète du parcours de votre utilisateur. Par exemple : avez-vous besoin d’une suite de rapports globale pour effectuer le suivi sur plusieurs domaines/sites ? Une remise d’identifiant visiteur est-elle nécessaire entre les domaines ou l’application vers une expérience hybride ? Les filtres URL internes doivent-ils être mis à jour pour le suivi inter-domaines ?

**COMMENT :** Identifiez le propriétaire du document afin de fournir la gouvernance et une source unique de responsabilité pour la gestion des mises à jour.
Dans l’onglet Propriétés, listez les éléments suivants :
* **Nom de la propriété :** Il peut s’agir d’un domaine, d’un sous-domaine, d’un nom d’application, etc. Même dans le même domaine, si certaines parties de celui-ci sont gérées séparément (comme par une autre équipe ou une technologie différente), elles doivent être séparées.
* **Lien (URL)** à la propriété lorsque disponible
* **Propriétaire et contacts :** Répertorier le ou les contacts principaux de la propriété
* **Méthode de balise :** Nombre d’entre nous avons différentes méthodes de code et mises en oeuvre en place (Launch, fichiers JS, AEP, etc.). Si nécessaire, vous pouvez ventiler cette opération davantage (par version de code ou système de gestion des balises, par exemple), mais cette opération a pour but de suivre toutes vos méthodes et versions de code, où le code doit être mis à jour et comment il doit être géré. Si vous utilisez Adobe Launch, indiquez le nom de la propriété Launch.

N’oubliez pas d’inclure toutes les propriétés numériques, même si elles ne sont pas balisées avec Adobe Analytics. Cela vous aidera à comprendre votre paysage numérique et la manière dont vos utilisateurs interagissent avec toutes vos propriétés.

Il est recommandé de garder ce document aussi simple que possible et de ne pas le consigner avec trop d’informations afin qu’il reste facile à interpréter par les différentes parties de l’organisation. Les équipes d’Analytics connaissent souvent mieux le paysage numérique que n’importe quelle autre équipe. Par conséquent, ce document est souvent utilisé par d’autres équipes et cadres pour fournir une vue d’ensemble approfondie.

>[!TIP]
>
>Créez une dimension de nom/propriété de site dans Adobe Analytics. Avoir une dimension dédiée (généralement un eVar) dans Adobe Analytics qui identifie le nom du site/de l’application permet de segmenter, de résoudre les problèmes, de créer des suites de rapports virtuelles, etc. Les avantages sont infinis, en particulier lorsque vous combinez plusieurs sites dans une seule suite de rapports (globale). La clé consiste à s’assurer que vos équipes de développement définissent toujours cette valeur dans la dimension des propriétés, y compris tous les chargements de page (s.t calls/trackState) et tous les événements personnalisés (s.tl calls/trackAction). Les règles de traitement peuvent s’avérer un outil précieux pour vous aider à définir correctement et de manière cohérente ces valeurs.

[Regardez cette vidéo de Doug Moore](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html){target=&quot;_blank&quot;} pour plus d’informations sur le remplissage du manuel d’implémentation.

## Auteurs

Ce document a été co-écrit par :

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, responsable de la plateforme Digital Analytics chez NortonLifeLock Champion Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, conseillère principale chez Adobe
