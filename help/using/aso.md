---
title: ASO
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 95%

---

# ASO {#aso}

AEM System Overview (vue d’ensemble du système AEM)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="AEM System Overview (vue d’ensemble du système AEM)"
>abstract="Le code ASO identifie des informations d’ordre générale concernant l’instance AEM. Chaque recherche fournit une valeur d’un type particulier d’information système qui peut vous aider dans la restructuration et planification de votre migration."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr" text="AEM as a Cloud Service – Notes de mise à jour"

`ASO` identifie des informations générales sur l’instance AEM. Chaque recherche fournit une valeur d’un type particulier d’informations système.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `aem.version` : version d’AEM.
* `aem.product` : détection de l’utilisation d’un produit AEM (Commerce, Forms, etc.).
* `node.count` : nombre approximatif de nœuds d’un certain type (Page, Ressource, etc.) et le total général des nœuds.
* `node.store` : type d’implémentation de l’entrepôt de nœuds (SegmentNodeStore, DocumentNodeStore) et sa taille.
* `data.store` : type d’implémentation de l’entrepôt de données (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task` : tâche de maintenance.
* `slow.query` : requête lente.
* `group.membership` : nombre d’utilisateurs et de sous-groupes (membres directs/déclarés uniquement) dans un groupe.
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

* La version d’AEM, le nombre de nœuds, l’appartenance à un groupe, le magasin de nœuds, les types d’implémentation du magasin de données, le nombre de balises CQ et de balises intelligentes, la version des composants principaux, le type d’instance AEM et le nombre de ressources non traitées sont fournis à titre d’information.
* Un nombre élevé d’URL de redirection vers un microsite (> 1 000) peut surcharger le Dispatcher et les serveurs de publication de requêtes lourdes.
* L’application personnalisée peut s’appuyer sur des produits ou des fonctionnalités qui ne sont pas disponibles dans AEM as a Cloud Service.
* La mise à niveau avec des fonctionnalités non prises en charge peut entraîner l’échec de la mise à niveau et une application non fonctionnelle.
* Un nombre élevé de workflows de création en cours d’exécution ou périmés peut dégrader les performances.
* Des requêtes lentes peuvent réduire les performances du système.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Guide de mise en œuvre"
>abstract="Les informations exposées par le biais du code ASO fournissent des informations générales sur votre environnement AEM, parmi lesquelles sa version, les modules complémentaires de produit et les informations au niveau du système. Ces informations doivent être examinées pour tous les produits ou fonctionnalités non pris en charge dans AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Les mises à niveau d’AEM avec des produits ou des fonctionnalités non pris en charge ne sont pas recommandées et peuvent ne pas être prises en charge.
* Les ressources non traitées doivent être traitées et la propriété dam:assetState du nœud jcr:content de la ressource doit être définie sur « processed » ou vous devez supprimer ces ressources du jeu de migration avant de migrer vers AEMaaCS.
* Les URL de redirection vers un microsite peuvent être remplacées à l’aide d’Apache Rewrites.
* Voir [documentation](https://experienceleague.adobe.com/docs/experience-manager-65/developing/bestpractices/troubleshooting-slow-queries.html?lang=fr) pour résoudre les problèmes liés aux requêtes lentes.
* Consultez les [notes de mise à jour](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr) pour en savoir plus sur les dernières modifications apportées à AEM as a Cloud Service.
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
