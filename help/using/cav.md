---
title: CAV
description: Page d’aide sur le code de détection des motifs.
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: ht
source-wordcount: '316'
ht-degree: 100%

---

# CAV {#cav}

Content Area Violation (violation de zone de contenu)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Content Area Violation (violation de zone de contenu)"
>abstract="Le code CAV identifie le modèle selon lequel différentes zones de contenu sont utilisées d’une façon qui enfreint les règles de la classification de contenu. Cette violation vous donnerait une vue d’ensemble des recouvrements et du contenu restreint qui pourrait nécessiter des modifications lors de la migration vers AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Fusion des ressources Sling"

`CAV` identifie le modèle dans lequel différentes zones de contenu sont utilisées d’une façon qui enfreint les règles de classification de contenu.

Le traitement des requêtes Sling définit la façon dont le contenu d’une ressource, en particulier sa propriété `sling:resourceType`, est utilisé pour déterminer le script à utiliser pour le rendu du contenu. Voir [Localisation du script](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) pour plus d’informations. Sling fournit également des techniques permettant d’accéder aux ressources et de les fusionner par le biais des recouvrements et des remplacements. Ces techniques sont décrites comme faisant partie de [Sling Resource Merger](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) et des [recouvrements](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Pour permettre aux personnes de mieux comprendre les zones de `/libs` qui peuvent être utilisées et recouvertes en toute sécurité, le contenu de `/libs` a été classé avec les propriétés « Mixin » :

* Public
* Résumé
* Final
* Interne

Chaque classification implique des règles sur la manière dont le contenu peut être utilisé, hérité ou superposé. Voir [Mise à niveau durable](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) pour une description détaillée.

## Enjeux et risques possibles {#implications-and-risks}

* Une mise à niveau d’AEM peut entraîner des problèmes de rendu de page et d’autres comportements indésirables.
* Les mises à jour de sécurité ne sont pas efficaces.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous recommandons d’examiner les motifs identifiés avec le CAS contenant différentes violations de la zone de contenu. Les zones de classification de contenu final et interne doivent être évitées. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Mises à niveau possibles"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Réduisez l’utilisation de la superposition de contenu aux cas où elle est nécessaire.
* En particulier, évitez de superposer le contenu restreint (classification Finale et Interne).
* Envisagez d’adapter les changements issus de `/libs` après les mises à niveau d’AEM, les installations du pack de services ou du pack de correctifs cumulatif.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
