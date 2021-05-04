---
title: URC
description: Page d’aide sur le code de la détection des motifs
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 63%

---

# URC {#urc}

Unsupported Runmode Configuration (configuration du mode d’exécution non prise en charge)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Unsupported Runmode Configuration (configuration du mode d’exécution non prise en charge)"
>abstract="URC identifie l’utilisation de configurations basées sur un nom de mode d’exécution qui n’est pas pris en charge en AEM en tant que Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes" text="Modes d’exécution pris en charge"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#runmodes" text="Modes d’exécution"

`URC` identifie l’utilisation de configurations basées sur un nom de mode d’exécution non pris en charge dans AEM as a Cloud Service.

## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Guide de mise en oeuvre"
>abstract="Il est recommandé de vérifier si tous les modes d’exécution utilisés dans votre application sont pris en charge et de s’assurer qu’ils respectent les instructions de résolution du mode d’exécution."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#deploying" text="Instructions relatives à la résolution du mode d’exécution"

* L’ensemble de noms pouvant être utilisé pour les modes d’exécution dans AEM as a Cloud Service est limité.
* Les configurations basées sur des noms de mode d’exécution non pris en charge n’auront aucun effet lorsqu’elles seront déployées sur AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Outils et ressources"
>abstract="Examinez le projet WKND-legacy pour comprendre comment les violations URC peuvent être rendues compatibles avec AEM Cloud Service. Consultez également l’exemple de violation URC sur Github pour comprendre comment les configurations OSGi personnalisées basées sur le mode d’exécution peuvent être mises à jour pour se conformer à AEM en tant que Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Projet WKND-Legacy"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Exemple de violation avec un URC - Github"

* Examinez l’utilisation de cette configuration pour déterminer si elle est nécessaire.
* Renommez la configuration pour utiliser l’un des [noms de mode d’exécution](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=fr#custom-runmodes) pris en charge et suivez les [lignes directrices de résolution du mode d’exécution](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=fr#runmode-resolution).
* Examiner le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) et découvrez comment les [violations URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) peuvent être corrigées et rendues compatibles avec AEM as a Cloud Service.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
