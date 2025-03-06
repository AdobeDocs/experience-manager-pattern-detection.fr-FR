---
title: AC
description: Page d’aide sur le code de détection des motifs.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---

# AC {#ac}

## Contexte {#background}

AC identifie l&#39;utilisation du bundle Assets incompatible avec AEM 6.5 LTS

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Solutions possibles {#solutions}

Recherchez les solutions possibles pour les différents sous-types ci-dessous :

* `asset.bundles.detected` - Ce lot sera désinstallé pendant la mise à niveau.
* `asset.usage` - Supprimez toutes les dépendances de composant Évaluation des ressources et Catalogue de ressources du code personnalisé. Le cas échéant, modifiez le code pour utiliser la nouvelle `com.day.cq.dam.scene7.api.model.Scene7ViewerConfig#getSettingsList()` de `List<Scene7ConfigSetting>` API.
* `asset.overlays.detected` - Les recouvrements créés sur les composants Évaluation Assets et Catalogue doivent être supprimés.
* `asset.resource.type.detected` - Supprimez toute utilisation du type de ressource du composant d’évaluation Assets dans votre code personnalisé.
* `asset.paths.detected` - Déplacez le contenu client présent sous ces chemins et supprimez ces chemins après vous être assuré qu’ils ne sont pas utilisés dans AEM.