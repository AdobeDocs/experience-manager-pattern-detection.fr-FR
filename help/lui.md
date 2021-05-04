---
title: LUI
description: Page d’aide sur le code de la détection des motifs
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
translation-type: tm+mt
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 68%

---

# LUI {#lui}

Legacy User Interface (interface utilisateur classique)

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Legacy User Interface (interface utilisateur classique)"
>abstract="LUI identifie l’utilisation d’éléments d’interface utilisateur déconseillés qui ne sont pas recommandés ou ne sont pas pris en charge dans les versions ultérieures d’AEM et dans AEM en tant que Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=fr" text="Changements notables - AEM en tant que Cloud Service"

`LUI` identifie l’utilisation d’éléments d’interface utilisateur obsolètes qui ne sont pas recommandés ou ne sont pas pris en charge dans les versions ultérieures d’AEM et dans AEM as a Cloud Service.

Des sous-types permettent d’identifier les différents types d’éléments d’interface utilisateur qui peuvent ou doivent être mis à niveau :

* `legacy.dialog.classic` : les boîtes de dialogue classiques de l’interface utilisateur basées sur ExtJS doivent être remplacées par Coral.
   * Cela est détecté lorsque le nom de la boîte de dialogue est « dialog » ou « design_dialog » et lorsque la valeur de propriété `jcr:primaryType` ou la valeur de propriété `xtype` est « cq:Dialog ».
* `legacy.dialog.coral2` : les boîtes de dialogue Coral 2 doivent être mises à jour pour utiliser Coral 3.
   * Cela est détecté lorsque la boîte de dialogue et ses noms de nœud de contenu enfant sont « cq:dialog/content », « cq:design_dialog/content », « cq:dialog.coral2/content » ou « cq:design_dialog.coral2/content » et la valeur de propriété `sling:resourceType` ne contient pas
« granite/ui/components/coral/foundation ».
* `legacy.custom.component` : les composants qui héritent de `foundation/components`, doivent être mis à jour pour utiliser les composants principaux.
   * Cela est détecté lorsque la valeur de la propriété `jcr:primaryType` est « cq:Component » et que la valeur de la propriété
      `sling:resourceSuperType` contient « foundation/components » ou l’une des valeurs de propriété
      `sling:resourceSuperType` de la chaîne de composants supertypes contiennent « foundation/components ».
* `legacy.static.template` : les modèles statiques doivent être mis à niveau vers les modèles modifiables.
   * Cela est détecté lorsque la valeur de la propriété `jcr:primaryType` est « cq:Template ».

## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Guide de mise en oeuvre"
>abstract="L’interface utilisateur classique n’est plus disponible en tant que Cloud Service dans AEM et l’interface standard pour la création est l’interface utilisateur tactile. La bonne pratique consiste à déplacer toutes les interfaces non prises en charge et les personnalisations liées doivent être reconfigurées vers de nouvelles fonctionnalités compatibles avec AEM en tant que Cloud Service. Les clients peuvent tirer parti de la suite de modernisation des AEM existantes pour réduire les efforts nécessaires à la modernisation des implémentations de AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Outils de modernisation d’AEM"

* L’interface utilisateur classique n’est plus disponible dans AEM as a Cloud Service. L’interface standard pour la création est l’interface utilisateur tactile.
* S’appuyer sur des composants personnalisés classiques peut augmenter les coûts de maintenance au fil du temps.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Outils et ressources"
>abstract="Grâce à AEM Modernisation Suite, les clients peuvent convertir les boîtes de dialogue Classic(ExtJS) en boîtes de dialogue Coral. L’objectif est d’aider les clients à passer des fonctionnalités non prises en charge ou héritées aux offres d’AEM robustes et modernes. Ces outils sont configurables, adaptés à la configuration et extensibles. En outre, explorez le remplacement de composants personnalisés par l&#39;ensemble de composants principaux normalisés afin d&#39;accélérer le temps de développement et de réduire les coûts de maintenance de vos applications."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/component.html" text="Convertisseur de composants"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="Composants principaux"

* Utilisez la [suite des outils de modernisation d’AEM](https://opensource.adobe.com/aem-modernize-tools/) pour réduire les efforts nécessaires à la modernisation de vos implémentations AEM Sites. Ces outils incluent la conversion :
   * des boîtes de dialogue classiques (ExtJS) vers les boîtes de dialogue Coral ;
   * des composants de base en composants principaux ;
   * des modèles statiques et de contrôle des colonnes en modèles modifiables et en grille réactive ;
   * des conceptions et boîtes de dialogue de conception en stratégies de modèles modifiables.
* Si possible, examinez la bibliothèque de composants personnalisés et la transition de votre projet, en fonction de l’ensemble de [composants principaux](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=fr) normalisés afin d’accélérer le temps de développement et de réduire les coûts de maintenance de vos applications.
* Veuillez contacter notre [équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour obtenir des clarifications ou des réponses à vos questions.
