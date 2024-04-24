---
title: NCC
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 56%

---

# NCC {#ncc}

Modifications non compatibles

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Modifications non compatibles"
>abstract="NCC identifie la situation dans laquelle certains nœuds ou lots JCR sont modifiés de manière non compatible. Le client n’a peut-être pas connaissance de cette modification avant une mise à niveau."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Changements notables – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notes de mise à jour d’AEM as a Cloud Service"

`NCC`  Identifie la situation dans laquelle certains noeuds ou lots JCR sont modifiés d’une manière non compatible. Le client n’a peut-être pas connaissance de cette modification avant une mise à niveau.

## Enjeux et risques possibles {#implications-and-risks}

* Les fonctionnalités qui dépendent de tout composant utilisant des modifications non compatibles peuvent être rompues et ne pas être résolues correctement.
* Certaines fonctionnalités de l’application cliente ou certaines fonctionnalités AEM peuvent ne pas fonctionner correctement après une mise à niveau.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Guide de mise en œuvre"
>abstract="Il est recommandé de consulter le code personnalisé et de s’assurer que seuls les composants Sling compatibles sont superposés ou référencés. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Recouvrements"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Superposez ou référencez uniquement les composants Sling compatibles.
* Envisagez d’adapter les ressources provenant de `/libs` ou de lots après une mise à niveau d’AEM.
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
