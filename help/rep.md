---
title: REP
description: Page d’aide sur le code de la détection des motifs
exl-id: e788deba-a301-404f-8e90-51f721409e69
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 86%

---

# [!DNL REP] {#rep}

Agent de réplication

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Agent de réplication"
>abstract="REP identifie les agents de réplication activés. Ces rapports sont générés en raison des problèmes potentiels qui devraient être résolus lors de la mise à niveau vers AEM as a Cloud Service. AEM as a Cloud Service utilise Sling Content Distribution pour distribuer le contenu de l’environnement de création vers celui de publication. Cette opération est effectuée en dehors de l’exécution d’AEM à l’aide du service de pipeline Adobe I/O. La configuration dans l’environnement AEM as a Cloud Service est automatique."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents" text="Changements notables - AEM en tant que Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents" text="Conseils de développement "

`REP` identifie les agents de réplication activés. Ces rapports sont générés en raison des problèmes potentiels qui devraient être résolus lors de la mise à niveau vers AEM as a Cloud Service.

AEM as a Cloud Service utilise [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) pour distribuer le contenu de l’environnement de création vers celui de publication. Cette opération est effectuée en dehors de l’exécution d’AEM à l’aide du service de pipeline Adobe I/O. La configuration dans l’environnement AEM as a Cloud Service est automatique.

## Enjeux et risques possibles {#implications-and-risks}

* La configuration de la réplication a changé avec AEM as a Cloud Service. Tous les agents de réplication actuels doivent être revus afin de déterminer lesquels sont remplacés par des fonctionnalités standard, quelles configurations doivent être déplacées vers le code et lesquelles ne sont pas prises en charge.
* Toute utilisation d’agents de réplication dans du code ou des workflows personnalisés doit être examinée lors de la mise à niveau vers AEM as a Cloud Service.
* La réplication inverse n’est initialement pas prise en charge dans AEM as a Cloud Service.
* Il n’est pas nécessaire de configurer un agent de purge de Dispatcher distinct. Ce paramètre est automatiquement configuré dans l’environnement AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Guide de mise en oeuvre"
>abstract="La meilleure pratique consiste à examiner, refactoriser et optimiser les fonctionnalités personnalisées directement dépendantes des agents de réplication et à les rendre compatibles avec AEM en tant que Cloud Service. Contactez l&#39;assistance Adobe pour obtenir de l&#39;aide et des éclaircissements"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication" text="Réplication - AEM en tant que Cloud Service"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Consultez les [Conseils de développement](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=fr#no-reverse-replication-agents) AEM as a Cloud Service et les notes de mise à jour des [agents de réplication](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=fr#replication-agents).
* Examinez, restructurez et optimisez les fonctionnalités qui dépendent directement des agents de réplication pour effectuer des tâches métier.
* Découvrez comment le déploiement dans AEM as a Cloud Service affecte la [réplication](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=fr#replication).
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
