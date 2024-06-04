---
title: NBCC
description: Page d’aide sur le code de détection des motifs.
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 76%

---

# NBCC {#nbcc}

OBSOLÈTE : Modifications non rétrocompatibles (remplacées par NCC, Modifications non compatibles)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Non-Backwards Compatible Changes (modifications non rétrocompatibles)"
>abstract="NBCC identifie la situation dans laquelle certains nœuds ou lots JCR sont modifiés de manière non compatible. Il est possible que les clientes et clients ne se rendent pas compte de cette modification avant une mise à niveau."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Changements notables - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notes de mise à jour - AEM as a Cloud Service"

`NBCC`  Identifie la situation dans laquelle certains noeuds ou lots JCR sont modifiés d’une manière non compatible. Il est possible que les clientes et clients ne se rendent pas compte de cette modification avant une mise à niveau.

## Implications et risques éventuels {#implications-and-risks}

* Les fonctionnalités qui dépendent de tout composant qui utilise des modifications non rétrocompatibles peuvent être interrompues et ne pas être résolues correctement.
* Certaines fonctionnalités de l’application cliente ou certaines fonctionnalités AEM peuvent ne pas fonctionner correctement après une mise à niveau.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons de consulter le code personnalisé et de vous assurer que seuls les composants Sling rétrocompatibles sont superposés ou référencés. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Recouvrements"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Superposez ou référencez uniquement les composants Sling rétrocompatibles.
* Tenir compte de l&#39;adaptation des ressources issues de `/libs` ou des lots après une mise à niveau d’AEM.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
