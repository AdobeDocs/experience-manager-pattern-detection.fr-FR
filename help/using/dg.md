---
title: DG
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 94%

---

# DG {#dg}

Developer Guideline (conseil pour les développeurs)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Conseils pour les développeurs"
>abstract="Le code DG identifie les écarts par rapport à certaines lignes directrices de développement pour AEM 6.5 et AEM as a Cloud Service. Le respect des bonnes pratiques peut améliorer la maintenabilité et les performances de votre système. Bien que certains de ces écarts ne constituent pas un problème dans d’autres contextes d’application, y compris avec les versions précédentes d’AEM, ils peuvent causer des problèmes lorsqu’ils sont utilisés avec AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=fr" text="Développement AEM – Conseils et bonnes pratiques"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=fr" text="Conseils de développement pour AEM as a Cloud Service"


`DG` identifie les écarts par rapport à certaines lignes directrices de développement pour [AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=fr) et [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=fr). Le respect des bonnes pratiques peut améliorer la maintenabilité et les performances de votre système. Bien que certains de ces écarts ne constituent pas un problème dans d’autres contextes d’application, y compris avec les versions précédentes d’AEM, ils peuvent causer des problèmes lorsqu’ils sont utilisés avec AEM as a Cloud Service.

Des sous-types sont utilisés pour identifier les différents types de violations détectées :

* `java.io.inputstream` : utilisation de `java.io.InputStream` dans le code d’application.
* `maintenance.task.configuration` : configuration d’une certaine activité de maintenance périodique.
* `sling.commons.scheduler` : utilisation de l’API de planificateur Sling Commons pour une tâche planifiée.
* `unsupported.asset.api` : utilisation d’API Asset Manager non prises en charge dans le code de l’application.
* `javax.jcr.observation.EventListener` : utilisation de l’écouteur d’événement dans le code d’application.
* `custom.guava.cache` : utilisation du cache Guava dans le code d’application.

## Enjeux et risques possibles {#implications-and-risks}

* `java.io.inputstream`
   * La diffusion en flux continu de données binaires avec `java.io.InputStream` peut consommer des ressources de mémoire au point d’avoir une incidence sur les performances. Cela est particulièrement problématique en raison de la mémoire limitée disponible dans les conteneurs utilisés dans AEM as a Cloud Service.

* `maintenance.task.configuration`
   * Certaines tâches de maintenance qui exigeaient précédemment une configuration explicite sont désormais automatiquement configurées et gérées dans AEM as a Cloud Service.
   * La configuration de la tâche de maintenance dans AEM as a Cloud Service doit être migrée vers le contrôle de code source.

* `sling.commons.scheduler`
   * Les applications dépendantes des tâches d’arrière-plan utilisant le [planificateur Sling Commons](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) peuvent ne pas fonctionner comme prévu, car l’exécution ne peut pas être garantie dans AEM as a Cloud Service.
   * Les lignes directrices de développement d’AEM as a Cloud Service pour les [tâches d’arrière-plan et les travaux à long terme](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=fr#background-tasks-and-long-running-jobs) suggèrent que le code exécuté en tant que tâche planifiée doit supposer que l’instance sur laquelle il est exécuté peut être supprimée à tout moment. Par conséquent, le code doit être résilient et doit pouvoir être repris.

* `unsupported.asset.api`
   * Les API Asset Manager suivantes sont marquées comme non prises en charge dans AEM as a Cloud Service.
      * createAssetForBinary
      * getAssetForBinary
      * removeAssetForBinary
      * createAsset

* `javax.jcr.observation.EventListener`
   * Les applications qui dépendent d’un écouteur d’événement peuvent ne pas fonctionner comme prévu, car l’exécution ne peut pas être garantie.

* `custom.guava.cache`
   * L’utilisation du cache Guava peut entraîner des problèmes de performances sur AEM.


## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="Guide de mise en œuvre"
>abstract="Conformément aux lignes directrices et aux bonnes pratiques de développement AEM, les clients doivent revoir leurs mises en œuvre en fonction de l’utilisation du planificateur Sling Commons et les transformer en tâches Sling, restructurer leurs tâches de maintenance système, passer en revue la diffusion en continu de toutes les données binaires et adapter leur code pour qu’il soit conforme à AEM as a Cloud Service."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Tâches Sling"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html?lang=fr" text="Tâches de maintenance dans AEM as a Cloud Service"

* `java.io.inputstream`
   * Utilisez une approche de chargement avec accès direct au binaire dans laquelle le binaire est ajouté directement au magasin de données.
   * Pour connaître les cas d’utilisation des ressources, voir [aem-upload](https://github.com/adobe/aem-upload). Pour les autres types de binaires, la logique de chargement personnalisée peut être modélisée selon ce même motif.

* `maintenance.task.configuration`
   * Examinez la documentation de la [Tâche de maintenance](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html?lang=fr) AEM as a Cloud Service.
   * Assurez-vous que la [Configuration de la tâche de maintenance](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=fr#maintenance-tasks-configuration-in-source-control) est dans le contrôle source.

* `sling.commons.scheduler`
   * Remplacez l’utilisation du [planificateur Sling Commons](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) par les [Tâches Sling](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), qui ont une garantie d’exécution d’au moins une fois.
   * Si possible, les tâches de longue durée devraient être évitées.

* `unsupported.asset.api`
   * Au lieu d’utiliser les API non prises en charge par Asset Manager, reportez-vous à la section [aem-upload](https://github.com/adobe/aem-upload).

* `javax.jcr.observation.EventListener`
   * Au lieu d’utiliser l’écouteur d’événement, il est conseillé de refactoriser le mécanisme de gestion des événements en [Tâches Sling](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing) car il garantit le traitement.

* `custom.guava.cache`
   * Si nécessaire, les caches doivent être créés en dehors d’AEM. La solution de mise en cache externe peut être envisagée.
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
