---
title: OAUI
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# OAUI {#oaui}

Instance des utilisateurs OAuth

## Arrière-plan {#background}

`OAUI` identifie le modèle dans lequel au moins un utilisateur configuré lié à OAuth nécessite une migration correcte.

OAuth est configuré pour les utilisateurs lorsqu’il existe un sous-noeud nommé `oauth` directement sous un noeud `rep:AuthorizableId` sous la forme `/home/user-path/user-node/oauth`.

Voici un exemple : `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Incidences possibles et risques {#implications-and-risks}

* Les utilisateurs externes configurés avec OAuth ne pourront pas se connecter aux instances d’auteur/publication tant qu’ils n’auront pas été reconfigurés avec la procédure ci-dessous.

## Solutions possibles {#solutions}

* Contactez votre représentant d’Adobe pour discuter des options de migration des utilisateurs.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
