---
title: OAUI
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 47%

---

# OAUI {#oaui}

OAuth Users Instance (instance d’utilisateurs OAuth)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth Users Instance (instance d’utilisateurs OAuth)"
>abstract="Le code OAUI identifie le motif pour lequel au moins un utilisateur configuré et lié à OAuth a besoin d’être migré de façon adaptée. OAuth est configuré pour des utilisateurs lorsqu’il existe un sous-nœud appelé « oauth » directement dans un nœud rep:AuthorizableId, sous la forme /home/user-path/user-node/oauth."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service – Notes de mise à jour"

OAUI identifie le modèle dans lequel il existe au moins un utilisateur configuré OAuth qui nécessite une migration correcte.

OAuth est configuré pour les utilisateurs lorsqu’il existe un sous-nœud nommé `oauth` directement sous un nœud `rep:AuthorizableId` sous la forme de `/home/user-path/user-node/oauth`.

Exemple : `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`

## Enjeux et risques possibles {#implications-and-risks}

* Les utilisateurs externes configurés avec OAuth ne peuvent pas se connecter aux instances de création/publication tant qu’ils ne sont pas reconfigurés selon la procédure ci-dessous.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Guide de mise en œuvre"
>abstract="Les utilisateurs externes configurés avec OAuth ne peuvent pas se connecter aux instances de création/publication tant qu’ils ne sont pas reconfigurés pour être compatibles avec AEM as a Cloud Service. AEM as a Cloud Service offre la prise en charge de l’authentification IMS uniquement pour les utilisateurs Auteur, Admin et Dev et l’intégration basée sur SAML pour les environnements de publication. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support" text="Assistance IMS – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="Intégration SAML – Publication"

* Contactez votre représentant d’Adobe si vous devez discuter des options de migration des utilisateurs.
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
