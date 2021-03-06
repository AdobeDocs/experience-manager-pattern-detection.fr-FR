---
title: ACV
description: Page d’aide sur le code de la détection des motifs
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 09e6149b971dc975dff517d98f8b2faaa8138b51
workflow-type: ht
source-wordcount: '310'
ht-degree: 100%

---

# ACV {#acv}

Programme de validation de contenu des ressources

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Programme de validation de contenu des ressources"
>abstract="ACV identifie les nœuds obligatoires manquants dans le contenu des ressources."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html?lang=fr" text="Modifications notables – Experience Manager en tant que Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr" text="Experience Manager en tant que Cloud Service – Notes de mise à jour"

Le programme de validation de contenu des ressources `ACV` identifie les nœuds obligatoires manquants et les infractions dans le contenu des ressources. Cela peut entraîner l’échec de certaines fonctionnalités d’Assets sur Experience Manager as a Cloud Service.

Des sous-types sont utilisés pour identifier les différents types d’informations, notamment :

* `missing.jcrcontent` : identifier les dossiers comportant des nœuds obligatoires manquants dans le référentiel. L’identification de tout contenu manquant dans le référentiel permet d’éviter les fonctionnalités ou les cas d’utilisation rompus.
* `missing.original.rendition` : identifier les ressources comportant des nœuds obligatoires manquants dans le référentiel.
* `metadata.descendants.violation` : identifier les ressources avec plus de 100 descendants sous le nœud de métadonnées de la ressource dans le référentiel.

## Enjeux et risques possibles {#implications-and-risks}

* Cela peut entraîner l’échec de certaines fonctionnalités d’Assets qui dépendent de propriétés héritées sur Experience Manager as a Cloud Service.
* AEM Assets dépend de l’existence du rendu original. Le traitement de la ressource dans Cloud Service va rentrer dans une boucle si le rendu original est absent.
* Un grand nombre de descendants sous le nœud de métadonnées peut ralentir le chargement de dossiers composés de ressources qui enfreignent cette règle.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Guide de mise en œuvre"
>abstract="Adobe recommande de passer en revue la structure de contenu pour éviter les workflows rompus qui dépendent de propriétés héritées. Contactez l’assistance clientèle pour obtenir de l’aide."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Analysez un dossier s’il manque un nœud enfant. Créez les nœuds manuellement si le nombre de dossiers est gérable. Sinon, utilisez un script.
* Pour les ressources auxquelles il manque le rendu original, vous pouvez, au choix, télécharger de nouveau les ressources ou les supprimer avant d’effectuer une migration.
* Contactez notre [équipe d’assistance clientèle Experience Manager](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou pour répondre à vos préoccupations.
