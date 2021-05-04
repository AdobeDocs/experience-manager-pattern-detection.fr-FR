---
title: CTEM
description: Page d’aide sur le code de la détection des motifs
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 67%

---

# CTEM {#ctem}

Modèle personnalisé

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Modèle personnalisé"
>abstract="CTEM identifie les composants personnalisés qui ont été installés sur AEM. Ces renseignements sont fournis afin d’évaluer les bonnes pratiques"

`CTEM` identifie les modèles personnalisés qui ont été installés sur AEM. Ces renseignements sont fournis afin d’évaluer les bonnes pratiques.

Les modèles sont identifiés par une valeur principale de type « cq:Template ». Un sous-type est utilisé avec ce code pour identifier la catégorie du modèle :

* `custom.editable.template` : le chemin d’accès du modèle ne commence pas par « /apps ».
* `custom.static.template` : le chemin d’accès du modèle commence par « /apps ».

## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Guide de mise en oeuvre"
>abstract="La bonne pratique consiste à changer tous les modèles statiques en modèles modifiables. Les clients peuvent utiliser les outils de modernisation des AEM existants pour migrer les modèles statiques vers des modèles modifiables."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html" text="Modèles modifiables"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Outils de modernisation d’AEM"

* La bonne pratique consiste à changer tous les modèles statiques en modèles modifiables.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Outils et ressources"
>abstract="Grâce à AEM Modernisation Suite, les clients peuvent manipuler la structure d&#39;une page d&#39;une définition statique à un modèle modifiable. L&#39;objectif est d&#39;aider les clients à passer des capacités limitées des fonctionnalités héritées aux offres d&#39;AEM robustes et modernes. Ces outils sont configurables, adaptés à la configuration et extensibles. Contactez l&#39;assistance Adobe pour obtenir de l&#39;aide et des éclaircissements"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/page-structure.html" text="Convertisseur de structure de page"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Tirez profit des [Outils de modernisation d’AEM](https://opensource.adobe.com/aem-modernize-tools/) pour migrer des modèles statiques vers des modèles modifiables.
* Pour plus d’informations sur les modèles modifiables, consultez [Modèles](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=fr).
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
