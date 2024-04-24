---
title: INS
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: d89e1589-3195-4b2d-98f4-136bedaecb0b
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 60%

---

# INS {#ins}

Espace de noms non valide

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_overview"
>title="Espace de noms non valide"
>abstract="L’INS identifie les problèmes d’espace de noms sur l’instance AEM"

`INS`  (Espace de noms non valide) Identifie les problèmes d’espace de noms sur l’instance AEM.

Des sous-types sont utilisés pour identifier les différents types d’informations, notamment :

* `uri` : identifie l’URI d’espace de noms non valide dans AEM.

## Enjeux et risques possibles {#implications-and-risks}

* Impossible de répliquer le contenu (sur plusieurs niveaux) ou de copier le contenu (sur plusieurs niveaux) `env`, par `/crx/packMgr`ou Copie de contenu).

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="Guide de mise en œuvre"
>abstract="Contactez l’assistance clientèle pour obtenir de l’aide."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Corrigez les définitions d’espace de noms en fonction des [Spécifications JCR](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html). Suivez les étapes mentionnées [ici](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163).
* Contactez le [Équipe d’assistance clientèle Experience Manager](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre aux préoccupations.
