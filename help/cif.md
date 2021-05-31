---
title: CIF
description: Page d’aide sur le code de la détection des motifs
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 84aea5b24e51ce5672826bad4ec126074bf24a09
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 10%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifie la version classique de l’utilisation de Commerce Integration Framework qui est incompatible avec AEM en tant que Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" Contenu et commerce"

`CIF` CIF identifie la version classique de l’utilisation de Commerce Integration Framework qui est incompatible avec AEM en tant que Cloud Service. Le message de chaque résultat `CIF` identifie l’utilisation et fournit des informations supplémentaires.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `commerce.integration.framework.detected`: Une version classique de Commerce Integration Framework incompatibilité avec AEM en tant que Cloud Service.


## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Guide de mise en œuvre"
>abstract="La bonne pratique consiste à passer en revue toutes les versions classiques de l’utilisation de Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="Modifications notables apportées à CIF"

* La version classique de Commerce Integration Framework n’est plus prise en charge sur AEM en tant que Cloud Service. Cela bloquerait la mise à niveau vers AEM en tant que Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Outils et ressources"
>abstract="Ce guide permet d’identifier les zones à mettre à jour pour la migration des Experience Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="Guide de migration pour CIF"

* Pour Experience Manager en tant que Cloud Service, le module complémentaire CIF est la seule solution d’intégration commerciale prise en charge pour Adobe Commerce et les solutions commerciales tierces. Le module complémentaire CIF est déployé automatiquement pour les clients sur Experience Manager en tant que Cloud Service, aucun déploiement manuel n’est nécessaire. Voir [Prise en main d’AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html).
* Pour prendre en charge les projets qui déploient l’Adobe CIF, [AEM les composants principaux CIF](https://github.com/adobe/aem-core-cif-components).
* Le module complémentaire CIF est également disponible pour AEM 6.5 via le [portail de distribution de logiciels](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). Il est compatible et fournit les mêmes fonctionnalités que le module complémentaire CIF pour Experience Manager en tant que Cloud Service ; aucun ajustement n’est nécessaire.
* Le CIF classique avec ses dépendances n’est plus disponible. Le code reposant sur cette version de CIF à l’aide des API Java com.adobe.cq.commerce.api doit être adapté au module complémentaire CIF et à ses principes.
