---
title: IOI
description: Page d’aide sur le code de la détection des motifs
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 78%

---

# IOI {#ioi}

Internal Oak Import (importation Oak interne)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Internal Oak Import (importation Oak interne)"
>abstract="Le code IOI identifie l&#39;utilisation par le client des paquets internes Oak, en les important via OSGi. Ils sont généralement exportés sans aucune version particulière et sont uniquement destinés à une consommation par d’autres lots Oak ou des services AEM de bas niveau."

`IOI` identifie l’utilisation par le client de packages Oak internes, en les important via OSGi. Ils sont généralement exportés sans aucune version particulière et sont uniquement destinés à une consommation par d’autres lots Oak ou des services AEM de bas niveau.

Certains d’entre eux sont utilisés par `com.adobe.granite.repository`, qui installe un référentiel pour AEM au démarrage. Un autre exemple est le lot Adobe `com.adobe.granite.maintenance.oak`, qui englobe et fournit des tâches de maintenance Oak.

## Enjeux et risques possibles {#implications-and-risks}

* Dans une future version d’AEM, les exportations internes pourraient être supprimées, ce qui provoquerait des problèmes de dépendances brisées et des lots inactifs dépendant directement d’Oak.
* L’API dans les exportations internes peut changer.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Guide de mise en oeuvre"
>abstract="Les clients doivent revoir leur code personnalisé pour identifier l’utilisation de ces API et les reconsidérer pour les rendre compatibles avec AEM en tant que Cloud Service. Contactez l&#39;assistance Adobe pour obtenir de l&#39;aide et des éclaircissements"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Utilisez l’API Sling Resource (ou l’API JCR) au lieu d’un accès de bas niveau.
* Évitez de dépendre de packages internes qui ne font partie d’aucune API ou SPI publique.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
