---
title: ASO
description: Page d’aide sur le code de la détection des motifs
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
translation-type: tm+mt
source-git-commit: 449288e567adda9998a89e0ad5198fd5a4e93f35
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 71%

---

# ASO {#aso}

AEM System Overview (vue d’ensemble du système AEM)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="AEM System Overview (vue d’ensemble du système AEM)"
>abstract="Le code ASO identifie des informations générales sur l’instance AEM. Chaque recherche fournit une valeur d’un type particulier d’informations système qui peut vous aider à planifier votre migration et à restructurer vos efforts."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM en tant que Cloud Service - Notes de mise à jour"

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

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Guide de mise en oeuvre"
>abstract="Les informations exposées par le biais du code ASO fournissent des informations générales pour votre environnement AEM, y compris la version, les modules complémentaires de produit, les informations au niveau du système. Ces informations doivent être examinées pour tous les produits ou fonctionnalités non pris en charge dans AEM en tant que Cloud Service. Contactez le Support aux Adobes pour obtenir de l&#39;aide et des éclaircissements."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Les mises à niveau d’AEM avec des produits ou des fonctionnalités non pris en charge ne sont pas recommandées et peuvent ne pas être prises en charge.
* Consultez les [notes de mise à jour](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr) pour en savoir plus sur les dernières modifications apportées à AEM as a Cloud Service.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
