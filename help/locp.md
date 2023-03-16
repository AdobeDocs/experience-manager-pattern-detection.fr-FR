---
title: LOCP
description: Page d’aide sur le code de la détection des motifs
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 100%

---

# LOCP {#locp}

/libs Overwriting Custom Packages (remplacement de packages personnalisés dans /libs)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages (remplacement de packages personnalisés dans /libs)"
>abstract="LOCP identifie la détection d’un package personnalisé qui livre du contenu dans /libs, qui est antimodèle (sauf dans le cas des ACL)."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=fr" text="Mises à niveau possibles"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=fr#platform" text="Fusion des ressources Sling"

`LOCP` identifie la détection d’un package personnalisé qui livre du contenu à `/libs`, qui est antimodèle (sauf dans le cas des ACL).

## Enjeux et risques possibles {#implications-and-risks}

* Le code client peut être supprimé ou remplacé pour tout Service Pack, pack de correctifs cumulés ou mise à niveau majeure d’AEM.
* Dans certains cas, le nouveau contenu peut ne pas s’installer correctement.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Guide de mise en œuvre"
>abstract="Les clients doivent consulter leur code et leurs packages personnalisés afin de déterminer si le contenu est distribué à /libs et le refactoriser pour qu’il repose sur le recouvrement du contenu dans /apps et le rendre compatible avec AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=fr#platform" text="Recouvrements"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Les packages clients doivent déployer leur contenu sur `/apps` au lieu de `/libs`.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
