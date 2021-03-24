---
title: DG
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 2%

---


# DG {#dg}

Guide du développeur

## Arrière-plan {#background}

`DG` identifie les écarts par rapport à certaines lignes directrices de développement pour  [AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html) et  [AEM en tant que Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html). Le respect des meilleures pratiques peut améliorer la maintenance et les performances de votre système. Bien que certains de ces écarts ne soient pas un problème dans d&#39;autres contextes d&#39;application, y compris avec les versions précédentes d&#39;AEM, ils peuvent causer des problèmes lorsqu&#39;ils sont utilisés avec AEM en tant que Cloud Service.

Les sous-types sont utilisés pour identifier les différents types de violations détectées :

* `java.io.inputstream`: Utilisation de  `java.io.InputStream` dans le code de l’application.
* `maintenance.task.configuration`: Configuration d&#39;une certaine activité de maintenance périodique.
* `sling.commons.scheduler`: Utilisation de l’API du Planificateur Sling Commons pour une tâche planifiée.

## Incidences possibles et risques {#implications-and-risks}

* `java.io.inputstream`
   * La diffusion en flux continu de données binaires avec `java.io.InputStream` peut consommer des ressources de mémoire au point d&#39;avoir une incidence sur les performances. Ceci est particulièrement problématique en raison de la mémoire limitée disponible dans les conteneurs utilisés en AEM en tant que Cloud Service.

* `maintenance.task.configuration`
   * Certaines tâches de maintenance qui exigeaient auparavant une configuration explicite sont désormais automatiquement configurées et gérées dans AEM en tant que Cloud Service.
   * La configuration de la tâche de maintenance dans AEM en tant que Cloud Service doit être déplacée dans le contrôle de code source.

* `sling.commons.scheduler`
   * Les applications dépendantes des tâches d&#39;arrière-plan utilisant [le Planificateur Sling Commons](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) peuvent ne pas fonctionner comme prévu, car l&#39;exécution ne peut pas être garantie en AEM en tant que Cloud Service.
   * AEM en tant que directives de développement Cloud Service pour [les tâches d&#39;arrière-plan et les travaux à long terme](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#background-tasks-and-long-running-jobs) suggèrent que le code exécuté en tant que tâche planifiée doit supposer que l&#39;instance sur laquelle il est exécuté peut être supprimé à tout moment. Par conséquent, le code doit être résilient et réutilisable.

## Solutions possibles {#solutions}

* `java.io.inputstream`
   * Utilisez une approche de transfert direct-binaire dans laquelle le binaire est ajouté directement à la banque de données.
   * Pour les cas d’utilisation des ressources, utilisez [aem-upload](https://github.com/adobe/aem-upload). Pour les autres types de binaires, la logique de téléchargement personnalisée peut être modélisée selon ce même modèle.

* `maintenance.task.configuration`
   * Examinez AEM en tant que Cloud Service [Documentation sur la Tâche de maintenance](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html).
   * Assurez-vous que [Configuration de la Tâche de maintenance](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#maintenance-tasks-configuration-in-source-control) est dans le contrôle de code source.

* `sling.commons.scheduler`
   * Remplacez [Sling Commons Planificateur](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) par [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), qui ont une garantie d’exécution au moins une fois.
   * Les emplois de longue durée devraient être évités si possible.

* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
