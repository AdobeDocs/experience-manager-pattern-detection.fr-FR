---
title: CAV
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 45%

---

# CAV {#cav}

Content Area Violation (violation de zone de contenu)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Content Area Violation (violation de zone de contenu)"
>abstract="Le code CAV identifie le modèle selon lequel différentes zones de contenu sont utilisées d’une façon qui enfreint les règles de la classification de contenu. Cette violation vous donnerait un aperçu des superpositions, du contenu restreint qui peut nécessiter d’être modifié une fois qu’il est déplacé vers AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Fusion des ressources Sling"

`CAV` Identifie le modèle dans lequel différentes zones de contenu sont utilisées d’une manière qui viole les règles de la classification de contenu.

Le traitement des requêtes Sling définit la manière dont le contenu d’une ressource, sa `sling:resourceType` en particulier, est utilisée pour déterminer le script utilisé pour effectuer le rendu du contenu. Voir [Localisation du script](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) pour plus d’informations. Sling fournit également des techniques permettant d’accéder aux ressources et de les fusionner par le biais des superpositions et des remplacements. Ils sont décrits comme faisant partie de [Sling Resource Merger](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) et des [Superpositions](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Pour que les clients puissent comprendre plus facilement et plus en toute sécurité les zones d’ `/libs` peuvent utiliser et superposer le contenu en toute sécurité dans `/libs` a été classé avec des propriétés &quot;mixin&quot; : Public, Abstract, Final et Interne. Chaque classification implique des règles sur la manière dont le contenu peut être utilisé, hérité ou superposé. Voir [Mise à niveau durable](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) pour une description détaillée.

## Enjeux et risques possibles {#implications-and-risks}

* Une mise à niveau d’AEM peut entraîner des problèmes de rendu de page et d’autres comportements indésirables.
* Les mises à jour de sécurité ne sont pas efficaces.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Guide de mise en œuvre"
>abstract="Les modèles identifiés avec le CAS où il existe différentes violations de zones de contenu doivent être examinés. Les zones de classification de contenu final et interne doivent être évitées. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Mises à niveau possibles"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Réduisez l’utilisation de la superposition de contenu aux cas où elle est nécessaire.
* En particulier, évitez de superposer le contenu restreint (classification Finale et Interne).
* Envisagez d’adapter les changements issus de `/libs` après AEM mises à niveau, installations Service Pack ou Cumulative Fix Pack.
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
