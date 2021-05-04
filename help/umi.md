---
title: UMI
description: Page d’aide sur le code de la détection des motifs
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
translation-type: tm+mt
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 70%

---

# UMI {#umi}

Upgrade Misconfiguration Issue (problème de configuration de la mise à niveau)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Upgrade Misconfiguration Issue (problème de configuration de la mise à niveau)"
>abstract="UMI identifie les modifications apportées à certaines configurations OSGi qui provoqueront des problèmes lors de la mise à niveau, y compris une mise à niveau ayant échoué ou une fonctionnalité réduite."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=fr" text="Changements notables - AEM en tant que Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr" text="AEM en tant que Cloud Service - Notes de mise à jour"

`UMI` identifie les modifications apportées à certaines configurations OSGi qui provoqueront des problèmes lors de la mise à niveau, y compris une mise à niveau ayant échoué ou une fonctionnalité réduite.

Les configurations suivantes sont vérifiées pour modification :
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## Enjeux et risques possibles {#implications-and-risks}

* La modification ou la suppression de configurations peut provoquer les problèmes suivants :
   * La mise à niveau peut être bloquée (par exemple, `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` était absent, mais présent dans `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Des problèmes d’autorisation peuvent survenir après la mise à niveau (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Certaines fonctionnalités peuvent ne pas fonctionner comme prévu. Par exemple, la modification de `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` peut entraîner la non-compilation de certains fichiers JSP, ce qui entraîne une perte de fonctionnalités.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Guide de mise en oeuvre"
>abstract="La meilleure pratique consiste à revoir vos configurations actuelles et à rétablir les modifications apportées aux configurations mentionnées afin d’éviter tout problème de mise à niveau ultérieure. Contactez l&#39;assistance Adobe pour obtenir de l&#39;aide et des éclaircissements"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Ne modifiez pas et ne supprimez pas les quatre configurations mentionnées ci-dessus.
* Si les configurations ont été modifiées, elles doivent être restaurées avec les valeurs attendues. Ces valeurs sont indiquées dans les messages `UMI`.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
