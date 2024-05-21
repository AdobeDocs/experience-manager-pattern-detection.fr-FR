---
title: LOCP
description: Page d’aide sur le code de détection des motifs.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 65%

---

# LOCP {#locp}

/libs Overwriting Custom Packages (remplacement de packages personnalisés dans /libs)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages (remplacement de packages personnalisés dans /libs)"
>abstract="LOCP identifie la détection d’un module personnalisé qui diffuse du contenu à `/libs`, qui est un anti-motif (sauf s’il existe des listes de contrôle d’accès)."
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
>abstract="Les clients doivent consulter leur code personnalisé et leurs modules pour déterminer si du contenu est diffusé à `/libs`. Si nécessaire, refactorisez-le pour qu’il repose sur le recouvrement du contenu sous /apps et le rende compatible avec AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Recouvrements"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Les packages clients doivent déployer leur contenu sur `/apps` au lieu de `/libs`.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
