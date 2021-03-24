---
title: LUI
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# LUI {#lui}

Interface utilisateur héritée

## Arrière-plan {#background}

`LUI` identifie l’utilisation d’éléments d’interface utilisateur déconseillés qui ne sont pas recommandés ou ne sont pas pris en charge dans les versions ultérieures d’AEM et dans AEM en tant que Cloud Service.

Les sous-types permettent d’identifier les différents types d’éléments d’interface utilisateur qui doivent ou doivent être mis à niveau :

* `legacy.dialog.classic`: Les boîtes de dialogue classiques de l’interface utilisateur basées sur ExtJS doivent être remplacées par Coral.
   * Ceci est détecté lorsque le nom de la boîte de dialogue est &quot;dialog&quot; ou &quot;design_dialog&quot; et lorsque
la valeur de propriété `jcr:primaryType` ou la valeur de propriété `xtype` est &quot;cq:Dialog&quot;.
* `legacy.dialog.coral2`: Les boîtes de dialogue Coral 2 doivent être mises à jour pour utiliser Coral 3.
   * Ceci est détecté lorsque la boîte de dialogue et ses noms de noeud de contenu enfant sont &quot;cq:dialog/content&quot;,
&quot;cq:design_dialog/content&quot;, &quot;cq:dialog.coral2/content&quot; ou &quot;cq:design_dialog.coral2/content&quot;
et la valeur de propriété `sling:resourceType` ne contient pas
&quot;granit/ui/components/coral/foundation&quot;.
* `legacy.custom.component`: Les composants qui héritent de  `foundation/components`, doivent être mis à jour pour utiliser les composants principaux.
   * Ceci est détecté lorsque la valeur de la propriété `jcr:primaryType` est &quot;cq:Component&quot; et que la variable
      `sling:resourceSuperType` La valeur de propriété contient &quot;foundation/components&quot; ou l’une des valeurs suivantes :
      `sling:resourceSuperType` les valeurs de propriété de la chaîne de composants supertypes contiennent &quot;fondation/composants&quot;.
* `legacy.static.template`: Les modèles statiques doivent être mis à niveau vers les modèles modifiables.
   * Ceci est détecté lorsque la valeur de la propriété `jcr:primaryType` est &quot;cq:Template&quot;.

## Incidences possibles et risques {#implications-and-risks}

* L’interface utilisateur classique n’est plus disponible en tant que Cloud Service dans AEM. L’interface utilisateur standard pour la création est tactile.
* S&#39;appuyer sur des composants personnalisés hérités peut augmenter les coûts de maintenance au fil du temps.

## Solutions possibles {#solutions}

* Utilisez [AEM Modernization Tools suite](https://opensource.adobe.com/aem-modernize-tools/) pour réduire les efforts nécessaires à la modernisation de vos implémentations AEM Sites. Ces outils incluent la conversion de :
   * Boîtes de dialogue classiques (ExtJS) vers les boîtes de dialogue Coral
   * Les composants de base en composants principaux
   * Modèles statiques et contrôle des colonnes en modèles modifiables et grille réactive
   * Conception et conception de boîtes de dialogue pour modifier des stratégies de modèles
* Examinez la bibliothèque et la transition de composants personnalisés de votre projet, si possible, en fonction de l&#39;ensemble de [composants de base](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=fr) normalisés afin d&#39;accélérer le temps de développement et de réduire les coûts de maintenance de vos applications.
* Veuillez contacter notre [AEM équipe d&#39;assistance](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
