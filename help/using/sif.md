---
title: SIF
description: Page d’aide sur le code de détection des motifs.
exl-id: c0a5c565-16e7-407b-befc-5a2966089da1
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 7%
---
# SIF {#sif}

## Contexte {#background}

SIF identifie l’utilisation sociale incompatible avec AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Solutions possibles {#solutions}

Recherchez les solutions possibles pour les différents sous-types ci-dessous :

* `social.bundles.detected` - Ces lots seront désinstallés pendant la mise à niveau
* `social.packages.detected` - Ces packages seront supprimés pendant la mise à niveau
* `social.packages.dependency` - Veuillez supprimer la dépendance de package du réseau social des packages personnalisés
* `social.nodes.detected` - Mise à jour du code personnalisé pour ne pas créer de nœuds sociaux
* `social.configs.detected` - N’utilisez pas les propriétés de configuration des réseaux sociaux dans le code personnalisé
* `social.users.detected` - N’utilisez pas d’utilisateurs des réseaux sociaux dans le code personnalisé
* `social.overlays.detected` - Utilisation de la suppression des recouvrements sociaux
* `social.paths.detected` - Supprimez les chemins d’accès sociaux après vous être assuré qu’ils ne sont pas utilisés dans AEM
* `social.resource.type.detected` - Supprimer l’utilisation des types de ressources sociales
* `social.usage` - Supprimez les API sociales du code personnalisé.
