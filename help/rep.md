---
title: REP
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 7d05067fc624571e6fe520e2a1addd5dff8acbd8
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 2%

---


# [!DNL REP] {#rep}

Agent de réplication

## Arrière-plan {#background}

`REP` identifie les agents de réplication activés. Elles sont signalées en raison des problèmes potentiels qui devraient être résolus lors de la mise à niveau vers AEM en tant que Cloud Service.

AEM en tant que Cloud Service utilise [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) pour distribuer le contenu de l’auteur aux environnements de publication. Cette opération est effectuée en dehors de l’exécution AEM à l’aide du service de pipeline de l’Adobe I/O. Ce paramètre est automatiquement configuré dans l’AEM configuré en tant qu’environnement Cloud Service.

## Incidences possibles et risques {#implications-and-risks}

* La configuration de la réplication a changé avec AEM en tant que Cloud Service. Tous les agents de réplication actuels doivent être revus afin de déterminer lesquels sont remplacés par des fonctionnalités standard, quelles configurations doivent être déplacées vers le code et lesquelles ne sont pas prises en charge.
* Toute utilisation d&#39;agents de réplication dans du code ou des workflows personnalisés doit être examinée lors de la mise à niveau vers AEM en tant que Cloud Service.
* La réplication inverse n&#39;est pas prise en charge initialement en tant que Cloud Service dans AEM.
* Il n&#39;est pas nécessaire de configurer un agent de vidage de répartiteur distinct. Ce paramètre est automatiquement configuré dans l’AEM en tant qu’environnement Cloud Service.

## Solutions possibles {#solutions}

* Consultez l&#39;AEM en tant que Cloud Service [Directives de développement](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents) et notes de mise à jour pour [agents de réplication](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents).
* Examinez, refacturez et optimisez les fonctionnalités directement dépendantes des agents de réplication pour effectuer des tâches métier.
* Découvrez comment [la réplication](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication) est affectée par le déploiement en AEM en tant que Cloud Service.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
