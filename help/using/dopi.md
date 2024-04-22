---
title: DOPI
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 44%

---

# DOPI {#dopi}

Deprecated Ordered Property Index (index des propriétés organisées obsolètes)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Deprecated Ordered Property Index (index des propriétés organisées obsolètes)"
>abstract="Le code DOPI identifie l’utilisation de définitions d’index de propriété classées (`primaryType=oak:QueryIndexDefinition` AND type=&quot;ordered&quot;), qui ont été abandonnés depuis la version 6.1 et ont été supprimés dans la version 6.2."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="Index organisé – Obsolète"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/operations/indexing" text="Indexation – AEM as a Cloud Service"

DOPI identifie l’utilisation de définitions d’index de propriété classées (`primaryType=oak:QueryIndexDefinition` ET `type="ordered"`), qui ont été abandonnés depuis la version 6.1 et ont été supprimés dans la version 6.2.

## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Guide de mise en œuvre"
>abstract="La bonne pratique consiste à passer en revue tous les index ordonnés obsolètes et à les déplacer vers des index Lucene pris en charge afin d’éviter des problèmes de performances significatifs ou des exigences client non fonctionnelles."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/practices/best-practices-for-queries-and-indexing" text="Bonnes pratiques relatives aux requêtes et à l’indexation"

* Certaines requêtes peuvent ne pas répondre.
* La fonctionnalité du client peut ne pas fonctionner correctement.
* Les avertissements transversaux ou même les erreurs et les sanctions de performances importantes comme les index obsolètes n’ont aucun effet.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Outils et ressources"
>abstract="Examinez le projet WKND hérité et découvrez comment les violations du protocole DOPI peuvent être corrigées et rendues compatibles avec AEM Cloud Service. Consultez également l’ exemple de violation DOPI sur GitHub pour comprendre comment les index triés hérités peuvent être convertis en index Lucene pris en charge dans AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Projet hérité WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Exemple de violation DOPI - GitHub"

* Modifiez la définition d’index afin qu’elle devienne (ou remplace l’index par) une définition d’index prise en charge. (Voir [Requêtes et indexation Oak](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing)).
* Examinez le projet [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) et découvrez comment [les violations DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) peuvent être corrigées et rendues compatibles avec AEM as a Cloud Service.
* Contactez le [Équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
