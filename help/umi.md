---
title: UMI
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: ht
source-wordcount: '145'
ht-degree: 100%

---


# UMI {#umi}

Upgrade Misconfiguration Issue (problème de configuration de la mise à niveau)

## Arrière-plan {#background}

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

* Ne modifiez pas et ne supprimez pas les quatre configurations mentionnées ci-dessus.
* Si les configurations ont été modifiées, elles doivent être restaurées avec les valeurs attendues. Ces valeurs sont indiquées dans les messages `UMI`.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
