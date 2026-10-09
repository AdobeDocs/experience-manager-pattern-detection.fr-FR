---
title: OU
description: Page d’aide sur le code de Pattern Detector.
exl-id: 6ec96fab-dd6e-46af-864f-05dad387cbb6
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 97%
---
# OU {#ou}

Utilisation obsolète

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_overview"
>title="Utilisation obsolète"
>abstract="OU permet d’identifier la situation dans laquelle certains nœuds JCR, tels que Sling, les composants AEM ou les exportations OSGi de l’API, sont modifiés ou supprimés d’une manière non compatible. Il est possible que les clientes et clients ne se rendent pas compte de cette modification avant une mise à niveau. Ils peuvent être mis à niveau vers une version non compatible ou ne pas être disponibles du tout."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Changements notables - AEM as a Cloud Service"

`OU` identifie la situation dans laquelle certains nœuds JCR, tels que des composants Sling ou AEM ou des exports OSGi d’API, sont modifiés ou supprimés d’une manière non compatible. Il est possible que les clientes et clients ne se rendent pas compte de cette modification avant une mise à niveau. Ils peuvent être mis à niveau vers une version non compatible ou ne pas être disponibles du tout.

Comme les anciennes versions ne sont pas installées par défaut, l’application du client risque de ne pas fonctionner correctement.

## Enjeux et risques possibles {#implications-and-risks}

* La fonctionnalité qui dépend de tout composant utilisant des composants ou des API obsolètes peut être défaillante et ne pas être résolue correctement après une mise à niveau.
* Certaines fonctionnalités de l’application cliente ou certaines fonctionnalités AEM peuvent ne pas fonctionner correctement ou ne pas être actives après une mise à niveau.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_guidance"
>title="Guide de mise en œuvre"
>abstract="Il est recommandé de revoir et d’adapter le code client pour lui permettre d’utiliser la dernière version des composants ou des API AEM. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API du SDK Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Court terme : l’installation d’un package de compatibilité peut s’avérer utile.
* À long terme : adaptez le code client pour utiliser la dernière version des composants ou des API AEM.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
