---
title: OID
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---


# OID {#oid}

Définition de l&#39;index en chêne

## Arrière-plan {#background}

`OID` identifie les problèmes liés aux définitions de l&#39;index Oak. Il identifie les modifications apportées aux définitions standard de l&#39;index de chêne. Il identifie également les définitions d’index Oak personnalisées qui sont incompatibles avec AEM en tant que Cloud Service. Le message de chaque recherche `OID` identifie l&#39;index et fournit des informations supplémentaires.

Les sous-types permettent d’identifier les différents types d’informations :

* `custom.index.violation`: Incompatibilité d’index Oak personnalisé avec AEM en tant que Cloud Service.
* `standard.index.modification`: Modification d’un index standard de chêne.

## Incidences possibles et risques {#implications-and-risks}

* Les modifications apportées aux définitions d’index standard de chêne peuvent être perdues lors d’une mise à niveau AEM.
* Les définitions de chêne sont immuables, doivent être incluses dans un pack avec le code du projet client et doivent uniquement être déployées à l’aide de Cloud Manager.
* Toutes les définitions d&#39;index de chêne doivent respecter la convention d&#39;appellation et d&#39;autres règles pour les index de chêne en AEM Cloud Service. Ceux qui ne le font pas peuvent provoquer un comportement indésirable.

## Solutions possibles {#solutions}

* Résolvez les violations de règles d&#39;index identifiées dans le message.
* Suivez AEM en tant que Cloud Service [instructions d’emballage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) pour déployer les définitions d’index Oak nouvelles ou personnalisées.
* Les index standard AEM personnalisés et les nouvelles définitions d&#39;index Oak personnalisés doivent suivre les [directives d&#39;indexation de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition) pour AEM en tant que Cloud Service.
* Examinez le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) et comprenez comment [les violations d&#39;OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) peuvent être corrigées et rendues compatibles avec l&#39;AEM en tant que Cloud Service.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
* Tirez parti du [convertisseur d’index](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools) pour migrer les définitions d’index de chêne personnalisé existantes vers AEM en tant que définitions d’index de chêne personnalisé compatibles avec les Cloud Service.
