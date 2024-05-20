---
title: CCOM
description: Page d’aide sur le code de détection des motifs.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 60%

---

# CCOM {#ccom}

Custom Component (composant personnalisé)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Custom Component (composant personnalisé)"
>abstract="CCOM identifie les composants personnalisés installés sur AEM. Ces renseignements sont fournis afin d’évaluer les bonnes pratiques"

`CCOM` Identifie les composants personnalisés installés sur AEM. Ces informations sont fournies afin d’évaluer les bonnes pratiques.

Un sous-type est utilisé avec ce code pour identifier la catégorie du composant :

* `custom.core`: un supertype dans la chaîne de supertypes du composant contient `core/wcm/components/`, indiquant qu’il hérite d’un composant principal.
* `custom.foundation`: un supertype de la chaîne de supertypes du composant contient &quot;`core/wcm/components/`, indiquant qu’il hérite d’un composant principal.
* `custom.overlay.foundation`: le chemin d’accès au composant contient `wcm/foundation/components/` ou `foundation/components/`, indiquant qu’il incruste un composant de base.
* `custom` : le composant personnalisé n’hérite ni ne se superpose sur aucun composant principal ou de base.

## Enjeux et risques possibles {#implications-and-risks}

* La bonne pratique consiste à réduire le nombre de composants personnalisés, à utiliser les composants principaux et à utiliser les composants principaux avec le système de style afin de réduire la dette technique.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Guide de mise en œuvre"
>abstract="La bonne pratique consiste à réduire au minimum le nombre de composants personnalisés, à utiliser des composants principaux et à les utiliser avec le système de style pour réduire la dette technique."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-core-components/using/introduction" text="Composants principaux"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring" text="Système de style"

* Pour plus d’informations sur les composants principaux, consultez [Présentation des composants principaux](https://experienceleague.adobe.com/fr/docs/experience-manager-core-components/using/introduction).
* Pour plus d’informations sur le système de style, consultez [Utilisation du système de style](https://experienceleague.adobe.com/fr/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring).
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
