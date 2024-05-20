---
title: LUI
description: Page d’aide sur le code de détection des motifs.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 49%

---

# LUI {#lui}

Legacy User Interface (interface utilisateur classique)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Legacy User Interface (interface utilisateur classique)"
>abstract="LUI identifie l’utilisation d’éléments d’interface utilisateur obsolètes. Ces éléments qui ne sont pas recommandés ou qui ne sont pas pris en charge dans les versions ultérieures d’AEM et dans AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Changements notables - AEM as a Cloud Service"

`LUI`  Identifie l’utilisation d’éléments d’interface utilisateur obsolètes. Ces éléments ne sont pas recommandés ou ne sont pas pris en charge dans les versions ultérieures d’AEM et dans AEM as a Cloud Service.

Des sous-types permettent d’identifier les différents types d’éléments d’interface utilisateur qui peuvent ou doivent être mis à niveau :

* `legacy.dialog.classic`: les boîtes de dialogue de l’interface utilisateur classique basées sur ExtJS doivent être remplacées par Coral.
   * Ce sous-type est détecté lorsque le nom de la boîte de dialogue est `dialog` ou `design_dialog` et lorsque la variable `jcr:primaryType` ou la valeur de la propriété `xtype` La valeur de la propriété est `cq:Dialog`.
* `legacy.dialog.coral2` : les boîtes de dialogue `Coral 2` doivent être mises à jour pour utiliser `Coral 3`.
   * Ce sous-type est détecté lorsque la boîte de dialogue et ses noms de noeud de contenu enfant sont
      * `cq:dialog/content`,
      * `cq:design_dialog/content`,
      * `cq:dialog.coral2/content`,
      * ou `cq:design_dialog.coral2/content`
et la variable `sling:resourceType` La valeur de propriété ne contient pas `granite/ui/components/coral/foundation`.
* `legacy.custom.component` : les composants qui héritent de `foundation/components` doivent être mis à jour pour utiliser les composants principaux.
   * Ce sous-type est détecté lorsque la variable `jcr:primaryType` La valeur de la propriété est `cq:Component` et la variable
     `sling:resourceSuperType` La valeur de propriété contient &quot;foundation/components&quot;. Ou, l’une des valeurs de propriété
     `sling:resourceSuperType` Les valeurs de propriété de la chaîne des composants supertype contiennent &quot;foundation / components&quot;.
* `legacy.static.template` : les modèles statiques doivent être mis à niveau vers les modèles modifiables.
   * Ce sous-type est détecté lorsque la variable `jcr:primaryType` La valeur de la propriété est `cq:Template`.
* `content.fragment.template`: les modèles de fragment de contenu doivent créer des modèles de fragment pour remplacer les modèles de fragment.
   * Les schémas de fragment de contenu se trouvent aux emplacements suivants :
      * Les schémas de fragment de contenu prêts à l’emploi sont stockés dans `/libs/settings/dam/cfm/templates`.
      * Ils peuvent être superposés dans `/apps/settings/dam/cfm/templates` ou `/conf/.../settings/dam/cfm/templates`(... = global ou « tenant »).
* `translation.dictionary`: `I18n` dictionnaire présent sous `/apps`.
   * `/apps` est inaltérable au moment de l’exécution et translation.html ne sera plus disponible dans AEM as a cloud service.

## Enjeux et risques possibles {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Guide de mise en œuvre"
>abstract="L’interface utilisateur classique n’est plus disponible dans AEM as a Cloud Service. L’interface standard de création est l’interface utilisateur tactile. La bonne pratique consiste à déplacer toutes les interfaces non prises en charge et les personnalisations liées vers de nouvelles fonctionnalités compatibles avec AEM as a Cloud Service. Les clientes et clients peuvent utiliser les outils de modernisation AEM existants afin de faciliter la modernisation des implémentations AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Outils de modernisation d’AEM"

* L’interface utilisateur classique n’est plus disponible dans AEM as a Cloud Service. L’interface standard pour la création est l’interface utilisateur tactile.
* S’appuyer sur des composants personnalisés classiques peut augmenter les coûts de maintenance au fil du temps.
* Les modèles de fragment de contenu ont remplacé les modèles de fragment de contenu dans AEM 6.3. La migration de fragments de contenu basés sur des modèles hérités vers AEM as a Cloud Service conserve ces fragments comme fonctionnels, mais il n’est pas possible de créer des fragments basés sur le modèle hérité. Il n’est pas non plus possible de diffuser ces fragments à l’aide d’AEM GraphQL, qui nécessite des modèles de fragment de contenu comme schémas.
* /apps est non modifiable au moment de l’exécution et translator.html ne serait plus disponible dans AEM as a Cloud Service. Ainsi, `I18n` Les dictionnaires doivent provenir de Git par le biais du pipeline CI/CD.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Outils et ressources"
>abstract="Grâce aux outils de modernisation AEM, les clients peuvent convertir les boîtes de dialogue Classic(ExtJS) en boîtes de dialogue Coral. L’objectif est d’aider les clients à abandonner les fonctionnalités non prises en charge ou héritées pour adopter les fonctionnalités AEM, plus efficaces et modernes. Ces outils sont configurables, s’adaptent à leur configuration et offrent de nombreuses possibilités d’extension. Vous pouvez également envisager de remplacer les composants personnalisés par un jeu de composants principaux normalisés afin d’accélérer le temps de développement et de réduire les coûts de maintenance de vos applications."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Convertisseur de composants"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-core-components/using/introduction" text="Composants principaux"

* Pour réduire les efforts nécessaires à la modernisation de vos mises en oeuvre AEM Sites, utilisez le [Suite d’outils de modernisation d’AEM](https://opensource.adobe.com/aem-modernize-tools/). Ces outils incluent la conversion :
   * des boîtes de dialogue classiques (ExtJS) vers les boîtes de dialogue Coral ;
   * des composants de base en composants principaux ;
   * Modèles statiques et contrôle des colonnes vers des modèles modifiables et une grille réactive
   * Conceptions et boîtes de dialogue de conception pour modifier les stratégies de modèle
* Si possible, examinez la bibliothèque de composants personnalisés et la transition de votre projet, en fonction de l’ensemble de [composants principaux](https://experienceleague.adobe.com/fr/docs/experience-manager-core-components/using/introduction) normalisés afin d’accélérer le temps de développement et de réduire les coûts de maintenance de vos applications.
* Créez des modèles de fragment de contenu dotés de fonctionnalités équivalentes aux modèles hérités et utilisez ces modèles pour la création future de fragments de contenu. Pour plus d’informations, voir [Modèles de fragment de contenu](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models).
* `I18n` Les dictionnaires doivent provenir de Git via le pipeline CI/CD. [Documentation](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
