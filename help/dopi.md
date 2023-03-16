---
title: DOPI
description: Page d’aide sur le code de la détection des motifs
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 100%

---

# DOPI {#dopi}

Deprecated Ordered Property Index (index des propriétés organisées obsolète)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Deprecated Ordered Property Index (index des propriétés organisées obsolète)"
>abstract="Le code DOPI identifie l’utilisation de définitions d’index de propriétés organisés (primaryType=oak:QueryIndexDefinition AND type=&quot;ordered&quot;), qui ont été abandonnées depuis la version 6.1 et ont été supprimées dans la version 6.2."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=fr#the-ordered-index" text="Index organisé – Obsolète"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=fr" text="Indexation – AEM as a Cloud Service"

`DOPI` identifie l’utilisation de définitions d’index de propriété organisées (`primaryType=oak:QueryIndexDefinition` ET `type="ordered"`), obsolètes depuis la version 6.1 et supprimées dans la version 6.2.

## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Guide de mise en œuvre"
>abstract="Nous vous recommandons d’examiner tous les index organisés obsolètes et de les déplacer vers des index Lucene pris en charge afin d’éviter des problèmes de performances importants ou des exigences clientes non fonctionnelles."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/practices/best-practices-for-queries-and-indexing.html?lang=fr" text="Bonnes pratiques relatives aux requêtes et à l’indexation"

* Certaines requêtes peuvent ne pas répondre.
* La fonctionnalité du client peut ne pas fonctionner correctement.
* Les avertissements transversaux ou même les erreurs et les sanctions de performances importantes comme les index obsolètes n’ont aucun effet.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Outils et ressources"
>abstract="Examinez le projet WKND hérité et découvrez comment les violations du protocole DOPI peuvent être corrigées et rendues compatibles avec AEM Cloud Service. Consultez également l’exemple de violation du protocole DOPI sur Github pour comprendre comment les index organisés hérités peuvent être convertis en index Lucene pris en charge dans AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Projet hérité WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Exemple de violation du protocole DOPI – Github"

* Modifiez la définition d’index ou remplacez l’index par une définition d’index prise en charge. (Voir [Requêtes et indexation Oak](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=fr)).
* Examinez le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) et découvrez comment [les violations DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) peuvent être corrigées et rendues compatibles avec AEM as a Cloud Service.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
