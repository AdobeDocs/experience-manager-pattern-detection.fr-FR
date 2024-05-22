---
title: OID
description: Page d’aide sur le code de détection des motifs.
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 86%

---

# OID {#oid}

Oak Index Definition

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Oak Index Definition (définition d’index Oak)"
>abstract="OID identifie les problèmes liés aux définitions d’index Oak. Il identifie les modifications apportées aux définitions standard de l’index Oak. Il identifie également les définitions d’index Oak personnalisés qui sont incompatibles avec AEM as a Cloud Service. Le message de chaque recherche OID identifie l’index et fournit des informations supplémentaires."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/operations/indexing#how-to-use" text="Instructions d’indexation de contenu"

`OID` identifie les problèmes liés aux définitions d’index Oak. Il identifie les modifications apportées aux définitions standard de l’index Oak. Il identifie également les définitions d’index Oak personnalisés qui sont incompatibles avec AEM as a Cloud Service. Le message pour chaque résultat d’`OID` identifie l’index et fournit des informations supplémentaires.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `index.rule.violation` : incompatibilité d’index Oak personnalisé avec AEM as a Cloud Service.
* `standard.index.modification` : modification d’un index Oak standard.

## Implications et risques éventuels {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons d’examiner tous les index personnalisés et de les restructurer conformément aux directives d’indexation de contenu. Utilisez Index Converter pour migrer les définitions d’index Oak personnalisées existantes vers une définition d’index Oak personnalisée compatible avec AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#oak-indexes" text="Instructions relatives aux packages"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools" text="Index Converter"

* Les modifications apportées aux définitions d’index Oak standard peuvent être perdues lors d’une mise à niveau d’AEM.
* Les définitions Oak ne sont pas modifiables, elles doivent être incluses dans un package avec le code du projet client et doivent uniquement être déployées à l’aide de Cloud Manager.
* Toutes les définitions d’index Oak doivent respecter la convention de nommage et les autres règles des index Oak dans AEM as a Cloud Service. Sinon, cela peut entraîner un comportement indésirable.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Outils et ressources"
>abstract="Examinez le projet WKND hérité pour comprendre comment les violations du protocole OID peuvent être résolues dans votre projet. Consultez également l’ exemple de violation OID sur GitHub. Il peut vous aider à comprendre comment les index hérités peuvent être convertis à l’aide de l’outil convertisseur d’index et rendus compatibles avec AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="Projet hérité WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Exemple de violation du protocole OID - GitHub"

* Résolvez les violations de règles d’index identifiées dans le message.
* Pour déployer de nouvelles définitions d’index Oak ou des définitions personnalisées, suivez les [instructions relatives aux packages](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) d’AEM as a Cloud Service.
* Les index standard AEM personnalisés et les nouvelles définitions d’index Oak personnalisés doivent suivre les [directives d’indexation de contenu](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/operations/indexing#preparing-the-new-index-definition) pour AEM as a Cloud Service.
* Examinez le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) et découvrez comment [les violations OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) peuvent être corrigées et rendues compatibles avec AEM as a Cloud Service.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
* Utilisez la variable [Convertisseur d’index](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools) pour migrer les définitions d’index Oak personnalisé existantes vers AEM définitions d’index Oak personnalisé compatibles as a Cloud Service.
