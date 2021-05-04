---
title: OAUI
description: Page d’aide sur le code de la détection des motifs
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 48%

---

# OAUI {#oaui}

OAuth Users Instance (instance d’utilisateurs OAuth)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth Users Instance (instance d’utilisateurs OAuth)"
>abstract="Le code OAUI identifie le modèle dans lequel au moins un utilisateur configuré pour OAuth nécessite une migration correcte. OAuth est configuré pour les utilisateurs lorsqu’il existe un sous-noeud nommé oauth directement sous un noeud rep:AuthorizableId sous la forme /home/user-path/user-node/oauth."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=fr" text="AEM en tant que Cloud Service - Notes de mise à jour"

`OAUI` identifie le modèle dans lequel au moins un utilisateur configuré lié à OAuth a besoin d’une migration correcte.

OAuth est configuré pour les utilisateurs lorsqu’il existe un sous-nœud nommé `oauth` directement sous un nœud `rep:AuthorizableId` sous la forme de `/home/user-path/user-node/oauth`.

Exemple : `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`

## Enjeux et risques possibles {#implications-and-risks}

* Les utilisateurs externes configurés avec OAuth ne pourront pas se connecter aux instances d’auteur/de publication tant qu’ils n’auront pas été reconfigurés avec la procédure ci-dessous.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Guide de mise en oeuvre"
>abstract="Les utilisateurs externes configurés avec OAuth ne pourront pas se connecter aux instances d’auteur/publication tant qu’ils ne seront pas reconfigurés pour être compatibles avec AEM en tant que Cloud Service. AEM en tant qu’offres Cloud Service prend uniquement en charge l’authentification IMS pour les utilisateurs Auteur, Admin et Dev et l’intégration SAML pour les environnements de publication. Contactez l&#39;assistance Adobe pour obtenir de l&#39;aide et des éclaircissements"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=fr" text="Support IMS - AEM en tant que Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/personalization/user-and-group-sync-for-publish-tier.html?lang=en#integration-with-an-idp" text="Intégration SAML - Publier"

* Veuillez contacter votre représentant Adobe pour discuter des options pour la migration des utilisateurs.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
