---
title: INST
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---


# INST {#inst}

Artifact installé

## Arrière-plan {#background}

`INST` identifie les packages et lots personnalisés et tiers qui ont été installés dans AEM par le client. Ces rapports aident à caractériser l&#39;état du système dans la portée générale d&#39;une mise à niveau.

Lorsque plusieurs versions d’un package ont été installées, seule la dernière version est signalée.

Les packages et lots détectés n’ont pas nécessairement été optimisés pour AEM en tant que Cloud Service. Tout module tiers doit être vérifié auprès de son créateur ou Adobe pour des raisons de compatibilité avec AEM en tant que Cloud Service.

Les sous-types permettent d’identifier différents types d’informations :

* `custom.bundle`: Groupe installé dans AEM.
* `custom.package`: Package qui a été installé dans AEM.

## Incidences possibles et risques {#implications-and-risks}

* L’installation de packages tiers à l’aide de CRX Package Manager n’est pas possible en AEM en tant que Cloud Service.
* Les applications dépendantes de packs tiers peuvent ne pas fonctionner comme prévu jusqu’à ce qu’elles soient correctement déployées pour fonctionner avec AEM en tant que Cloud Service.
* Les packs de fournisseurs tiers, s’ils ne sont pas optimisés pour AEM en tant que service Cloud, peuvent entraîner un comportement indésirable.

## Solutions possibles {#solutions}

* Les packs tiers doivent être déployés sur AEM dans le cadre du projet à l’aide du processus de déploiement de Cloud Manager [](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process).
* Examinez comment [incorporer des packages tiers](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages) dans votre projet pour AEM en tant que Cloud Service.
* Les packs tiers doivent respecter l’AEM en tant que Cloud Service [développement](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) et [emballage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html).
* Examiner le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) et comprendre comment [les violations INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) peuvent être corrigées et rendues compatibles avec l&#39;AEM en tant que Cloud Service.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
