---
title: CIF
description: Page d’aide sur le code de détection des motifs.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: ht
source-wordcount: '308'
ht-degree: 100%

---

# CIF {#cif}

Version classique de Commerce Integration Framework

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Version classique de Commerce Integration Framework"
>abstract="CIF identifie l’utilisation de la version classique de Commerce Integration Framework qui est incompatible avec AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Content and Commerce"

`CIF` identifie une utilisation de la version classique de Commerce integration framework incompatible avec AEM as a Cloud Service. Le message pour chaque résultat du `CIF` identifie le type d’utilisation et fournit des informations supplémentaires.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `commerce.integration.framework.detected` : occurrence d’incompatibilité de la version classique de Commerce Integration Framework avec AEM as a Cloud Service.


## Implications et risques éventuels {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Guide de mise en œuvre"
>abstract="La bonne pratique consiste à passer en revue toutes les utilisations de la version classique de Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/content-and-commerce/changes" text="Changements notables apportés à CIF"

* La version classique de Commerce Integration Framework n’est plus prise en charge dans AEM as a Cloud Service. Son utilisation bloque la mise à niveau vers AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Outils et ressources"
>abstract="Ce guide permet d’identifier les zones à mettre à jour pour la migration d’Experience Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/content-and-commerce/migration" text="Guide de migration pour CIF"

* Pour Experience Manager as a Cloud Service, le module complémentaire CIF est la seule solution d’intégration commerciale prise en charge pour Adobe Commerce et les solutions commerciales tierces. Le module complémentaire CIF est déployé automatiquement pour les clients sur Experience Manager as a Cloud Service, aucun déploiement manuel n’est nécessaire. Consultez [Prise en main d’AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started).
* Pour prendre en charge les projets qui déploient CIF, Adobe fournit [les composants principaux CIF AEM](https://github.com/adobe/aem-core-cif-components).
* Le module complémentaire CIF est également disponible pour AEM 6.5 dans le [portail de distribution logicielle](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). Il est compatible et fournit les mêmes fonctionnalités que le module complémentaire CIF pour Experience Manager as a Cloud Service ; aucun ajustement n’est nécessaire.
* Le CIF classique avec ses dépendances n’est plus disponible. Le code qui utilise cette version du CIF avec l’API Java™ com.adobe.cq.commerce.api doit être adapté au module complémentaire CIF et à ses principes.
