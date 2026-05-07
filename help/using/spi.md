---
title: IHP
description: Page d’aide sur le code de détection des motifs.
exl-id: 39f2d04e-c6e4-4da6-b000-0115bc2b87bf
source-git-commit: 29d702c9662fd185ef806123fc4f4a03a70d64aa
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
