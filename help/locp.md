---
title: LOCP
description: Page d’aide sur le code de la détection des motifs
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 55%

---

# LOCP {#locp}

/libs Overwriting Custom Packages (remplacement de packages personnalisés dans /libs)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages (remplacement de packages personnalisés dans /libs)"
>abstract="LOCP identifie la détection d&#39;un package personnalisé qui livre du contenu à /libs, qui est un anti-modèle (sauf dans le cas des ACL)."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=fr" text="Mises à niveau possibles"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Fusionner les ressources Sling"

`LOCP` identifie la détection d’un package personnalisé qui livre du contenu à `/libs`, qui est antimodèle (sauf dans le cas des ACL).

## Enjeux et risques possibles {#implications-and-risks}

* Le code client peut être supprimé ou remplacé pour tout Service Pack, pack de correctifs cumulés ou mise à niveau majeure d’AEM.
* Dans certains cas, le nouveau contenu peut ne pas s’installer correctement.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Guide de mise en oeuvre"
>abstract="Les clients doivent consulter leur code et leurs packages personnalisés pour déterminer si le contenu est distribué à /libs et le refactoriser pour qu’il repose sur l’incrustation du contenu sous /apps et le rendre compatible avec AEM en tant que Cloud Service. Contactez l&#39;assistance Adobe pour obtenir de l&#39;aide et des éclaircissements"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Recouvrements"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Les packages clients doivent déployer leur contenu sur `/apps` au lieu de `/libs`.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
