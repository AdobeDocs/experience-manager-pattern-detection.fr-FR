---
title: WRK
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 92%

---

# WRK {#wrk}

Workflow

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Workflow"
>abstract="Le code WRK identifie une recherche liée à un modèle ou à un lanceur de workflow. Ces rapports sont générés, car les modèles de workflow des ressources personnalisés doivent être migrés lors de la mise à niveau vers AEM as a Cloud Service. Avec AEM as a Cloud Service, le traitement des ressources est désormais effectué par les microservices de ressources."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=fr" text="Microservices de ressources"

`WRK` identifie une recherche liée à un modèle ou à un lanceur de workflow. Ces rapports sont générés, car les modèles de workflow des ressources personnalisés doivent être migrés lors de la mise à niveau vers AEM as a Cloud Service.

Un sous-type est utilisé pour identifier le type de problème de workflow actuellement détecté.

* `custom.asset.workflow` : détection d’un modèle ou d’un lanceur de workflow de ressources personnalisé.

## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Guide de mise en œuvre"
>abstract="Comme les workflows de ressources standard sont automatiquement pris en charge par les microservices de ressources, nous vous recommandons de passer en revue tous les modèles ou les lanceurs de workflow de ressources personnalisés afin de déterminer s’ils sont nécessaires une fois la migration vers AEM as a Cloud Service terminée. Les personnalisations des workflows de ressources nécessitent une migration pour fonctionner avec AEM as a Cloud Service à l’aide de l’outil de migration de workflow de ressources."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html?lang=fr" text="Prise en main des microservices de ressources"

* Le traitement des ressources a traditionnellement été effectué avec des workflows de ressources exécutés sur l’instance d’auteur AEM. Avec AEM as a Cloud Service, le traitement des ressources est désormais effectué par les microservices de ressources. Voir [microservices de ressources - Aperçu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=fr) pour plus d’informations.
* Les workflows de ressources standard sont automatiquement pris en charge par les microservices de ressources.
* Les personnalisations des workflows de ressources nécessitent une migration pour fonctionner avec AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Outils et ressources"
>abstract="Consultez l’outil de migration de workflows de ressources et planifiez son exécution une fois qu’un modèle ou un lanceur de workflow de ressources personnalisé est identifié. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html?lang=fr" text="Outil de migration des workflows de ressources"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Si un modèle ou un lanceur de workflow de ressources personnalisé est identifié, prévoyez d’exécuter l’[Outil de migration des workflows de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html?lang=fr).
* Pour plus d’informations, consultez [Prise en main de l’utilisation des microservices de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html?lang=fr).
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
