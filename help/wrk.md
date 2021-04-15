---
title: WRK
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: ht
source-wordcount: '197'
ht-degree: 100%

---


# WRK {#wrk}

Workflow

## Arrière-plan {#background}

`WRK` identifie une recherche liée à un modèle ou à un lanceur de workflow. Ces rapports sont générés, car les modèles de workflow des ressources personnalisés doivent être migrés lors de la mise à niveau vers AEM as a Cloud Service.

Un sous-type est utilisé pour identifier le type de problème de workflow actuellement détecté.

* `custom.asset.workflow` : détection d’un modèle ou d’un lanceur de workflow de ressources personnalisé.

## Enjeux et risques possibles {#implications-and-risks}

* Le traitement des ressources a traditionnellement été effectué avec des workflows de ressources exécutés sur l’instance d’auteur AEM. Avec AEM as a Cloud Service, le traitement des ressources est désormais effectué par les microservices de ressources. (Pour plus d’informations consultez la [Présentation des microservices de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=fr).
* Les workflows de ressources standard sont automatiquement pris en charge par les microservices de ressources.
* Les personnalisations des workflows de ressources nécessitent une migration pour fonctionner avec AEM as a Cloud Service.

## Solutions possibles {#solutions}

* Si un modèle ou un lanceur de workflow de ressources personnalisé est identifié, prévoyez d’exécuter l’[Outil de migration des workflows de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html?lang=fr).
* Pour plus d’informations, consultez [Prise en main de l’utilisation des microservices de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html?lang=fr).
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
