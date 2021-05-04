---
title: URS
description: Page d’aide sur le code de la détection des motifs
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 78%

---

# URS {#urs}

Structure de référentiel non prise en charge

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Structure de référentiel non prise en charge"
>abstract="Le service d&#39;identification des cas de structure de référentiel non prise en charge. Cette option permet d’afficher des informations afin d’éviter les conflits entre le code de produit AEM et le code client, le contenu étant restructuré à partir de /etc vers d’autres dossiers du référentiel et plus encore."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html" text="Restructuration des référentiels"

## Arrière-plan {#background}

`URS` identifie les cas de structure de référentiel non prise en charge. Depuis AEM 6.4, des lignes directrices ont été fournies pour la restructuration du contenu du référentiel. En délimitant clairement les hiérarchies pour le code produit AEM et le code client et en évitant les conflits entre eux, le contenu est restructuré à partir de `/etc` vers d’autres dossiers du référentiel, en respectant les règles de haut niveau suivantes :

* Le code produit AEM sera toujours placé dans `/libs`, qui ne doit pas être remplacé par le code personnalisé. Le code personnalisé doit être placé dans `/apps`, `/content` et `/conf`.
* Il est fortement recommandé que ces lignes directrices soient suivies pour AEM as a Cloud Service.

Des sous-types servent à identifier les types spécifiques de problèmes de référentiel qui doivent être résolus :
* `clientlibs.location` : bibliothèque cliente référençant `/etc` par chemin d’accès.
* `file.location` : fichier sous `/etc` qui a été modifié depuis l’installation.
* `node.location` : nœud sous `/etc` qui a été modifié depuis l’installation.
* `workflow.location` : modèle ou lanceur de workflow sous `/etc/workflow`.
* `package.structure` : package qui contient à la fois du contenu modifiable et du contenu non modifiable.

## Enjeux et risques possibles {#implications-and-risks}

* Le code personnalisé reposant sur des chemins d’accès plus anciens peut provoquer un comportement indésirable et affecter les fonctionnalités du produit.
* Les packages qui contiennent à la fois du contenu modifiable et du contenu non modifiable risquent de poser problème lors du déploiement.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Guide de mise en oeuvre"
>abstract="La meilleure pratique consiste à examiner votre projet de code et à s’assurer qu’il respecte les directives de structure de projet AEM et à éviter le code reposant sur des chemins d’accès de référentiel anciens/non pris en charge qui peuvent provoquer un comportement indésirable dans AEM en tant que Cloud Service. Contactez l&#39;assistance Adobe pour obtenir de l&#39;aide et des éclaircissements"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html" text="Lignes directrices AEM structure du projet"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Consultez [Restructuration du référentiel](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=fr) pour obtenir des instructions sur la préparation pour AEM as a Cloud Service.
* Consultez également [Structure du projet AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=fr) pour en savoir plus sur les zones modifiables et non modifiables du référentiel.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
* Tirez profit de [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html?lang=fr#refactoring-tools) pour restructurer des packages de projets existants en séparant le contenu et le code en packages distincts compatibles avec la structure de projet définie pour Adobe Experience Manager as a Cloud Service.
