---
title: UMI
description: Page d’aide sur le code de la détection des motifs
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '0'
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
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config` : déterminez si la propriété `org.apache.sling.commons.log.file` des enregistreurs personnalisés pointe vers autre chose que le fichier `logs/error.log`.

## Enjeux et risques possibles {#implications-and-risks}

* La modification ou la suppression de configurations peut provoquer les problèmes suivants :
   * La mise à niveau peut être bloquée (par exemple, `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` était absent, mais présent dans `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Des problèmes d’autorisation peuvent survenir après la mise à niveau (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Certaines fonctionnalités peuvent ne pas fonctionner comme prévu. Par exemple, la modification de `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` peut entraîner la non-compilation de certains fichiers JSP, ce qui entraîne une perte de fonctionnalités.
   * Les valeurs de la configuration `com.day.cq.commons.impl.ExternalizerImpl` d’Externalizer sont définies par les variables d’environnement de Cloud Manager dans AEM as a Cloud Service.
   * AEM as a Cloud Service ne prend pas en charge les fichiers journaux personnalisés. Les journaux écrits dans des journaux dont le nom est personnalisé ne seront pas accessibles à partir d’AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons de passer en revue vos configurations actuelles et d’annuler toute modification apportée aux configurations mentionnées afin d’éviter tout problème de mise à niveau ultérieur. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Ne modifiez et ne supprimez pas les quatre configurations mentionnées ci-dessus.
   * Dans le cas de la violation suivante :\
     « Les propriétés requises pour la configuration OSGi “xyz-configuration” sont manquantes : “[property-1, property-2...]”. »\
     Veuillez confirmer la légitimité de ces suppressions. Ces configurations OSGI sont en effet prêtes à l’emploi et peuvent ne jamais avoir été modifiées/enregistrées à partir du gestionnaire de configuration OSGi.
* Si les configurations ont été modifiées, elles doivent être restaurées avec les valeurs attendues. Ces valeurs sont indiquées dans les messages `UMI`.
* Pour `com.day.cq.commons.impl.ExternalizerImpl`, reportez-vous à la [documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/externalizer.html?lang=fr) pour définir la configuration d’Externalizer à l’aide des variables d’environnement de Cloud Manager dans AEM as a Cloud Service.
* Pour `org.apache.sling.commons.log.LogManager.factory.config`, modifiez la configuration OSGI pour envoyer l’enregistreur personnalisé au fichier `logs/error.log`. Veuillez consulter la [documentation](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs.html?lang=fr) pour le repointage vers le fichier `logs/error.log`.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
