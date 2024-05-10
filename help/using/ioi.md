---
title: IOI
description: Page d’aide sur le code de détection des motifs.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '219'
ht-degree: 100%

---

# IOI {#ioi}

Internal Oak Import (import Oak interne)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Internal Oak Import (importation Oak interne)"
>abstract="Le code IOI identifie l’utilisation par le client de packages Oak internes, en les important par OSGi. Ils sont généralement exportés sans version particulière et sont uniquement destinés à une consommation par d’autres lots Oak ou par des services AEM de bas niveau."

`IOI` identifie l’utilisation par le client ou la cliente de packages Oak internes, en les important via OSGi. Ils sont généralement exportés sans version particulière et sont uniquement destinés à une consommation par d’autres lots Oak ou par des services AEM de bas niveau.

Certains d’entre eux sont utilisés par `com.adobe.granite.repository`, qui installe un référentiel pour AEM au démarrage. Un autre exemple est le lot Adobe `com.adobe.granite.maintenance.oak`, qui englobe et fournit des tâches de maintenance Oak.

## Enjeux et risques possibles {#implications-and-risks}

* Dans une future version d’AEM, les exportations internes pourraient être supprimées, ce qui provoquerait des problèmes de dépendances brisées et des lots inactifs dépendant directement d’Oak.
* L’API dans les exportations internes peut changer.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Guide de mise en œuvre"
>abstract="Les clients doivent passer en revue leur code personnalisé pour identifier l’utilisation de ces API et les modifier de telle manière à les rendre compatibles avec AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Utilisez l’API Sling Resource (ou l’API JCR) au lieu d’un accès de bas niveau.
* Évitez de dépendre de packages internes qui ne font partie d’aucune API ou SPI publique.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
