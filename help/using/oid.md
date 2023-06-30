---
title: OID
description: Page d’aide sur le code de la détection des motifs
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: d3e518cf8ad53a2cd28d4eea7f9b75c672881507
workflow-type: ht
source-wordcount: '485'
ht-degree: 100%

---

# OID {#oid}

Oak Index Definition

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Oak Index Definition (définition d’index Oak)"
>abstract="OID identifie les problèmes liés aux définitions d’index Oak. Il identifie les modifications apportées aux définitions standard de l’index Oak. Il identifie également les définitions d’index Oak personnalisés qui sont incompatibles avec AEM as a Cloud Service. Le message de chaque recherche OID identifie l’index et fournit des informations supplémentaires."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=fr#how-to-use" text="Instructions d’indexation de contenu"

`OID` identifie les problèmes liés aux définitions d’index Oak. Il identifie les modifications apportées aux définitions standard de l’index Oak. Il identifie également les définitions d’index Oak personnalisés qui sont incompatibles avec AEM as a Cloud Service. Le message de chaque recherche `OID` identifie l’index et fournit des informations supplémentaires.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `index.rule.violation` : incompatibilité d’index Oak personnalisé avec AEM as a Cloud Service.
* `standard.index.modification` : modification d’un index Oak standard.

## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons d’examiner tous les index personnalisés et à les restructurer conformément aux directives d’indexation de contenu. Tirez profit d’Index Converter pour migrer les définitions d’index Oak personnalisées existantes vers une définition d’index Oak personnalisée compatible avec AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=fr#oak-indexes" text="Instructions relatives aux packages"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html?lang=fr#refactoring-tools" text="Index Converter"

* Les modifications apportées aux définitions d’index Oak standard peuvent être perdues lors d’une mise à niveau d’AEM.
* Les définitions Oak ne sont pas modifiables, elles doivent être incluses dans un package avec le code du projet client et doivent uniquement être déployées à l’aide de Cloud Manager.
* Toutes les définitions d’index Oak doivent respecter la convention d’appellation et d’autres règles pour les index Oak dans AEM as a Cloud Service. L’inverse peut entraîner un comportement indésirable.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Outils et ressources"
>abstract="Examinez le projet WKND hérité pour comprendre comment les violations du protocole OID peuvent être résolues dans votre projet. Consultez également l’exemple de violation du protocole OID sur Github pour comprendre comment les index hérités peuvent être convertis à l’aide de l’outil Index Converter et rendus compatibles avec AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="Projet hérité WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Exemple de violation du protocole OID – Github"

* Résolvez les violations de règles d’index identifiées dans le message.
* Suivez les [lignes directrices pour le packaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=fr) AEM as a Cloud Service pour déployer des définitions d’index Oak nouvelles ou personnalisées.
* Les index standard AEM personnalisés et les nouvelles définitions d’index Oak personnalisés doivent suivre les [lignes directrices d’indexation de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=fr#preparing-the-new-index-definition) pour AEM as a Cloud Service.
* Examinez le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) et découvrez comment [les violations OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) peuvent être corrigées et rendues compatibles avec AEM as a Cloud Service.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
* Tirez profit d’[Index Converter](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html?lang=fr#refactoring-tools) pour migrer les définitions d’index Oak personnalisées existantes vers des définitions d’index Oak personnalisées compatibles avec AEM as a Cloud Service.
