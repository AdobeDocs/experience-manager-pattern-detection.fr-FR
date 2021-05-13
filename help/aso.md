---
title: ASO
description: Page d’aide sur le code de la détection des motifs
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
translation-type: ht
source-git-commit: 449288e567adda9998a89e0ad5198fd5a4e93f35
workflow-type: ht
source-wordcount: '300'
ht-degree: 100%

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
>title="Guide de mise en œuvre"
>abstract="Les informations exposées par le biais du code ASO fournissent des informations générales sur votre environnement AEM, parmi lesquelles sa version, les modules complémentaires de produit et les informations au niveau du système. Ces informations doivent être examinées pour tous les produits ou fonctionnalités non pris en charge dans AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Les mises à niveau d’AEM avec des produits ou des fonctionnalités non pris en charge ne sont pas recommandées et peuvent ne pas être prises en charge.
* Consultez les [notes de mise à jour](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr) pour en savoir plus sur les dernières modifications apportées à AEM as a Cloud Service.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
