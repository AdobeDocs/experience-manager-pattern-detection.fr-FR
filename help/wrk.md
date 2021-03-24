---
title: WRK
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 7%

---


# WRK {#wrk}

Workflow

## Arrière-plan {#background}

`WRK` identifie une recherche liée à un modèle de processus ou à un lanceur. Ces rapports sont générés car les modèles de processus des ressources personnalisées doivent être migrés lors de la mise à niveau vers AEM en tant que Cloud Service.

Un sous-type est utilisé pour identifier le type de problème de flux de travail actuellement détecté.

* `custom.asset.workflow`: Détection d’un modèle ou d’un lanceur de processus de ressources personnalisé.

## Incidences possibles et risques {#implications-and-risks}

* Le traitement des ressources a traditionnellement été effectué avec des workflows de ressources exécutés sur l’instance d’auteur AEM. Avec l’AEM en tant que Cloud Service, le traitement des actifs est désormais effectué par les microservices de ressources. (Pour plus d&#39;informations, consultez la [présentation des microservices de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=fr).
* Les workflows de ressources standard sont automatiquement pris en charge par mes microservices de ressources.
* Les personnalisations des workflows de ressources nécessitent une migration pour pouvoir travailler avec AEM en tant que Cloud Service.

## Solutions possibles {#solutions}

* Si un modèle ou un lanceur de processus de ressources personnalisé est identifié, prévoyez d&#39;exécuter l&#39;[Outil de migration de processus de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html).
* Pour plus d’informations, consultez la section [Prise en main de l’utilisation des microservices de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html?lang=fr).
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
