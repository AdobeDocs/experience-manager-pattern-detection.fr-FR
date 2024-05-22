---
title: DOPI
description: Page d’aide sur le code de détection des motifs.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 69%

---

# DOPI {#dopi}

Deprecated Ordered Property Index (index des propriétés organisées obsolètes)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Deprecated Ordered Property Index (index des propriétés organisées obsolètes)"
>abstract="Le code DOPI identifie l’utilisation de définitions d’index de propriété triées (`primaryType=oak:QueryIndexDefinition` ET `type="ordered"`). La définition a été abandonnée dans AEM 6.1 et supprimée dans AEM 6.2."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="Index organisé – Obsolète"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/operations/indexing" text="Indexation – AEM as a Cloud Service"

`DOPI`  Identifie l’utilisation de définitions d’index de propriété triées (`primaryType=oak:QueryIndexDefinition` ET `type="ordered"`). Les définitions ont été abandonnées dans AEM 6.1 et supprimées dans AEM 6.2.

## Implications et risques éventuels {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons d’examiner tous les index organisés obsolètes et de les déplacer vers des index Lucene pris en charge afin d’éviter des problèmes de performances importants ou des exigences clientes non fonctionnelles."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/practices/best-practices-for-queries-and-indexing" text="Bonnes pratiques relatives aux requêtes et à l’indexation"

* Certaines requêtes peuvent ne pas répondre.
* La fonctionnalité du client peut ne pas fonctionner correctement.
* Les avertissements transversaux ou même les erreurs et les sanctions de performances importantes comme les index obsolètes n’ont aucun effet.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Outils et ressources"
>abstract="Examinez le projet WKND hérité et découvrez comment les violations du protocole DOPI peuvent être corrigées et rendues compatibles avec AEM Cloud Service. Consultez également l’ exemple de violation DOPI sur GitHub. Cela peut vous aider à comprendre comment les index triés hérités peuvent être convertis en index Lucene pris en charge dans AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Projet hérité WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Exemple de violation du protocole DOPI - GitHub"

* Modifiez la définition d’index afin qu’elle devienne (ou qu’elle remplace l’index par) une définition d’index prise en charge. (Voir [Requêtes et indexation Oak](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing)).
* Examinez le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) et découvrez comment [les violations DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) peuvent être corrigées et rendues compatibles avec AEM as a Cloud Service.
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
