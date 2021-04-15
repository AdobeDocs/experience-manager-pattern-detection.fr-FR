---
title: INST
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: ht
source-wordcount: '315'
ht-degree: 100%

---


# INST {#inst}

Installed Artifact (artefact installé)

## Arrière-plan {#background}

`INST` identifie les packages et les lots personnalisés et tiers qui ont été installés dans AEM par le client. Ces rapports aident à caractériser l’état du système dans la portée générale d’une mise à niveau.

Lorsque plusieurs versions d’un package ont été installées, seule la dernière version est indiquée.

Les packages et lots détectés n’ont pas nécessairement été optimisés pour AEM as a Cloud Service. Tout package tiers doit être vérifié auprès de son créateur ou Adobe pour des raisons de compatibilité avec AEM as a Cloud Service.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `custom.bundle` : lot installé dans AEM.
* `custom.package` : package installé dans AEM.

## Enjeux et risques possibles {#implications-and-risks}

* L’installation de packages tiers à l’aide du gestionnaire de modules CRX n’est pas possible dans AEM as a Cloud Service.
* Les applications qui dépendent de packages tiers peuvent ne pas fonctionner comme prévu jusqu’à ce qu’elles soient correctement déployées pour fonctionner avec AEM as a Cloud Service.
* Les packages de fournisseurs tiers, s’ils ne sont pas optimisés pour AEM as a Cloud Service, peuvent entraîner un comportement indésirable.

## Solutions possibles {#solutions}

* Les packages tiers doivent être déployés sur AEM dans le cadre du projet à l’aide du [processus de déploiement](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html?lang=fr#deployment-process) de Cloud Manager.
* Examinez comment [incorporer des packages tiers](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=fr#embedding-3rd-party-packages) dans votre projet pour AEM as a Cloud Service.
* Les packages tiers doivent respecter les lignes directrices de [développement](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=fr) et de [packaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html?lang=fr) d’AEM as a Cloud Service.
* Examinez le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) et découvrez comment [les violations INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) peuvent être corrigées et rendues compatibles avec AEM as a Cloud Service.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
