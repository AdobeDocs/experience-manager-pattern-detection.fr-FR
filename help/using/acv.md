---
title: ACV
description: Page d’aide sur le code de détection des motifs.
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: ht
source-wordcount: '475'
ht-degree: 100%

---

# ACV {#acv}

Programme de validation de contenu des ressources

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Programme de validation de contenu des ressources"
>abstract="ACV identifie les nœuds obligatoires manquants dans le contenu des ressources."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/overview" text="Modifications notables - Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Experience Manager as a Cloud Service - Notes de mise à jour"

`ACV` (programme de validation du contenu des ressources) : identifie les nœuds obligatoires manquants et les violations dans le contenu des ressources. Cela pourrait entraîner la défaillance de certaines fonctionnalités d’Assets sur Experience Manager as a Cloud Service.

Des sous-types sont utilisés pour identifier les différents types d’informations, notamment :

* `missing.jcrcontent` : identifier les dossiers comportant des nœuds obligatoires manquants dans le référentiel. L’identification de tout contenu manquant dans le référentiel permet d’éviter les fonctionnalités ou les cas d’utilisation rompus.
* `missing.original.rendition` : identifier les ressources comportant des rendus obligatoires manquants dans le référentiel. La prévisualisation des pages du PDF ne nécessite pas de génération de sous-ressources dans AEMaaCS. Par conséquent, pour les ressources PDF, le signalement des rendus originaux manquants dans les sous-ressources est supprimé.
* `metadata.descendants.violation` : identifier les ressources avec plus de 100 descendants sous le nœud de métadonnées de la ressource dans le référentiel.
* `conflict.node` : identifier la présence de nœuds de conflit dans le référentiel sous /content/dam/.
* `psb.file.large` : identifier les fichiers PSB volumineux (`dc:format : application/vnd.3gpp.pic-bw-small`) dont la taille est supérieure à 2 Go.
* `invalid.asset.name` : identifier des ressources contenant des caractères non valides [`* / : [ \ ] | # % { } ? &`] dans le nom.

## Implications et risques éventuels {#implications-and-risks}

* Cela pourrait entraîner la défaillance de certaines fonctionnalités d’Assets qui dépendent de propriétés héritées dans Experience Manager as a Cloud Service.
* AEM Assets dépend de l’existence du rendu original. Le traitement des ressources dans Cloud Service s’effectue en boucle si le rendu original est absent. La génération de sous-ressources n’est pas prise en charge dans AEMaaCS.
* Un nombre élevé de descendants sous un nœud de métadonnées peut ralentir le téléchargement des dossiers contenant des ressources en infraction.
* La présence de nœuds de conflit peut entraîner un échec de l’ingestion sur AEM as a Cloud Service.
* Experience Manager ne peut pas traiter de fichiers PSB haute résolution. Les clientes et clients qui utilisent ImageMagick pour traiter des fichiers volumineux peuvent subir un impact sur les performances si l’évaluation comparative correcte du serveur d’Experience Manager n’est pas effectuée.
* Les caractères non valides dans le nom de la ressource peuvent entraîner des échecs lors de la migration vers AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Guide de mise en œuvre"
>abstract="Adobe recommande de passer en revue la structure de contenu afin d’éviter la rupture des workflows qui dépendent de propriétés héritées. Contactez l’assistance clientèle pour obtenir de l’aide."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Analysez un dossier s’il manque un nœud enfant. Créez les nœuds manuellement si le nombre de dossiers est gérable. Sinon, utilisez un script.
* Pour les ressources auxquelles il manque le rendu original, vous pouvez, au choix, télécharger de nouveau les ressources ou les supprimer avant d’effectuer une migration.
* Aucune action n’est requise pour le rendu original des sous-ressources manquantes.
* En cas de conflit, les nœuds doivent être résolus ou supprimés avant la migration vers AEM as a Cloud Service.
* Contactez le service clientèle Adobe si vous prévoyez de traiter un grand nombre de fichiers PSD ou PSB volumineux. Experience Manager ne peut pas traiter de fichiers PSB haute résolution de plus de 30 000x23 000 pixels. Consultez la [documentation](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/assets/extending/best-practices-for-imagemagick).
* Contactez l’[équipe d’assistance clientèle Experience Manager](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
