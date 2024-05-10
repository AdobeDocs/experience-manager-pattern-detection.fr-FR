---
title: LOCP
description: Page d’aide sur le code de détection des motifs.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '169'
ht-degree: 100%

---

# LOCP {#locp}

/libs Overwriting Custom Packages (remplacement de packages personnalisés dans /libs)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages (remplacement de packages personnalisés dans /libs)"
>abstract="LOCP identifie la détection d’un package personnalisé qui livre du contenu dans /libs, qui est antimodèle (sauf dans le cas des ACL)."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Mises à niveau possibles"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Fusion des ressources Sling"

`LOCP` identifie la détection d’un package personnalisé qui diffuse du contenu à `/libs`, ce qui constitue un antipattern (sauf dans le cas des ACL).

## Enjeux et risques possibles {#implications-and-risks}

* Le code client peut être supprimé ou remplacé pour tout pack de services, pack de correctifs cumulatifs ou mise à niveau majeure d’AEM.
* Dans certains cas, le nouveau contenu peut ne pas s’installer correctement.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Guide de mise en œuvre"
>abstract="Les clients doivent consulter leur code et leurs packages personnalisés afin de déterminer si le contenu est distribué à /libs et le refactoriser pour qu’il repose sur le recouvrement du contenu dans /apps et le rendre compatible avec AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Recouvrements"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Les packages clients doivent déployer leur contenu sur `/apps` au lieu de `/libs`.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
