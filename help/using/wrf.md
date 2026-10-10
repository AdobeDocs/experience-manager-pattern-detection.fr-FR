---
title: WRF
description: Page d’aide sur le code de détection des motifs.
exl-id: 36578498-d5b2-46d1-a274-a1646ceaa764
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '91'
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
