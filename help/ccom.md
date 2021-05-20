---
title: CCOM
description: Page d’aide sur le code de la détection des motifs
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 100%

---

# CCOM {#ccom}

Custom Component (composant personnalisé)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Custom Component (composant personnalisé)"
>abstract="CCOM identifie les composants personnalisés qui ont été installés sur AEM. Ces renseignements sont fournis afin d’évaluer les bonnes pratiques"

`CCOM` identifie les composants personnalisés qui ont été installés sur AEM. Ces renseignements sont fournis afin d’évaluer les bonnes pratiques.

Un sous-type est utilisé avec ce code pour identifier la catégorie du composant :

* `custom.core` : un supertype de la chaîne de supertypes du composant contient « core/wcm/components/ », ce qui indique qu’il est hérité d’un composant principal.
* `custom.foundation` : un supertype de la chaîne de supertypes du composant contient « core/wcm/components/ », ce qui indique qu’il est hérité d’un composant principal.
* `custom.overlay.foundation` : le chemin du composant contient « wcm/foundation/components/ » ou « foundation/components/ », ce qui indique qu’il se superpose sur un composant de base.
* `custom` : le composant personnalisé n’hérite ni ne se superpose sur aucun composant principal ou de base.

## Enjeux et risques possibles {#implications-and-risks}

* La bonne pratique consiste à réduire au minimum le nombre de composants personnalisés, à tirer profit des composants principaux et à les utiliser avec le système de style pour réduire la dette technique.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Guide de mise en œuvre"
>abstract="La bonne pratique consiste à réduire au minimum le nombre de composants personnalisés, à tirer profit des composants principaux et à les utiliser avec le système de style pour réduire la dette technique."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="Composants principaux"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring" text="Système de style"

* Pour plus d’informations sur les composants principaux, consultez [Présentation des composants principaux](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=fr).
* Pour plus d’informations sur le système de style, consultez [Utilisation du système de style](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=fr#page-authoring).
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
