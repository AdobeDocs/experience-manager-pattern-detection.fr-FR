---
title: MI
description: Page d’aide sur le code de la détection des motifs
source-git-commit: aa05ebcb54c6945a903c76add4f31e3279cd05b5
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 100%

---

# MI {#mi}

Problème de configuration

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Problème de configuration"
>abstract="Le MI identifie les problèmes de configuration sur l’instance AEM"

`MI` Le MI (problème de configuration) identifie les problèmes de configuration sur l’instance AEM.

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
   * Il est conseillé de définir la valeur sur 0,5 afin de bénéficier de la moitié des processeurs disponibles.
* `missing.maintenance.configuration`
   * Nettoyage des révisions : reportez-vous à la section [Nettoyage des révisions](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=fr). La partie importante concernant la configuration est la suivante : [Nettoyage des révisions - Configuration de la compression complète et partielle](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=fr#how-to-configure-full-and-tail-compaction).
   * Nettoyage des fichiers binaires Lucene : reportez-vous à la section [Tableau de bord des opérations - Nettoyage des fichiers binaires Lucene](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-dashboard.html?lang=fr#lucene-binaries-cleanup).
   * Récupération de la mémoire du magasin de données : reportez-vous à la section [Récupération de la mémoire du magasin de données](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/data-store-garbage-collection.html?lang=fr).
   * Purge du workflow : reportez-vous à la section [Purge régulière des instances de workflow](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/workflows-administering.html?lang=fr#regular-purging-of-workflow-instances).
   * Tâche de maintenance du journal d’audit : reportez-vous à la section [Maintenance du journal d’audit](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-audit-log.html?lang=fr).
* Contactez notre [équipe d’assistance clientèle Experience Manager](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des explications ou pour répondre à vos préoccupations.