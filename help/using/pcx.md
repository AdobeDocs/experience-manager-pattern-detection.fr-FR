---
title: PCX
description: Page d’aide sur le code de la détection des motifs
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 100%

---

# PCX {#pcx}

Complexité de la page

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Page Complexity (complexité de la page)"
>abstract="PCX identifie les pages qui contiennent un grand nombre de nœuds dans leur structure."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=fr" text="Changements notables – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr" text="AEM as a Cloud Service – Notes de mise à jour"

`PCX` identifie les pages qui contiennent un grand nombre de nœuds dans leur structure.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `page.complexity.medium` : une page contient un nombre de nœuds modérément élevé qui peut affecter les performances de rendu.
* `page.complexity.high` : une page contient un nombre très élevé de nœuds qui affecteront probablement les performances de rendu.

## Enjeux et risques possibles {#implications-and-risks}

* Un grand nombre de nœuds dans une page peut affecter ses performances de rendu.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons de revoir la structure du contenu pour réduire la complexité des pages afin d’améliore les performances de rendu des pages. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Prenez des mesures pour réduire le nombre total de nœuds dans une page, notamment :
   * Vérifiez qu’il n’y a pas de conteneurs inutiles.
   * Testez si la même disposition peut être réalisée avec moins de conteneurs.
   * Simplifiez le contenu de la page.
   * Réduisez la profondeur de la structure des nœuds.
   * Pour simplifier, restructurez les fragments d’expérience inclus.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
