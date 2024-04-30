---
title: NBCC
description: Page d’aide sur le code de la détection des motifs.
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 88%

---

# NBCC {#nbcc}

OBSOLÈTE : Modifications non rétrocompatibles (remplacées par NCC, Modifications non compatibles)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Non-Backwards Compatible Changes (modifications non rétrocompatibles)"
>abstract="NBCC identifie la situation dans laquelle certains nœuds ou lots JCR sont modifiés de manière non compatible. Lest clientes et clients ne sont peut-être pas au courant de cette modification avant une mise à niveau."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Changements notables - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notes de mise à jour d’AEM as a Cloud Service"

`NBCC`  Identifie la situation dans laquelle certains noeuds ou lots JCR sont modifiés d’une manière non compatible. Lest clientes et clients ne sont peut-être pas au courant de cette modification avant une mise à niveau.

## Enjeux et risques possibles {#implications-and-risks}

* Les fonctionnalités qui dépendent de tout composant utilisant des modifications non rétrocompatibles peuvent être rompues et ne pas être résolues correctement.
* Certaines fonctionnalités de l’application cliente ou certaines fonctionnalités AEM peuvent ne pas fonctionner correctement après une mise à niveau.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons de consulter le code personnalisé et de vous assurer que seuls les composants Sling rétrocompatibles sont superposés ou référencés. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Recouvrements"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Recouvrez ou référencez uniquement les composants Sling rétrocompatibles.
* Envisagez d’adapter les ressources provenant de `/libs` ou de lots après une mise à niveau d’AEM.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
