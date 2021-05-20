---
title: NBCC
description: Page d’aide sur le code de la détection des motifs
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 100%

---

# NBCC {#nbcc}

Non-Backwards Compatible Changes (modifications non rétrocompatibles)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Non-Backwards Compatible Changes (modifications non rétrocompatibles)"
>abstract="NBCC identifie la situation dans laquelle certains nœuds ou lots JCR sont modifiés de manière non compatible. Le client n’est peut-être pas au courant de cette modification avant une mise à niveau."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=fr" text="Changements notables – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr" text="Notes de mise à jour d’AEM as a Cloud Service"

`NBCC` identifie la situation dans laquelle certains nœuds ou lots JCR sont modifiés de manière non compatible. Le client n’est peut-être pas au courant de cette modification avant une mise à niveau.

## Enjeux et risques possibles {#implications-and-risks}

* Les fonctionnalités qui dépendent de tout composant utilisant des modifications non rétrocompatibles peuvent être rompues et ne pas être résolues correctement.
* Certaines fonctionnalités de l’application cliente ou certaines fonctionnalités AEM peuvent ne pas fonctionner correctement après une mise à niveau.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons de consulter le code personnalisé et de vous assurer que seuls les composants Sling rétrocompatibles sont superposés ou référencés. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=fr#platform" text="Recouvrements"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Superposez ou référencez uniquement les composants Sling rétrocompatibles.
* Envisagez d’adapter les ressources provenant de `/libs` ou de lots après une mise à niveau d’AEM.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
