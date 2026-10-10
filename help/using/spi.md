---
title: IHP
description: Page d’aide sur le code de détection des motifs.
exl-id: 39f2d04e-c6e4-4da6-b000-0115bc2b87bf
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
# IHP {#spi}

## Contexte {#background}

SIF identifie l’utilisation de Search and Promote incompatible avec AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Solutions possibles {#solutions}

Recherchez les solutions possibles pour les différents sous-types ci-dessous :

* `searchpromote.bundles.detected` - Ces lots seront désinstallés pendant la mise à niveau
* `earchpromote.packages.detected` - Ces packages seront supprimés pendant la mise à niveau
* `searchpromote.packages.dependency` - Supprimez toute dépendance Search and Promote que vos packages personnalisés peuvent présenter
* `searchpromote.usage` - Supprimer les API Search and Promote de votre code personnalisé
* `searchpromote.users.detected` - N’utilisez pas les utilisateurs du service Search and Promote dans le code personnalisé
* `searchpromote.configs.detected` - N’utilisez pas les propriétés de configuration Search and Promote dans votre code personnalisé.
