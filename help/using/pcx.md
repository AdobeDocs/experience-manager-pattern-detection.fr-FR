---
title: PCX
description: Page d’aide sur le code de la détection des motifs.
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 95%

---

# PCX {#pcx}

Complexité de la page

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Page Complexity (complexité de la page)"
>abstract="PCX identifie les pages qui contiennent un grand nombre de nœuds dans leur structure."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Changements notables - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Notes de mise à jour"

`PCX`  Identifie les pages qui contiennent de nombreux noeuds dans leur structure.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `page.complexity.medium` : une page contient un nombre de nœuds modérément élevé qui peut affecter les performances de rendu.
* `page.complexity.high` : une page contient un nombre de nœuds élevé qui peut affecter les performances de rendu.

## Enjeux et risques possibles {#implications-and-risks}

* De nombreux nœuds dans une page peut affecter ses performances de rendu.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons de revoir la structure du contenu pour réduire la complexité des pages afin d’améliorer les performances de rendu des pages. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Réduisez le nombre total de nœuds dans une page en procédant comme suit :
   * Vérifiez qu’il n’y a pas de conteneurs inutiles.
   * Testez si la même disposition peut être réalisée avec moins de conteneurs.
   * Simplifiez le contenu de la page.
   * Réduisez la profondeur de la structure des nœuds.
   * Pour simplifier, restructurez les fragments d’expérience inclus.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
