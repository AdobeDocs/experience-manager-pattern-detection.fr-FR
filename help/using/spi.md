---
title: IHP
description: Page d’aide sur le code de détection des motifs.
source-git-commit: e050b9190f67fd6ccfac31490c4bf2a60d47731f
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