---
title: SCR
description: Page d’aide sur le code de détection des motifs.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---

# SCR {#scr}

## Contexte {#background}

SIF identifie l’utilisation d’AEM Screens incompatible avec AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Solutions possibles {#solutions}

Recherchez les solutions possibles pour les différents sous-types ci-dessous :

* `screens.bundles.detected` - Ces lots seront désinstallés pendant la mise à niveau.
* `screens.packages.detected` - Ces packages seront supprimés pendant la mise à niveau.
* `screens.packages.dependency` - Supprimez toute dépendance sur Screens de vos packages personnalisés.
* `screens.configs.detected` - Assurez-vous que vous n’utilisez aucune propriété de configuration Screens dans votre code personnalisé.
* `screens.users.detected` - Assurez-vous de ne pas utiliser les utilisateurs du service Screens dans le code personnalisé.
* `screens.paths.detected` - Supprimez les chemins Screens après vous être assuré qu’ils ne sont pas utilisés dans AEM.
* `screens.resource.type.detected` - Supprimez l’utilisation du type de ressource Screens.
* `screens.usage` - Supprimez les API Screens de votre code personnalisé.