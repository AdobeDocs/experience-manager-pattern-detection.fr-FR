---
title: REP
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: 7d05067fc624571e6fe520e2a1addd5dff8acbd8
workflow-type: ht
source-wordcount: '271'
ht-degree: 100%

---


# [!DNL REP] {#rep}

Agent de réplication

## Arrière-plan {#background}

`REP` identifie les agents de réplication activés. Ces rapports sont générés en raison des problèmes potentiels qui devraient être résolus lors de la mise à niveau vers AEM as a Cloud Service.

AEM as a Cloud Service utilise [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) pour distribuer le contenu de l’environnement de création vers celui de publication. Cette opération est effectuée en dehors de l’exécution d’AEM à l’aide du service de pipeline Adobe I/O. La configuration dans l’environnement AEM as a Cloud Service est automatique.

## Enjeux et risques possibles {#implications-and-risks}

* La configuration de la réplication a changé avec AEM as a Cloud Service. Tous les agents de réplication actuels doivent être revus afin de déterminer lesquels sont remplacés par des fonctionnalités standard, quelles configurations doivent être déplacées vers le code et lesquelles ne sont pas prises en charge.
* Toute utilisation d’agents de réplication dans du code ou des workflows personnalisés doit être examinée lors de la mise à niveau vers AEM as a Cloud Service.
* La réplication inverse n’est initialement pas prise en charge dans AEM as a Cloud Service.
* Il n’est pas nécessaire de configurer un agent de purge de Dispatcher distinct. Ce paramètre est automatiquement configuré dans l’environnement AEM as a Cloud Service.

## Solutions possibles {#solutions}

* Consultez les [Conseils de développement](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=fr#no-reverse-replication-agents) AEM as a Cloud Service et les notes de mise à jour des [agents de réplication](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=fr#replication-agents).
* Examinez, restructurez et optimisez les fonctionnalités qui dépendent directement des agents de réplication pour effectuer des tâches métier.
* Découvrez comment le déploiement dans AEM as a Cloud Service affecte la [réplication](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=fr#replication).
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
