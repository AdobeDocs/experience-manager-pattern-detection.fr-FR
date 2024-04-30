---
title: ASO
description: Page d’aide sur le code de la détection des motifs.
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 67%

---

# ASO {#aso}

AEM System Overview (vue d’ensemble du système AEM)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="AEM System Overview (vue d’ensemble du système AEM)"
>abstract="Le code ASO identifie des informations d’ordre générale concernant l’instance AEM. Chaque recherche fournit une valeur d’un type particulier d’information système qui peut vous aider dans la restructuration et planification de votre migration."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Notes de mise à jour"

`ASO` Identifie les informations générales sur l’instance AEM. Chaque recherche fournit une valeur d’un type particulier d’informations système.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `aem.version` : version d’AEM.
* `aem.product`: détection de l’utilisation d’un produit AEM (Commerce, Forms, etc.).
* `node.count`: nombre approximatif de noeuds d’un certain type (Page, Ressource, etc.) et total général des noeuds.
* `node.store` : type d’implémentation de l’entrepôt de nœuds (SegmentNodeStore, DocumentNodeStore) et sa taille.
* `data.store` : type d’implémentation de l’entrepôt de données (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task` : tâche de maintenance.
* `slow.query` : requête lente.
* `group.membership`: nombre d’utilisateurs et de sous-groupes ( membres directs/déclarés uniquement ) dans un groupe.
* `cqtag.count` : nombre de ressources avec balisage CQ.
* `smarttag.count` : nombre de ressources avec balisage intelligent.
* `ccom.version` : version du package de composants principaux.
* `instance.type` : type d’instance AEM (auteur, publication).
* `unprocessed.asset.count` : nombre de ressources non traitées.
* `vanity.url.count` : nombre d’URL de redirection vers un microsite.
* `index.size` : taille totale de l’index Lucene pouvant être migré.
* `workflow.count` : nombre de workflows de création en cours d’exécution et périmés.
* `jvm.arguments` : arguments JVM ajoutés à la ligne de commande lors du démarrage d’AEM.

## Enjeux et risques possibles {#implications-and-risks}

* La version AEM, le nombre de noeuds, l’appartenance au groupe, le magasin de noeuds, les types d’implémentation de l’entrepôt de données, le nombre de balises CQ, le nombre de balises intelligentes, la version du composant principal, le type d’instance AEM et le nombre de ressources non traitées sont fournis à titre d’information.
* Un nombre élevé d’URL de redirection vers un microsite (> 1 000) peut surcharger le Dispatcher et les serveurs de publication de requêtes lourdes.
* L’application personnalisée peut s’appuyer sur des produits ou des fonctionnalités qui ne sont pas disponibles dans AEM as a Cloud Service.
* La mise à niveau avec des fonctionnalités non prises en charge peut entraîner l’échec de la mise à niveau et une application non fonctionnelle.
* Un nombre élevé de workflows de création en cours d’exécution ou périmés peut dégrader les performances.
* Des requêtes lentes peuvent réduire les performances du système.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Guide de mise en œuvre"
>abstract="Les informations exposées par le biais du code ASO fournissent des informations générales pour votre environnement AEM, notamment la version, les modules complémentaires de produit et les informations au niveau du système. Examinez-les pour rechercher des fonctionnalités ou des produits non pris en charge dans AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Les mises à niveau AEM avec des produits ou des fonctionnalités non pris en charge ne sont pas recommandées et peuvent ne pas être prises en charge.
* Les ressources non traitées doivent être traitées et la variable `dam:assetState` sur la propriété `jcr:content` du noeud de la ressource doit être défini sur &quot;traité&quot;. Vous pouvez également supprimer ces ressources du jeu de migration avant de migrer vers AEMaaCS.
* Les URL de redirection vers un microsite peuvent être remplacées à l’aide d’Apache Rewrites.
* Consultez la [documentation](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/bestpractices/troubleshooting-slow-queries) pour résoudre les problèmes liés aux requêtes lentes.
* Voir [notes de mise à jour](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current) si vous souhaitez en savoir plus sur les dernières modifications apportées à AEM as a Cloud Service.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
