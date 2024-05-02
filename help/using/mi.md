---
title: MI
description: Page d’aide sur le code de la détection des motifs.
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 95%

---

# MI {#mi}

Problème de configuration

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Problème de configuration"
>abstract="Le MI identifie les problèmes de configuration sur l’instance AEM"

`MI` (Problème de configuration incorrect) Identifie les problèmes de configuration sur l’instance AEM.

Des sous-types sont utilisés pour identifier les différents types d’informations, notamment :

* `sling.job.max.parallel` : identifiez les tâches sling pour lesquelles la configuration parallèle maximale est définie sur -1.
* `missing.maintenance.configuration` : identifiez les configurations de tâche de maintenance manquantes.

## Enjeux et risques possibles {#implications-and-risks}

* `sling.job.max.parallel`
   * Une valeur de -1 est remplacée par le nombre de processeurs disponibles. Cela peut entraîner des problèmes de performances sur l’instance AEM.
* `missing.maintenance.configuration`
   * Les configurations de tâche de maintenance manquantes peuvent entraîner une perte de performances ou une corruption de l’instance.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Guide de mise en œuvre"
>abstract="Contactez l’assistance clientèle pour obtenir de l’aide."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* `sling.job.max.parallel`
   * Adobe recommande de définir la valeur sur 0,5 pour tirer parti de la moitié des processeurs disponibles.
* `missing.maintenance.configuration`
   * Nettoyage des révisions : reportez-vous à la section [Nettoyage des révisions](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup). La partie importante concernant la configuration est la suivante : [Nettoyage des révisions - Configuration de la compression complète et partielle](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup).
   * Nettoyage des fichiers binaires Lucene : reportez-vous à la section [Tableau de bord des opérations - Nettoyage des fichiers binaires Lucene](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/sites/administering/operations/operations-dashboard#lucene-binaries-cleanup).
   * Récupération de l’espace mémoire du magasin de données : reportez-vous à la section [Récupération de l’espace mémoire du magasin de données](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/sites/administering/operations/data-store-garbage-collection).
   * Purge de workflow : reportez-vous à la rubrique [Purge régulière des instances de workflow](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/sites/administering/operations/workflows-administering#regular-purging-of-workflow-instances).
   * Tâche de maintenance du journal d’audit : reportez-vous à la section [Maintenance du journal d’audit](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/sites/administering/operations/operations-audit-log).
* Contactez l’[équipe d’assistance clientèle Experience Manager](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
