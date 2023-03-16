---
title: OAUI
description: Page d’aide sur le code de la détection des motifs
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 100%

---

# OAUI {#oaui}

OAuth Users Instance (instance d’utilisateurs OAuth)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth Users Instance (instance d’utilisateurs OAuth)"
>abstract="Le code OAUI identifie le motif pour lequel au moins un utilisateur configuré et lié à OAuth a besoin d’être migré de façon adaptée. OAuth est configuré pour des utilisateurs lorsqu’il existe un sous-nœud appelé « oauth » directement dans un nœud rep:AuthorizableId, sous la forme /home/user-path/user-node/oauth."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr" text="AEM as a Cloud Service – Notes de mise à jour"

`OAUI` identifie le modèle dans lequel au moins un utilisateur configuré lié à OAuth a besoin d’une migration correcte.

OAuth est configuré pour les utilisateurs lorsqu’il existe un sous-nœud nommé `oauth` directement sous un nœud `rep:AuthorizableId` sous la forme de `/home/user-path/user-node/oauth`.

Exemple : `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`

## Enjeux et risques possibles {#implications-and-risks}

* Les utilisateurs externes configurés avec OAuth ne pourront pas se connecter aux instances d’auteur/de publication tant qu’ils n’auront pas été reconfigurés avec la procédure ci-dessous.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Guide de mise en œuvre"
>abstract="Les utilisateurs externes configurés avec OAuth ne pourront pas se connecter aux instances d’auteur ou de publication tant qu’ils n’auront pas été reconfigurés de telle manière à être compatibles avec AEM as a Cloud Service. AEM as a Cloud Service prend en charge l’authentification IMS uniquement pour les utilisateurs Auteur, Admin et Dev, et l’intégration SAML seulement pour les environnements de publication. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=fr" text="Assistance IMS – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/personalization/user-and-group-sync-for-publish-tier.html?lang=fr#integration-with-an-idp" text="Intégration SAML – Publication"

* Veuillez contacter votre représentant Adobe pour discuter des options pour la migration des utilisateurs.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
