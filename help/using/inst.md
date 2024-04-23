---
title: INST
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 77%

---

# INST {#inst}

Installed Artifact (artefact installé)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Installed Artifact (artefact installé)"
>abstract="INST identifie les packages ainsi que les lots personnalisés et tiers qui ont été installés dans AEM par le client. Ces rapports aident à caractériser l’état du système dans la portée générale d’une mise à niveau. Les packages tiers doivent respecter les instructions de développement et relatives aux packages d’AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Conseils de développement – AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package" text="Instructions relatives aux packages – AEM as a Cloud Service"

INST identifie les packages ainsi que les lots personnalisés et tiers qui ont été installés dans AEM par le client. Ces rapports aident à caractériser l’état du système dans la portée générale d’une mise à niveau.

Lorsque plusieurs versions d’un package ont été installées, seule la dernière version est indiquée.

Les packages et lots détectés n’ont pas nécessairement été optimisés pour AEM as a Cloud Service. Tout package tiers doit être vérifié auprès de son créateur ou Adobe pour des raisons de compatibilité avec AEM as a Cloud Service.

Des sous-types sont utilisés pour identifier les différents types d’informations :

* `custom.bundle` : lot installé dans AEM.
* `custom.package` : package installé dans AEM.

## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Guide de mise en œuvre"
>abstract="Les clients ne peuvent plus installer de modules tiers à l’aide du gestionnaire de modules CRX. Les clients doivent consulter ces artefacts installés qui doivent être structurés et les optimiser pour travailler avec AEM as a Cloud Service. Vérifiez la compatibilité d’un package tiers avec son créateur ou avec son Adobe avec AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embeddeds" text="Intégrer des sous-packages dans le package conteneur"


* L’installation de packages tiers à l’aide du gestionnaire de modules CRX n’est pas possible dans AEM as a Cloud Service.
* Les applications qui dépendent de packages tiers peuvent ne pas fonctionner comme prévu jusqu’à ce qu’elles soient correctement déployées pour fonctionner avec AEM as a Cloud Service.
* Les packages de fournisseurs tiers, s’ils ne sont pas optimisés pour AEM as a Cloud Service, peuvent entraîner un comportement indésirable.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Outils et ressources"
>abstract="Examinez le projet WKND hérité et découvrez comment les violations du protocole INST peuvent être corrigées et rendues compatibles avec AEM Cloud Service. Consultez également l’ exemple de violation INST sur GitHub pour comprendre comment cela peut être corrigé et déployé dans AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="Projet hérité WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Exemple de violation INST - GitHub"

* Les packages tiers doivent être déployés sur AEM dans le cadre du projet à l’aide du [processus de déploiement](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deployment-process) de Cloud Manager.
* Examinez comment [incorporer des packages tiers](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embedding-3rd-party-packages) dans votre projet pour AEM as a Cloud Service.
* Les packages tiers doivent respecter les lignes directrices de [développement](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines) et de [packaging](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package) d’AEM as a Cloud Service.
* Examinez le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) et découvrez comment [les violations INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) peuvent être corrigées et rendues compatibles avec AEM as a Cloud Service.
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
