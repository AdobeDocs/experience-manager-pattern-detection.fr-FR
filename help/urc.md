---
title: URC
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# URC {#urc}

Configuration du mode d&#39;exécution non prise en charge

## Arrière-plan {#background}

`URC` identifie l&#39;utilisation de configurations basées sur un nom runmode qui n&#39;est pas pris en charge en AEM en tant que Cloud Service.

## Incidences possibles et risques {#implications-and-risks}

* L&#39;ensemble de noms pouvant être utilisé pour les modes d&#39;exécution en AEM Cloud Service est limité.
* Les configurations basées sur des noms de mode d’exécution non pris en charge n’auront aucun effet lorsqu’elles seront déployées en tant que Cloud Service sur AEM.

## Solutions possibles {#solutions}

* Examinez l’utilisation de cette configuration pour déterminer si elle est nécessaire.
* Renommez la configuration pour utiliser l&#39;un des noms [runmode pris en charge](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) et suivez les [directives de résolution du mode d&#39;exécution](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution).
* Examiner le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) et comprendre comment [les violations URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) peuvent être corrigées et rendues compatibles avec l&#39;AEM en tant que Cloud Service.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
