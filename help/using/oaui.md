---
title: OAUI
description: Page d’aide sur le code de détection des motifs.
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 100%

---

# OAUI {#oaui}

OAuth Users Instance (instance d’utilisateurs OAuth)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth Users Instance (instance d’utilisateurs OAuth)"
>abstract="Le code OAUI identifie le motif pour lequel au moins un utilisateur configuré et lié à OAuth a besoin d’être migré de façon adaptée. OAuth est configuré pour des utilisateurs et utilisatrices lorsqu’il existe un sous-nœud appelé OAuth directement dans un nœud rep:AuthorizableId dans le formulaire /home/user-path/user-node/oauth."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Notes de mise à jour"

`OAUI` identifie le motif dans lequel au moins un profil utilisateur configuré lié à OAuth a besoin d’une migration correcte.

OAuth est configuré pour les utilisateurs lorsqu’il existe un sous-nœud nommé `oauth` directement sous un nœud `rep:AuthorizableId` sous la forme de `/home/user-path/user-node/oauth`.

Exemple : `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`

## Enjeux et risques possibles {#implications-and-risks}

* Les personnes externes configurées avec OAuth ne pourront pas se connecter aux instances de création ou de publication tant qu’elless n’auront pas été reconfigurées avec la procédure ci-dessous.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Guide de mise en œuvre"
>abstract="Les personnes externes configurées avec OAuth ne pourront pas se connecter aux instances de création ou de publication tant qu’elles n’auront pas été reconfigurées de manière à être compatibles avec AEM as a Cloud Service. AEM as a Cloud Service prend en charge l’authentification IMS uniquement pour les personnes faisant partie de l’équipe de création, d’administration et de développement, et l’intégration SAML seulement pour les environnements de publication. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/security/ims-support" text="Assistance IMS – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="Intégration SAML – Publication"

* Contactez votre représentant ou représentante Adobe pour discuter des options pour la migration des utilisateurs et utilisatrices.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous aves besoin de clarifications ou de réponses à vos préoccupations.
