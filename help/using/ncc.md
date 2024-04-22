---
title: NCC
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 91%

---

# NCC {#ncc}

Modifications non compatibles

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Modifications non compatibles"
>abstract="NCC identifie la situation dans laquelle certains nœuds ou lots JCR sont modifiés de manière non compatible. Le client n’est peut-être pas au courant de cette modification avant une mise à niveau."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=fr" text="Changements notables – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr" text="Notes de mise à jour d’AEM as a Cloud Service"

`NCC` identifie la situation dans laquelle certains nœuds ou lots JCR sont modifiés de manière non compatible. Le client n’est peut-être pas au courant de cette modification avant une mise à niveau.

## Enjeux et risques possibles {#implications-and-risks}

* Les fonctionnalités qui dépendent de tout composant utilisant des modifications non compatibles peuvent être rompues et ne pas être résolues correctement.
* Certaines fonctionnalités de l’application cliente ou certaines fonctionnalités AEM peuvent ne pas fonctionner correctement après une mise à niveau.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Guide de mise en œuvre"
>abstract="Il est recommandé de consulter le code personnalisé et de s’assurer que seuls les composants Sling compatibles sont superposés ou référencés. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=fr#platform" text="Recouvrements"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Superposez ou référencez uniquement les composants Sling compatibles.
* Envisagez d’adapter les ressources provenant de `/libs` ou de lots après une mise à niveau d’AEM.
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
