---
title: INS
description: Page d’aide sur le code de la détection des motifs
source-git-commit: e469b546a75a77e538a54de3ffc1ca385c8cf21d
workflow-type: ht
source-wordcount: '109'
ht-degree: 100%

---

# INS {#ins}

Espace de noms non valide

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_overview"
>title="Espace de noms non valide"
>abstract="L’INS identifie les problèmes d’espace de noms sur l’instance AEM"

`INS` L’espace de noms non valide identifie les problèmes d’espace de noms sur l’instance AEM.

Des sous-types sont utilisés pour identifier les différents types d’informations, notamment :

* `uri` : identifie l’URI d’espace de noms non valide dans AEM.

## Enjeux et risques possibles {#implications-and-risks}

* Impossible de répliquer le contenu (sur plusieurs niveaux) ou de copier le contenu (sur plusieurs environnements, via `/crx/packMgr` ou Copie de contenu).

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="Guide de mise en œuvre"
>abstract="Contactez l’assistance clientèle pour obtenir de l’aide."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Corrigez les définitions d’espace de noms en fonction des [Spécifications JCR](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html). Suivez les étapes mentionnées [ici](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163).
* Contactez notre [équipe d’assistance clientèle Experience Manager](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des explications ou pour répondre à vos préoccupations.