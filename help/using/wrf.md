---
title: WRF
description: Page d’aide sur le code de détection des motifs.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 8%

---

# WRF {#wrf}

## Contexte {#background}

WRF identifie l’utilisation de we-retail incompatible avec AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Solutions possibles {#solutions}

Recherchez les solutions possibles pour les différents sous-types ci-dessous :

* `weretail.bundles.detected` - Ces lots seront désinstallés pendant la mise à niveau
* `weretail.packages.detected` - Ces packages seront supprimés pendant la mise à niveau
* `weretail.configs.detected` - N’utilisez pas les propriétés de configuration We.Retail dans votre code personnalisé
* `weretail.packages.dependency` - Supprimer la dépendance de tout package personnalisé sur We.Retail
* `weretail.paths.detected` - Ces chemins We.Retail peuvent être supprimés après avoir vérifié que vous n’utilisez pas les réseaux sociaux
* `weretail.resource.type.detected` - Supprimer l’utilisation du type de ressource We.Retail
* `weretail.usage` - Supprimez les API We.Retail de votre code personnalisé.