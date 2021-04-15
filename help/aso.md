---
title: ASO
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: ht
source-wordcount: '198'
ht-degree: 100%

---


# ASO {#aso}

AEM System Overview (vue d’ensemble du système AEM)

## Arrière-plan {#background}

`ASO` identifie des informations générales sur l’instance AEM. Chaque recherche fournit une valeur d’un type particulier d’informations système.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `aem.version` : version d’AEM.
* `aem.product` : détection de l’utilisation d’un produit AEM (Commerce, Forms, etc.).
* `node.count` : nombre approximatif de nœuds d’un certain type (Page, Ressource, etc.).
* `node.store` : type d’implémentation du magasin de nœuds (SegmentNodeStore, DocumentNodeStore).
* `data.store` : type d’implémentation de l’entrepôt de données (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task` : tâche de maintenance.
* `slow.query` : requête lente.

## Enjeux et risques possibles {#implications-and-risks}

* La version d’AEM, le nombre de nœuds et les types d’implémentation du magasin de nœuds et de l’entrepôt de données sont fournis à titre informatif.
* L’application personnalisée peut s’appuyer sur des produits ou des fonctionnalités qui ne sont pas disponibles dans AEM as a Cloud Service.
* La mise à niveau avec des fonctionnalités non prises en charge peut entraîner l’échec de la mise à niveau et une application non fonctionnelle.

## Solutions possibles {#solutions}

* Les mises à niveau d’AEM avec des produits ou des fonctionnalités non pris en charge ne sont pas recommandées et peuvent ne pas être prises en charge.
* Consultez les [notes de mise à jour](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr) pour en savoir plus sur les dernières modifications apportées à AEM as a Cloud Service.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
