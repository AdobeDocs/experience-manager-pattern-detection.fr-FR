---
title: OCU
description: Page d’aide sur le code de la détection des motifs
exl-id: cb28c727-415d-436c-ab74-cf7f1f34f7c7
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 100%

---

# OCU {#ocu}

OBSOLÈTE : Utilisation du code obsolète (remplacé par OU, Utilisation obsolète)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_overview"
>title="Outdated Code Usage (utilisation de code obsolète)"
>abstract="OCU identifie la situation dans laquelle certains nœuds JCR, tels que Sling ou les composants AEM ou les exportations OSGi de l’API, sont modifiés ou supprimés d’une manière non compatible. Le client n’est peut-être pas au courant de cette modification avant une mise à niveau. Ils peuvent être mis à niveau vers une version non compatible ou ne pas être disponibles du tout."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=fr" text="Changements notables – AEM as a Cloud Service"

`OCU` identifie la situation dans laquelle certains nœuds JCR, tels que Sling ou les composants AEM ou les exportations OSGi de l’API, sont modifiés ou supprimés d’une manière non compatible. Le client n’est peut-être pas au courant de cette modification avant une mise à niveau. Ils peuvent être mis à niveau vers une version non compatible ou ne pas être disponibles du tout.

Comme les anciennes versions ne sont pas installées par défaut, l’application cliente risque de ne pas fonctionner correctement.

## Enjeux et risques possibles {#implications-and-risks}

* Les fonctionnalités qui dépendent de tout composant utilisant des composants ou des API obsolètes peuvent être rompues et ne pas être résolues correctement après une mise à niveau.
* Certaines fonctionnalités de l’application cliente ou certaines fonctionnalités AEM peuvent ne pas fonctionner correctement ou ne pas être actives après une mise à niveau.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_guidance"
>title="Guide de mise en œuvre"
>abstract="Il est recommandé de revoir et d’adapter le code client pour lui permettre d’utiliser la nouvelle version des composants ou des API AEM. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API du SDK Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* À court terme : l’installation du package de compatibilité peut vous aider.
* À long terme : adaptez le code client pour utiliser la dernière version des composants ou API AEM.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
