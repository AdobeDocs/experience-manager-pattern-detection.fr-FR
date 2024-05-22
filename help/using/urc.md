---
title: URC
description: Page d’aide sur le code de détection des motifs.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 77%

---

# URC {#urc}

Unsupported Runmode Configuration (configuration du mode d’exécution non prise en charge)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Unsupported Runmode Configuration (configuration du mode d’exécution non prise en charge)"
>abstract="URC identifie l’utilisation de configurations basées sur un nom de mode d’exécution non pris en charge dans AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Modes d’exécution pris en charge"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Modes d’exécution"

`URC` identifie l’utilisation de configurations basées sur un nom de mode d’exécution non pris en charge dans AEM as a Cloud Service.

## Implications et risques éventuels {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Guide de mise en œuvre"
>abstract="La bonne pratique consiste à vérifier si tous les modes d’exécution utilisés dans votre application sont pris en charge. Et assurez-vous qu’ils suivent les instructions de résolution du mode d’exécution."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Instructions relatives à la résolution du mode d’exécution"

* L’ensemble de noms pouvant être utilisé pour l’exécution de différents modes dans AEM as a Cloud Service est limité.
* Les configurations basées sur des noms de mode d’exécution non pris en charge n’ont aucun effet lorsqu’elles sont déployées sur AEM as a Cloud Service.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Outils et ressources"
>abstract="Examinez le projet hérité WKND et découvrez comment les violations du protocole URC peuvent être corrigées et rendues compatibles avec AEM Cloud Service. Passez également en revue l’exemple de violation URC sur GitHub pour comprendre comment mettre à jour les configurations OSGi basées sur le mode d’exécution personnalisé pour se conformer à AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Projet hérité WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Exemple de violation du protocole URC - GitHub"

* Examinez l’utilisation de cette configuration pour déterminer si elle est nécessaire.
* Renommez la configuration à l’aide de l’un des [noms du mode d’exécution](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) pris en charge et suivez les [instructions de résolution du mode d’exécution](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Examiner le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) et découvrez comment les [violations URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) peuvent être corrigées et rendues compatibles avec AEM as a Cloud Service.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
