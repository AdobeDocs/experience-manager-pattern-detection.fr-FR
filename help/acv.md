---
title: ACV
description: Page d’aide sur le code de la détection des motifs
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 0a6b0f8f2b64bf1c966b8f282a2205f2772afe3f
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 100%

---

# ACV {#acv}

Programme de validation de contenu des ressources

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Programme de validation de contenu des ressources"
>abstract="ACV identifie les nœuds obligatoires manquants dans le contenu des ressources."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html?lang=fr" text="Modifications notables – Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr" text="Experience Manager as a Cloud Service – Notes de mise à jour"

Le programme de validation de contenu des ressources `ACV` identifie les nœuds obligatoires manquants et les infractions dans le contenu des ressources. Cela peut entraîner l’échec de certaines fonctionnalités d’Assets sur Experience Manager as a Cloud Service.

Des sous-types sont utilisés pour identifier les différents types d’informations, notamment :

* `missing.jcrcontent` : identifier les dossiers comportant des nœuds obligatoires manquants dans le référentiel. L’identification de tout contenu manquant dans le référentiel permet d’éviter les fonctionnalités ou les cas d’utilisation rompus.
* `missing.original.rendition` : identifier les ressources comportant des rendus obligatoires manquants dans le référentiel. Notez que la prévisualisation des pages du PDF ne nécessite pas de génération de sous-ressources dans AEMaaCS. Par conséquent, pour les ressources de PDF, le signalement des rendus originaux manquants dans les sous-ressources est supprimé.
* `metadata.descendants.violation` : identifier les ressources avec plus de 100 descendants sous le nœud de métadonnées de la ressource dans le référentiel.
* `conflict.node` : identifier la présence de nœuds de conflit dans le référentiel sous /content/dam/.

## Enjeux et risques possibles {#implications-and-risks}

* Cela peut entraîner l’échec de certaines fonctionnalités d’Assets qui dépendent de propriétés héritées sur Experience Manager as a Cloud Service.
* AEM Assets dépend de l’existence du rendu original. Le traitement de la ressource dans Cloud Service va rentrer dans une boucle si le rendu original est absent. La génération de sous-ressources n’est pas prise en charge dans AEMaaCS.
* Un grand nombre de descendants sous le nœud de métadonnées peut ralentir le chargement de dossiers composés de ressources qui enfreignent cette règle.
* La présence de nœuds de conflit peut entraîner un échec de l’ingestion sur AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Guide de mise en œuvre"
>abstract="Adobe recommande de passer en revue la structure de contenu pour éviter les workflows rompus qui dépendent de propriétés héritées. Contactez l’assistance clientèle pour obtenir de l’aide."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Analysez un dossier s’il manque un nœud enfant. Créez les nœuds manuellement si le nombre de dossiers est gérable. Sinon, utilisez un script.
* Pour les ressources auxquelles il manque le rendu original, vous pouvez, au choix, télécharger de nouveau les ressources ou les supprimer avant d’effectuer une migration.
* Aucune action n’est requise pour le rendu original des sous-ressources manquantes.
* En cas de conflit, les nœuds doivent être résolus ou supprimés avant la migration vers AEM as a Cloud Service.
* Contactez notre [équipe d’assistance clientèle Experience Manager](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des explications ou pour répondre à vos préoccupations.
