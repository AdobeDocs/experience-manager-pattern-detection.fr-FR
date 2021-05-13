---
title: UMI
description: Page d’aide sur le code de la détection des motifs
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
translation-type: ht
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: ht
source-wordcount: '234'
ht-degree: 100%

---

# UMI {#umi}

Upgrade Misconfiguration Issue (problème de configuration de la mise à niveau)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Upgrade Misconfiguration Issue (problème de configuration de la mise à niveau)"
>abstract="UMI identifie les modifications apportées à certaines configurations OSGi qui provoqueront des problèmes lors de la mise à niveau, y compris une mise à niveau ayant échoué ou une fonctionnalité réduite."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=fr" text="Changements notables – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr" text="AEM as a Cloud Service – Notes de mise à jour"

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
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons de passer en revue vos configurations actuelles et d’annuler toute modification apportée aux configurations mentionnées afin d’éviter tout problème de mise à niveau ultérieur. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Ne modifiez pas et ne supprimez pas les quatre configurations mentionnées ci-dessus.
* Si les configurations ont été modifiées, elles doivent être restaurées avec les valeurs attendues. Ces valeurs sont indiquées dans les messages `UMI`.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
