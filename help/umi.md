---
title: UMI
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# UMI {#umi}

Problème de configuration de la mise à niveau

## Arrière-plan {#background}

`UMI` identifie les modifications apportées à certaines configurations OSGi qui provoqueront des problèmes lors de la mise à niveau, y compris une mise à niveau ayant échoué ou une fonctionnalité réduite.

Les configurations suivantes sont vérifiées pour modification :
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## Incidences possibles et risques {#implications-and-risks}

* La modification ou la suppression de configurations peut provoquer les problèmes suivants :
   * La mise à niveau peut être bloquée (par exemple, `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` était absent mais présent dans `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Les problèmes d’autorisation peuvent survenir après la mise à niveau (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Certaines fonctionnalités peuvent ne pas fonctionner comme prévu. Par exemple, la modification de `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` peut entraîner la non-compilation de certains fichiers JSP, ce qui entraîne en fin de compte la perte de fonctionnalités.

## Solutions possibles {#solutions}

* Ne modifiez pas ou ne supprimez pas les quatre configurations mentionnées ci-dessus.
* Si les configurations ont été modifiées, elles doivent être restaurées à leurs valeurs attendues. Ces valeurs sont indiquées dans les messages `UMI`.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
