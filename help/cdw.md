---
title: CDW
description: Page d’aide sur le code de la détection des motifs
source-git-commit: 04709ba74eedad903669aae589c605542e1e3b09
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 44%

---

# CDW {#cdw}

Widget de boîte de dialogue personnalisée

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Widget de boîte de dialogue personnalisée"
>abstract="Le CDW identifie les widgets de boîte de dialogue personnalisés qui doivent être mis à jour pour qu’ils soient compatibles avec AEM as a Cloud Service."

`CDW`  Les widgets de boîte de dialogue personnalisés identifient les widgets personnalisés CoralUI et Classic dialog . Ils doivent être mis à jour pour être compatibles avec AEM as a Cloud Service.

Des sous-types sont utilisés pour identifier les différents types d’informations, notamment :

* `custom.coral.widget`: Identifiez les widgets de boîte de dialogue personnalisés en fonction de CoralUI 2 ou CoralUI 3.
* `custom.classic.widget`: Identifiez les widgets de boîte de dialogue personnalisés en fonction d’ExtJs.

## Enjeux et risques possibles {#implications-and-risks}

* L’interface utilisateur classique n’est plus disponible dans AEM as a Cloud Service. L’interface standard pour la création est l’interface utilisateur tactile.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Guide de mise en œuvre"
>abstract="Contactez l’assistance clientèle pour obtenir de l’aide."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Les widgets de boîte de dialogue personnalisés Classic doivent être convertis d’ExtJS en [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html).
* Les widgets de boîte de dialogue Coral personnalisés doivent être évalués pour la mise à jour vers CoralUI 3.
* Contactez notre [équipe d’assistance clientèle Experience Manager](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou pour répondre à vos préoccupations.
