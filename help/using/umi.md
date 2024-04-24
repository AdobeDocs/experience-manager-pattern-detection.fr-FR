---
title: UMI
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 41%

---

# UMI {#umi}

Upgrade Misconfiguration Issue (problème de configuration de la mise à niveau)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Upgrade Misconfiguration Issue (problème de configuration de la mise à niveau)"
>abstract="UMI identifie les modifications apportées à certaines configurations OSGi qui provoquent des problèmes lors de la mise à niveau, y compris une mise à niveau ou une fonctionnalité réduite ayant échoué."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Changements notables – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service – Notes de mise à jour"

`UMI`  Identifie les modifications apportées à certaines configurations OSGi qui provoquent des problèmes lors de la mise à niveau, y compris une mise à niveau ayant échoué ou une fonctionnalité réduite.

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
   * Certaines fonctionnalités peuvent ne pas fonctionner comme prévu. Par exemple, changer `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` Il se peut que certains fichiers JSP ne soient pas compilés, ce qui entraîne une perte de fonctionnalité.
   * Les valeurs de la configuration de l’externaliseur `com.day.cq.commons.impl.ExternalizerImpl` sont définies par les variables d’environnement de cloud manager dans AEM as a Cloud Service.
   * AEM as a Cloud Service ne prend pas en charge les fichiers journaux personnalisés. Les journaux écrits dans des journaux personnalisés ne sont pas accessibles depuis AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Guide de mise en œuvre"
>abstract="La bonne pratique consiste à passer en revue vos configurations actuelles et à rétablir toute modification apportée aux configurations mentionnées afin d’éviter tout problème de mise à niveau ultérieure. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Ne modifiez et ne supprimez pas les quatre configurations mentionnées ci-dessus.
   * En cas de violation suivante :\
     &quot;Propriétés requises pour la configuration OSGi `xyz-configuration` sont manquantes : &#39;[property-1,property-2...]&#39;.&quot;\
     Confirmez si ces suppressions sont légitimes ou non, car ces configurations OSGI sont prêtes à l’emploi et peuvent ne jamais avoir été modifiées/enregistrées à partir du gestionnaire de configuration OSGi.
* Si les configurations ont été modifiées, elles doivent être restaurées avec les valeurs attendues. Ces valeurs sont indiquées dans les messages `UMI`.
* Pour `com.day.cq.commons.impl.ExternalizerImpl`, voir [documentation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) pour définir la configuration de l’externaliseur à l’aide des variables d’environnement de cloud manager dans AEM as a Cloud Service.
* Pour `org.apache.sling.commons.log.LogManager.factory.config`, modifiez la configuration OSGI pour envoyer l’enregistreur personnalisé au fichier `logs/error.log`. Voir [documentation](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) pour indiquer à la fonction `logs/error.log` fichier .
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
