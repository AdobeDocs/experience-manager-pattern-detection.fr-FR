---
title: UMI
description: Page d’aide sur le code de détection des motifs.
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 87%

---

# UMI {#umi}

Problème de mauvaise configuration de la mise à niveau

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problème de mauvaise configuration de la mise à niveau"
>abstract="UMI identifie les modifications apportées à certaines configurations OSGi qui provoquent des problèmes lors de la mise à niveau, y compris une mise à niveau ayant échoué ou une fonctionnalité réduite."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Changements notables - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Notes de mise à jour"

`UMI` identifie les modifications apportées à certaines configurations OSGi qui provoquent des problèmes lors de la mise à niveau, notamment l’échec d’une mise à niveau ou la limitation d’une fonctionnalité.

Les configurations suivantes sont vérifiées pour modification :

* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config` : déterminez si la propriété `org.apache.sling.commons.log.file` des enregistreurs personnalisés pointe vers un fichier autre que `logs/error.log`.

## Implications et risques éventuels {#implications-and-risks}

* La modification ou la suppression de configurations peut entraîner les problèmes suivants :
   * La mise à niveau peut être bloquée (par exemple, `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` était absent, mais présent dans `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Des problèmes d’autorisation peuvent survenir après la mise à niveau (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Certaines fonctionnalités peuvent ne pas fonctionner comme prévu. Par exemple, la modification de `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` peut entraîner la non-compilation de certains fichiers JSP, ce qui entraîne une perte de fonctionnalités.
   * Les valeurs de la configuration de l’externaliseur `com.day.cq.commons.impl.ExternalizerImpl` sont définies avec des variables d’environnement de gestionnaire de cloud dans AEM as a Cloud Service.
   * AEM as a Cloud Service ne prend pas en charge les fichiers journaux personnalisés. Les journaux écrits dans des journaux dont le nom est personnalisé ne sont pas accessibles à partir d’AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons de passer en revue vos configurations actuelles et d’annuler toute modification apportée aux configurations mentionnées afin d’éviter tout problème de mise à niveau ultérieur. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Ne modifiez et ne supprimez pas les quatre configurations mentionnées ci-dessus.
   * Dans le cas de la violation suivante :\
     « Les propriétés requises pour la configuration OSGi `xyz-configuration` sont manquantes : “[property-1,property-2...]”. »\
     Confirmez la légitimité de ces suppressions car ces configurations OSGI sont prêtes à l’emploi et peuvent ne jamais avoir été modifiées/enregistrées à partir du gestionnaire de configuration OSGi.
* Si les configurations ont été modifiées, elles doivent être restaurées avec les valeurs attendues. Ces valeurs sont indiquées dans les messages `UMI`.
* Pour `com.day.cq.commons.impl.ExternalizerImpl`, reportez-vous à la [documentation](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) pour définir la configuration d’Externalizer à l’aide des variables d’environnement de Cloud Manager dans AEM as a Cloud Service.
* Pour `org.apache.sling.commons.log.LogManager.factory.config`, modifiez la configuration OSGI pour envoyer l’enregistreur personnalisé au fichier `logs/error.log`. Consultez la [documentation](https://experienceleague.adobe.com/fr/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) pour le repointage vers le fichier `logs/error.log`.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
