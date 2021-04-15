---
title: OAUI
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: ht
source-wordcount: '107'
ht-degree: 100%

---


# OAUI {#oaui}

OAuth Users Instance (instance d’utilisateurs OAuth)

## Arrière-plan {#background}

`OAUI` identifie le modèle dans lequel au moins un utilisateur configuré lié à OAuth a besoin d’une migration correcte.

OAuth est configuré pour les utilisateurs lorsqu’il existe un sous-nœud nommé `oauth` directement sous un nœud `rep:AuthorizableId` sous la forme de `/home/user-path/user-node/oauth`.

Exemple : `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`

## Enjeux et risques possibles {#implications-and-risks}

* Les utilisateurs externes configurés avec OAuth ne pourront pas se connecter aux instances d’auteur/de publication tant qu’ils n’auront pas été reconfigurés avec la procédure ci-dessous.

## Solutions possibles {#solutions}

* Veuillez contacter votre représentant Adobe pour discuter des options pour la migration des utilisateurs.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
