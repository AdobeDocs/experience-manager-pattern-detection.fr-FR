---
title: URS
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# URS {#urs}

Structure de référentiel non prise en charge

## Arrière-plan {#background}

`URS` identifie les cas de structure de référentiel non prise en charge. À partir de l&#39;AEM 6.4, des lignes directrices ont été fournies pour la restructuration du contenu du référentiel. En délimitant clairement les hiérarchies pour le code de produit AEM et le code client et en évitant les conflits entre eux, le contenu est restructuré à partir de `/etc` vers d&#39;autres dossiers du référentiel, en respectant les règles de haut niveau suivantes :

* AEM code de produit sera toujours placé dans `/libs`, qui ne doit pas être remplacé par le code personnalisé Le code personnalisé doit être placé dans `/apps`, `/content` et `/conf`.
* Il est fortement recommandé que ces directives soient suivies pour AEM Cloud Service.

Les sous-types servent à identifier les types spécifiques de problèmes de référentiel qui doivent être résolus :
* `clientlibs.location`: Bibliothèque cliente référençant  `/etc` par chemin d’accès.
* `file.location`: Fichier sous  `/etc` lequel a été modifié depuis l’installation.
* `node.location`: Noeud sous  `/etc` lequel a été modifié depuis l’installation.
* `workflow.location`: Un modèle de processus ou un lanceur sous  `/etc/workflow`.
* `package.structure`: Package contenant à la fois du contenu modifiable et du contenu non modifiable.

## Incidences possibles et risques {#implications-and-risks}

* Le code personnalisé reposant sur des chemins plus anciens peut provoquer un comportement indésirable et affecter les fonctionnalités du produit.
* Les packages contenant à la fois du contenu mutable et immuable risquent de poser des problèmes lors du déploiement.

## Solutions possibles {#solutions}

* Consultez la section [Restructuration du référentiel](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) pour obtenir des instructions sur la préparation de l&#39;AEM en tant que Cloud Service.
* Consultez également [AEM Structure du projet](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) pour en savoir plus sur les zones mutables et immuables du référentiel.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
* Tirez parti de [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools) pour restructurer les packages de projets existants en séparant le contenu et le code en packages distincts afin d&#39;être compatible avec la structure de projet définie pour Adobe Experience Manager en tant que Cloud Service.