---
title: DM
description: Page d’aide sur le code de la détection des motifs
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 100%

---

# DM {#dm}

Dynamic Media

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="Le code DM identifie l’utilisation d’AEM Assets Dynamic Media dans votre implémentation actuelle. Le mode Dynamic Media est détecté par le mode d’exécution."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=fr" text="Développement AEM – Conseils et bonnes pratiques"
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
>title="Guide de mise en œuvre"
>abstract="AEM as a Cloud Service ne prend en charge que le mode d’exécution dynamicmedia_scene7. Passez en revue les paramètres actuels et contactez l’équipe d’assistance Adobe pour obtenir de l’aide et plus d’informations."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html?lang=fr" text="Configuration de Dynamic Media"
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"


* `dynamic.media.runmode`
   * Pour plus d’informations, consultez [Configuration de Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html?lang=fr).

* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
