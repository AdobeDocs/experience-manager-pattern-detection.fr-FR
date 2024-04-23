---
title: CIF
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 55%

---

# CIF {#cif}

Version classique de Commerce Integration Framework

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Version classique de Commerce Integration Framework"
>abstract="CIF identifie la version classique de l’utilisation du Commerce integration framework incompatible avec AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Content and Commerce"

CIF CIF identifie la version classique de l’utilisation du Commerce integration framework qui est incompatible avec la version as a Cloud Service. Le message de chaque `CIF` find identifie l’utilisation et fournit des informations supplémentaires.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `commerce.integration.framework.detected` : occurrence d’incompatibilité de la version classique de Commerce Integration Framework avec AEM as a Cloud Service.


## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Guide de mise en œuvre"
>abstract="La bonne pratique consiste à passer en revue toutes les utilisations de la version classique de Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/changes" text="Changements notables apportés à CIF"

* La version classique de Commerce Integration Framework n’est plus prise en charge dans AEM as a Cloud Service. Son utilisation bloque la mise à niveau vers AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Outils et ressources"
>abstract="Ce guide permet d’identifier les zones que vous devez mettre à jour pour la migration des Experience Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/migration" text="Guide de migration pour CIF"

* Pour Experience Manager as a Cloud Service, le module complémentaire CIF est la seule solution d’intégration commerciale prise en charge pour Adobe Commerce et les solutions commerciales tierces. Le module complémentaire CIF est déployé automatiquement pour les clients sur Experience Manager as a Cloud Service, aucun déploiement manuel n’est nécessaire. Consultez [Prise en main d’AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started).
* Pour prendre en charge les projets qui déploient CIF, Adobe fournit [les composants principaux CIF AEM](https://github.com/adobe/aem-core-cif-components).
* CIF module complémentaire est également disponible pour AEM 6.5 au moyen de la fonction [Portail de distribution de logiciels](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). Il est compatible et fournit les mêmes fonctionnalités que le module complémentaire CIF pour Experience Manager as a Cloud Service ; aucun ajustement n’est nécessaire.
* Le CIF classique avec ses dépendances n’est plus disponible. Le code reposant sur cette version CIF utilisant les API Java™ com.adobe.cq.commerce.api doit être adapté au module complémentaire CIF et à ses principes.
