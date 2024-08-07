---
title: URS
description: Page d’aide sur le code de détection des motifs.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 84%

---

# URS {#urs}

Structure de référentiel non prise en charge

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Structure de référentiel non prise en charge"
>abstract="La structure de référentiel non prise en charge (URS) identifie les cas d’URS et les caractéristiques de nœuds. Cette option fait apparaître les informations afin d’éviter les conflits entre le code de produit AEM et le code client, le contenu étant restructuré à partir de `/etc` vers d’autres dossiers du référentiel et plus en profondeur."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Restructuration des référentiels"

## Contexte {#background}

`URS` Identifie les cas d’URS (structure de référentiel non prise en charge) et les caractéristiques de noeud. Depuis AEM 6.4, des lignes directrices ont été fournies pour la restructuration du contenu du référentiel. En délimitant clairement les hiérarchies pour AEM code de produit et de client, et en évitant les conflits entre eux tous, le contenu est restructuré de `/etc` vers d’autres dossiers du référentiel. Vous devez pour cela respecter les règles de haut niveau suivantes :

* AEM code de produit est toujours placé dans `/libs` que le code personnalisé ne doit pas remplacer.
* Le code personnalisé doit être placé dans `/apps`, `/content` et `/conf`.
* Il est fortement recommandé que ces lignes directrices soient suivies pour AEM as a Cloud Service.

Des sous-types servent à identifier les types spécifiques de problèmes de référentiel qui doivent être résolus :

* `clientlibs.location` : bibliothèque cliente référençant `/etc` par chemin d’accès.
* `file.location` : fichier sous `/etc` qui a été modifié depuis l’installation.
* `node.location` : nœud sous `/etc` qui a été modifié depuis l’installation.
* `workflow.location` : modèle ou lanceur de workflow sous `/etc/workflow`.
* `package.structure` : package qui contient à la fois du contenu modifiable et du contenu non modifiable.
* `node.size` : nœud dont la taille n’est pas prise en charge.

## Enjeux et risques possibles {#implications-and-risks}

* Le code personnalisé reposant sur des chemins d’accès plus anciens peut provoquer un comportement indésirable et affecter les fonctionnalités du produit.
* Les packages qui contiennent à la fois du contenu modifiable et du contenu non modifiable risquent d’entraîner des problèmes lors du déploiement.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons de passer en revue votre projet de code. Assurez-vous qu’il respecte les directives relatives à la structure de projet AEM et évitez tout code reposant sur des chemins d’accès de référentiel anciens ou non pris en charge, ce qui pourrait provoquer un comportement indésirable dans AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Instructions relatives à la structure de projet AEM"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Consultez [Restructuration du référentiel](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring) pour obtenir des instructions sur la préparation pour AEM as a Cloud Service.
* Consultez également [Structure des projets AEM](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) pour en savoir plus sur les zones modifiables et non modifiables du référentiel.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
* Utilisez [Repository Modernizer](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools) pour restructurer les packages de projets existants en séparant le contenu et le code en packages discrets compatibles avec la structure de projet définie par Adobe Experience Manager as a Cloud Service.
