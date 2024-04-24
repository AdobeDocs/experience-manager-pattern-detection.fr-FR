---
title: REP
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 73%

---

# [!DNL REP] {#rep}

Agent de réplication

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Agent de réplication"
>abstract="REP identifie les agents de réplication activés. Ces rapports sont générés en raison des problèmes potentiels qui devraient être résolus lors de la mise à niveau vers AEM as a Cloud Service. AEM as a Cloud Service utilise Sling Content Distribution pour distribuer le contenu de l’environnement de création vers celui de publication. Cette opération est effectuée en dehors de l’exécution AEM à l’aide du service de pipeline de Adobe I/O Runtime sur Adobe Developer. Il est automatiquement configuré dans l’environnement as a Cloud Service configuré AEM."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents" text="Changements notables – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents" text="Conseils de développement"

`REP`  Identifie les agents de réplication activés. Ces rapports sont générés en raison des problèmes potentiels qui devraient être résolus lors de la mise à niveau vers AEM as a Cloud Service.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `forward.replication` : identifier les agents de réplication de transfert activés.
* `reverse.replication` : identifier les agents de réplication inverse activés.
* `standard.replication.agent.modification` : identifier les agents de réplication standard activés qui sont modifiés.
* `custom.replication.agent.detection` : identifier les agents de réplication personnalisés activés.

AEM as a Cloud Service utilise [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) pour distribuer le contenu de l’environnement de création vers celui de publication. Cette opération est effectuée en dehors de l’exécution AEM à l’aide du service de pipeline de Adobe I/O Runtime sur Adobe Developer. Il est automatiquement configuré dans l’environnement as a Cloud Service configuré AEM.

## Enjeux et risques possibles {#implications-and-risks}

* La configuration de la réplication a changé avec AEM as a Cloud Service. Tous les agents de réplication actuels doivent être revus afin de déterminer lesquels sont remplacés par des fonctionnalités standard, quelles configurations doivent être déplacées vers le code et lesquelles ne sont pas prises en charge.
* Toute utilisation d’agents de réplication dans du code ou des workflows personnalisés doit être examinée lors de la mise à niveau vers AEM as a Cloud Service.
* La réplication inverse n’est initialement pas prise en charge dans AEM as a Cloud Service.
* Il n’est pas nécessaire de configurer un agent de vidage Dispatcher distinct. Ce paramètre est automatiquement configuré dans l’environnement AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons d’examiner, de refactoriser et d’optimiser les fonctionnalités personnalisées dépendant directement des agents de réplication et de les rendre compatibles avec AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication" text="Réplication – AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Consultez les [Conseils de développement](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents) AEM as a Cloud Service et les notes de mise à jour des [agents de réplication](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents).
* Examinez, restructurez et optimisez les fonctionnalités qui dépendent directement des agents de réplication pour effectuer des tâches métier.
* Découvrez comment le déploiement dans AEM as a Cloud Service affecte la [réplication](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication).
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
