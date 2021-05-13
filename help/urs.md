---
title: URS
description: Page d’aide sur le code de la détection des motifs
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
translation-type: ht
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: ht
source-wordcount: '408'
ht-degree: 100%

---

# URS {#urs}

Structure de référentiel non prise en charge

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Structure de référentiel non prise en charge"
>abstract="L’URS identifie les cas de structure de référentiel non prise en charge. Cette option permet d’uniformiser les informations afin d’éviter les conflits entre le code de produit AEM et le code client, le contenu étant restructuré à partir de /etc vers d’autres dossiers du référentiel et plus en profondeur."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=fr" text="Restructuration des référentiels"

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
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons de passer en revue votre projet de code, de vous assurer qu’il respecte les directives relatives à la structure de projet AEM et d’éviter tout code reposant sur des chemins d’accès de référentiel anciens ou non pris en charge, ce qui pourrait provoquer un comportement indésirable dans AEM as a Cloud Service. Contactez l’assistance Adobe pour obtenir plus d’aide et d’informations"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=fr" text="Instructions relatives à la structure de projet AEM"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Consultez [Restructuration du référentiel](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=fr) pour obtenir des instructions sur la préparation pour AEM as a Cloud Service.
* Consultez également [Structure du projet AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=fr) pour en savoir plus sur les zones modifiables et non modifiables du référentiel.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
* Tirez profit de [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html?lang=fr#refactoring-tools) pour restructurer des packages de projets existants en séparant le contenu et le code en packages distincts compatibles avec la structure de projet définie pour Adobe Experience Manager as a Cloud Service.
