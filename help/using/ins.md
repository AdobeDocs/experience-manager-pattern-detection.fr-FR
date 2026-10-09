---
title: INS
description: Page d’aide sur le code de détection des motifs.
exl-id: d89e1589-3195-4b2d-98f4-136bedaecb0b
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 100%
---
# INS {#ins}

Espace de noms non valide

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_overview"
>title="Espace de noms non valide"
>abstract="L’INS identifie les problèmes d’espace de noms sur l’instance AEM"

`INS` (Espace de noms non valide) : identifie les problèmes d’espace de noms dans l’instance AEM.

Des sous-types sont utilisés pour identifier les différents types d’informations, notamment :

* `uri` : identifie l’URI d’espace de noms non valide dans AEM.

## Enjeux et risques possibles {#implications-and-risks}

* Impossible de répliquer le contenu (sur plusieurs niveaux) ou de copier le contenu (sur `env`, via `/crx/packMgr` ou Copie de contenu).

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="Guide de mise en œuvre"
>abstract="Contactez l’assistance clientèle pour obtenir de l’aide."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Corrigez les définitions d’espace de noms en fonction des [Spécifications JCR](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html). Suivez les étapes mentionnées [ici](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163).
* Contactez l’[équipe d’assistance clientèle Experience Manager](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
