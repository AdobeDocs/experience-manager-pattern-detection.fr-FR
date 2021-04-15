---
title: URC
description: Page d’aide sur le code de la détection des motifs
translation-type: ht
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: ht
source-wordcount: '176'
ht-degree: 100%

---


# URC {#urc}

Unsupported Runmode Configuration (configuration du mode d’exécution non prise en charge)

## Arrière-plan {#background}

`URC` identifie l’utilisation de configurations basées sur un nom de mode d’exécution non pris en charge dans AEM as a Cloud Service.

## Enjeux et risques possibles {#implications-and-risks}

* L’ensemble de noms pouvant être utilisé pour les modes d’exécution dans AEM as a Cloud Service est limité.
* Les configurations basées sur des noms de mode d’exécution non pris en charge n’auront aucun effet lorsqu’elles seront déployées sur AEM as a Cloud Service.

## Solutions possibles {#solutions}

* Examinez l’utilisation de cette configuration pour déterminer si elle est nécessaire.
* Renommez la configuration pour utiliser l’un des [noms de mode d’exécution](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=fr#custom-runmodes) pris en charge et suivez les [lignes directrices de résolution du mode d’exécution](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=fr#runmode-resolution).
* Examiner le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) et découvrez comment les [violations URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) peuvent être corrigées et rendues compatibles avec AEM as a Cloud Service.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
