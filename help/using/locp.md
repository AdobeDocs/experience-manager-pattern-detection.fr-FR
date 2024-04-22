---
title: LOCP
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 61%

---

# LOCP {#locp}

/libs Overwriting Custom Packages (remplacement de packages personnalisés dans /libs)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages (remplacement de packages personnalisés dans /libs)"
>abstract="LOCP identifie la détection d’un package personnalisé qui livre du contenu dans /libs, qui est antimodèle (sauf dans le cas des ACL)."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Mises à niveau possibles"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Fusion des ressources Sling"

LOCP identifie la détection d’un module personnalisé qui diffuse du contenu à `/libs`, qui est un anti-modèle (sauf dans le cas des listes de contrôle d’accès).

## Enjeux et risques possibles {#implications-and-risks}

* Le code client peut être supprimé ou remplacé pour toute mise à niveau de CFP, de SP ou d’AEM majeure.
* Il arrive que le nouveau contenu ne soit pas correctement installé.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Guide de mise en œuvre"
>abstract="Les clients doivent consulter leur code et leurs packages personnalisés afin de déterminer si le contenu est distribué à /libs et le refactoriser pour qu’il repose sur le recouvrement du contenu dans /apps et le rendre compatible avec AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Recouvrements"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Les packages clients doivent déployer leur contenu sur `/apps` au lieu de `/libs`.
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si des clarifications ou des préoccupations s’imposent.
