---
title: WRK
description: Page d’aide sur le code de détection des motifs.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 100%

---

# WRK {#wrk}

Workflow

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Workflow"
>abstract="Le code WRK identifie une recherche liée à un modèle ou à un lanceur de workflow. Ces identifications sont rapportées, car les modèles de workflows de ressource personnalisés doivent être migrés lors de la mise à niveau vers AEM as a Cloud Service. Avec AEM as a Cloud Service, les microservices de ressources effectuent le traitement des ressources."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview" text="Microservices de ressources"

`WRK` identifie un résultat lié à un modèle ou à un lanceur de workflow. Ces identifications sont rapportées, car les modèles de workflows de ressource personnalisés doivent être migrés lors de la mise à niveau vers AEM as a Cloud Service.

Un sous-type est utilisé pour identifier le type de problème de workflow actuellement détecté.

* `custom.asset.workflow` : détection d’un modèle ou d’un lanceur de workflow de ressources personnalisé.

## Implications et risques éventuels {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Guide de mise en œuvre"
>abstract="Les workflows de ressources standard sont automatiquement pris en charge par les microservices de ressources. Par conséquent, il est reommandé d’examiner tous les modèles de workflows de ressource personnalisés ou le lanceur. Lors de la révision, vous pouvez voir s’ils sont nécessaires après votre transition vers AEM as a Cloud Service. Les personnalisations des workflows de ressources nécessitent une migration pour fonctionner avec AEM as a Cloud Service à l’aide de l’outil de migration des workflows de ressources."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use" text="Prise en main des microservices de ressources"

* Le traitement des ressources a traditionnellement été effectué avec des workflows de ressources exécutés sur l’instance de création AEM. Avec AEM as a Cloud Service, les microservices de ressources effectuent le traitement des ressources. Pour plus d’informations, consultez la [vue d’ensemble sur les microservices de ressources](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview).
* Les workflows de ressources standard sont automatiquement pris en charge par les microservices de ressources.
* Les personnalisations des workflows de ressources nécessitent une migration pour fonctionner avec AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Outils et ressources"
>abstract="Consultez et planifiez l’exécution de l’outil de migration du workflow des ressources une fois qu’un modèle de workflow des ressources personnalisé ou un lanceur a été identifié. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool" text="Outil de migration des workflows de ressources"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Si un modèle ou un lanceur de workflow de ressources personnalisé est identifié, prévoyez d’exécuter l’[Outil de migration des workflows de ressources](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool).
* Pour plus d’informations, consultez [Prise en main de l’utilisation des microservices de ressources](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use).
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
