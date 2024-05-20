---
title: DM
description: Découvrez comment le code du détecteur de motifs identifie l’utilisation d’AEM Assets - Dynamic Media.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 81%

---

# DM {#dm}

Dynamic Media

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="Le code DM identifie l’utilisation d’AEM Assets Dynamic Media dans votre implémentation actuelle. Le mode d’exécution détecte le mode Dynamic Media."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="Développement sur AEM – Conseils et bonnes pratiques"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Conseils de développement sur AEM as a Cloud Service"

`DM` (Dynamic Media) : identifie l’utilisation d’AEM Assets Dynamic Media. Le mode d’exécution détecte le mode Dynamic Media.

Un sous-type est utilisé avec ce code :

* `dynamic.media.runmode` : la valeur associée à ce sous-type, si elle est fournie, est :
   * `dynamicmedia` : Dynamic Media - Mode hybride
   * `dynamicmedia_scene7` : Dynamic Media - Mode Scene7

## Enjeux et risques possibles {#implications-and-risks}

* `dynamic.media.runmode`
   * Il peut y avoir des problèmes de mise à niveau liés à Dynamic Media.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Guide de mise en œuvre"
>abstract="AEM as a Cloud Service ne prend en charge que le mode d’exécution dynamicmedia_scene7. Passez en revue les paramètres actuels et contactez l’équipe d’assistance Adobe pour obtenir de l’aide et des clarifications."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Configuration de Dynamic Media"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"


* `dynamic.media.runmode`
   * Pour plus d’informations, consultez [Configurer Dynamic Media](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media).

* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
