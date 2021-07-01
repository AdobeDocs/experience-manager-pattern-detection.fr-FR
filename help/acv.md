---
title: ACV
description: Page d’aide sur le code de la détection des motifs
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
source-git-commit: d61fbb28fdf91fd9b356654d5cd2d50b156398c4
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 18%

---

# ACV {#acv}

Validateur de contenu des ressources

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Validateur de contenu des ressources"
>abstract="ACV identifie les noeuds obligatoires manquants dans le contenu des ressources."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html?lang=fr" text="Modifications notables - Experience Manager en tant que Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr" text="Experience Manager en tant que Cloud Service - Notes de mise à jour"

`ACV`  La validation du contenu des ressources identifie les noeuds obligatoires manquants dans le contenu des ressources. Cela peut entraîner l’échec de certaines fonctionnalités Assets sur Experience Manager en tant que Cloud Service.

Les sous-types sont utilisés pour identifier les différents types d’informations, tels que :

* `assets.sanity.missing.jcrcontent`: Identifiez les dossiers comportant des noeuds obligatoires manquants dans le référentiel. L’identification de tout contenu manquant dans le référentiel permet d’éviter les fonctionnalités ou les cas d’utilisation rompus.

## Enjeux et risques possibles {#implications-and-risks}

Cela peut entraîner l’échec de certaines fonctionnalités Assets qui dépendent des propriétés héritées en tant que Cloud Service dans Experience Manager.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Guide de mise en œuvre"
>abstract="Adobe recommande de passer en revue la structure de contenu afin d’éviter les workflows rompus qui dépendent de propriétés héritées. Contactez l’assistance clientèle pour obtenir de l’aide.&quot;
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Analysez un dossier s’il manque un noeud enfant. Créez les noeuds manuellement si le nombre de dossiers est gérable, sinon utilisez un script.
* Contactez notre [équipe d’assistance clientèle Experience Manager](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou pour répondre aux préoccupations.
