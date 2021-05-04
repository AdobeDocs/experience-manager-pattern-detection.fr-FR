---
title: DM
description: Page d’aide sur le code de la détection des motifs
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 76%

---

# DM {#dm}

Dynamic Media

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="Le code DM identifie l&#39;utilisation d&#39;AEM Assets Dynamic Media dans votre implémentation actuelle. Le mode Dynamic Media est détecté par le mode d’exécution."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=fr" text="Développement des AEM - Lignes directrices et bonnes pratiques"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=fr" text="Conseils de développement pour AEM as a Cloud Service"

`DM` identifie l’utilisation de Dynamic Media avec AEM Assets. Le mode Dynamic Media est détecté par le mode d’exécution.

Un sous-type est utilisé avec ce code :

* `dynamic.media.runmode` : la valeur associée à ce sous-type, si elle est fournie, est :
   * `dynamicmedia` : Dynamic Media - Mode hybride
   * `dynamicmedia_scene7` : Dynamic Media - Mode Scene7

## Enjeux et risques possibles {#implications-and-risks}

* `dynamic.media.runmode`
   * Il peut y avoir des problèmes de mise à niveau liés à Dynamic Media.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Guide de mise en oeuvre"
>abstract="AEM en tant que Cloud Service ne prend en charge que le mode d’exécution dynamicmedia_scene7. Veuillez consulter les paramètres actuels et contacter l&#39;équipe d&#39;assistance à l&#39;Adobe pour obtenir de l&#39;aide et des éclaircissements."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html" text="Configuration de Dynamic Media"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"


* `dynamic.media.runmode`
   * Pour plus d’informations, consultez [Configuration de Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html?lang=fr).

* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
