---
title: CDW
description: Page d’aide sur le code de la détection des motifs
exl-id: a9e9dae8-0aa2-4679-a3c1-418cab01cfda
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 100%

---

# CDW {#cdw}

Widget personnalisé de boîte de dialogue

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Widget personnalisé de boîte de dialogue"
>abstract="Le CDW identifie les widgets personnalisés de boîte de dialogue qui doivent être mis à jour pour qu’ils soient compatibles avec AEM as a Cloud Service."

`CDW`  Les widgets personnalisés de boîte de dialogue identifient les widgets personnalisés de boîte de dialogue CoralUI et classique. Ils doivent être mis à jour pour être compatibles avec AEM as a Cloud Service.

Des sous-types sont utilisés pour identifier les différents types d’informations, notamment :

* `custom.coral.widget` : Identifiez les widgets personnalisés de boîte de dialogue en fonction de CoralUI 2 ou CoralUI 3.
* `custom.classic.widget` : Identifiez les widgets personnalisés de boîte de dialogue en fonction d’ExtJs.

## Enjeux et risques possibles {#implications-and-risks}

* L’interface utilisateur classique n’est plus disponible dans AEM as a Cloud Service. L’interface standard pour la création est l’interface utilisateur tactile.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Guide de mise en œuvre"
>abstract="Contactez l’assistance clientèle pour obtenir de l’aide."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Les widgets personnalisés de boîte de dialogue classique doivent être convertis d’ExtJS en [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html).
* Les widgets personnalisés de boîte de dialogue Coral doivent être évalués pour la mise à jour vers CoralUI 3.
* Contactez notre [équipe d’assistance clientèle Experience Manager](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou pour répondre à vos préoccupations.
