---
title: WRK
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 62%

---

# WRK {#wrk}

Workflow

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Workflow"
>abstract="Le code WRK identifie une recherche liée à un modèle ou à un lanceur de workflow. Ces rapports sont générés, car les modèles de workflow des ressources personnalisés doivent être migrés lors de la mise à niveau vers AEM as a Cloud Service. Avec AEM as a Cloud Service, le traitement des ressources est désormais effectué par les microservices de ressources."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview" text="Microservices de ressources"

WRK identifie un résultat associé à un modèle de workflow ou à un lanceur. Ces rapports sont générés, car les modèles de workflow des ressources personnalisés doivent être migrés lors de la mise à niveau vers AEM as a Cloud Service.

Un sous-type est utilisé pour identifier le type de problème de workflow actuellement détecté.

* `custom.asset.workflow` : détection d’un modèle ou d’un lanceur de workflow de ressources personnalisé.

## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Guide de mise en œuvre"
>abstract="Les workflows de ressources standard sont automatiquement pris en charge par mes microservices de ressources. Par conséquent, la bonne pratique consiste à passer en revue tous les modèles de workflow de ressources personnalisés ou le lanceur pour voir s’ils sont nécessaires après la transition vers AEM as a Cloud Service. Les personnalisations des workflows de ressources nécessitent que la migration fonctionne avec AEM as a Cloud Service à l’aide de l’outil de migration des workflows de ressources"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use" text="Prise en main des microservices de ressources"

* Le traitement des ressources a traditionnellement été effectué avec des workflows de ressources exécutés sur l’instance d’auteur AEM. Avec AEM as a Cloud Service, le traitement des ressources est désormais effectué par les microservices de ressources. Voir [microservices de ressources - Aperçu](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview) pour plus d’informations.
* Les workflows de ressources standard sont automatiquement pris en charge par les microservices de ressources.
* Pour que les personnalisations des workflows de ressources fonctionnent avec AEM as a Cloud Service, la migration doit être effectuée.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Outils et ressources"
>abstract="Consultez l’outil de migration de workflows de ressources et planifiez son exécution une fois qu’un modèle ou un lanceur de workflow de ressources personnalisé est identifié. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool" text="Outil de migration des workflows de ressources"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Si un modèle ou un lanceur de workflow de ressources personnalisé est identifié, prévoyez d’exécuter l’[Outil de migration des workflows de ressources](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool).
* Pour plus d’informations, consultez [Prise en main de l’utilisation des microservices de ressources](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use).
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
