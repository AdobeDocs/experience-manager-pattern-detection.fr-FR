---
title: ASO
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 4%

---


# ASO {#aso}

Présentation AEM système

## Arrière-plan {#background}

`ASO` identifie des informations générales sur l’instance AEM. Chaque recherche fournit une valeur d&#39;un type particulier d&#39;informations système.

Les sous-types permettent d’identifier différents types d’informations :

* `aem.version`: Version AEM.
* `aem.product`: Détection de l&#39;utilisation d&#39;un produit AEM (Commerce, Forms, etc.).
* `node.count`: Nombre approximatif de noeuds d’un certain type (Page, Ressource, etc.).
* `node.store`: Type d’implémentation de la banque de noeuds (SegmentNodeStore, DocumentNodeStore).
* `data.store`: Type d&#39;implémentation du magasin de données (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Tâche de maintenance.
* `slow.query`: Une requête lente.

## Incidences possibles et risques {#implications-and-risks}

* La version AEM, le nombre de noeuds et les types d’implémentation de la banque de noeuds et de la banque de données sont fournis à titre d’information.
* L’application personnalisée peut s’appuyer sur des produits ou des fonctionnalités qui ne sont pas disponibles dans AEM en tant que Cloud Service.
* La mise à niveau avec des fonctionnalités non prises en charge peut entraîner l’échec de la mise à niveau et l’échec de l’application.

## Solutions possibles {#solutions}

* Les mises à niveau AEM avec des produits ou des fonctionnalités non pris en charge ne sont pas recommandées et peuvent ne pas être prises en charge.
* Consultez les [notes de mise à jour](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr) pour en savoir plus sur les dernières modifications apportées à l&#39;AEM en tant que Cloud Service.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
