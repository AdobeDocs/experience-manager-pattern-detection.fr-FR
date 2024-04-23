---
title: CTEM
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 68%

---

# CTEM {#ctem}

Modèle personnalisé

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Modèle personnalisé"
>abstract="CTEM identifie les composants personnalisés qui ont été installés sur AEM. Ces renseignements sont fournis afin d’évaluer les bonnes pratiques"

CTEM identifie les modèles personnalisés qui ont été installés sur AEM. Ces renseignements sont fournis afin d’évaluer les bonnes pratiques.

Les modèles sont identifiés par une valeur de type principal de `cq:Template`. Un sous-type est utilisé avec ce code pour identifier la catégorie du modèle :

* `custom.editable.template` : le chemin d’accès du modèle ne commence pas par « /apps ».
* `custom.static.template` : le chemin d’accès du modèle commence par « /apps ».

## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Guide de mise en œuvre"
>abstract="La bonne pratique consiste à changer tous les modèles statiques en modèles modifiables. Les clients peuvent utiliser les outils de modernisation d’AEM existants pour migrer des modèles statiques vers des modèles modifiables."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates" text="Modèles modifiables"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Outils de modernisation d’AEM"

* La bonne pratique consiste à changer tous les modèles statiques en modèles modifiables.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Outils et ressources"
>abstract="Grâce aux outils de modernisation AEM, les clients peuvent modifier la structure d’une page dotée d’une définition statique pour la transformer en modèle modifiable. L’objectif est d’aider les clients à abandonner les capacités limitées des fonctionnalités héritées pour adopter les fonctionnalités AEM, plus efficaces et modernes. Ces outils sont configurables, configurables et extensibles. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/structure/about.html" text="Convertisseur de structure de page"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Utilisez la variable [Outils de modernisation d’AEM](https://opensource.adobe.com/aem-modernize-tools/) pour migrer des modèles statiques vers des modèles modifiables.
* Pour plus d’informations sur les modèles modifiables, consultez [Modèles](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates).
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
