---
title: LUI
description: Page d’aide sur le code de détection des motifs.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 100%

---

# LUI {#lui}

Interface d’utilisation héritée (Legacy User Interface, LUI)

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Interface d’utilisation héritée (Legacy User Interface, LUI)"
>abstract="La LUI identifie l’utilisation d’éléments d’interface d’utilisation obsolètes. Ces éléments ne sont pas recommandés ou ne sont pas pris en charge dans les versions ultérieures d’AEM et dans AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Changements notables - AEM as a Cloud Service"

La `LUI` identifie l’utilisation d’éléments d’interface d’utilisation obsolètes. Ces éléments ne sont pas recommandés ou ne sont pas pris en charge dans les versions ultérieures d’AEM et dans AEM as a Cloud Service.

Des sous-types permettent d’identifier les différents types d’éléments d’interface d’utilisation qui peuvent ou doivent être mis à niveau :

* `legacy.dialog.classic` : les boîtes de dialogue classiques de l’interface d’utilisation basées sur ExtJS doivent être remplacées par Coral.
   * Ce sous-type est détecté lorsque le nom de la boîte de dialogue est `dialog` ou `design_dialog` et lorsque la valeur de la propriété `jcr:primaryType` ou celle de `xtype` est `cq:Dialog`.
* `legacy.dialog.coral2` : les boîtes de dialogue `Coral 2` doivent être mises à jour pour utiliser `Coral 3`.
   * Ce sous-type est détecté lorsque la boîte de dialogue et ses noms de nœud de contenu enfant sont
      * `cq:dialog/content`,
      * `cq:design_dialog/content`,
      * `cq:dialog.coral2/content`,
      * ou `cq:design_dialog.coral2/content`,
et que la valeur de la propriété `sling:resourceType` ne contient pas `granite/ui/components/coral/foundation`.
* `legacy.custom.component` : les composants qui héritent de `foundation/components` doivent être mis à jour pour utiliser les composants principaux.
   * Ce sous-type est détecté lorsque la valeur de la propriété `jcr:primaryType` est `cq:Component` et que la
     valeur de la propriété `sling:resourceSuperType` contient « foundation/components ». Ou, l’une des valeurs de propriété
     `sling:resourceSuperType` de la chaîne de composants supertypes contient « foundation/components ».
* `legacy.static.template` : les modèles statiques doivent être mis à niveau vers les modèles modifiables.
   * Ce sous-type est détecté lorsque la valeur de la propriété `jcr:primaryType` est `cq:Template`.
* `content.fragment.template` : les templates de fragment de contenu doivent créer des modèles de fragment pour remplacer les templates de fragment.
   * Les schémas de fragment de contenu se trouvent aux emplacements suivants :
      * Les schémas de fragment de contenu prêts à l’emploi sont stockés dans `/libs/settings/dam/cfm/templates`.
      * Ils peuvent être superposés dans `/apps/settings/dam/cfm/templates` ou `/conf/.../settings/dam/cfm/templates`(... = global ou « tenant »).
* `translation.dictionary` : dictionnaire `I18n` présent sous `/apps`.
   * `/apps` est non modifiable au moment de l’exécution et translator.html ne serait plus disponible dans AEM as a Cloud Service.

## Implications et risques éventuels {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Guide de mise en œuvre"
>abstract="L’interface utilisateur classique n’est plus disponible dans AEM as a Cloud Service. L’interface standard de création est l’interface utilisateur tactile. La bonne pratique consiste à déplacer toutes les interfaces non prises en charge et à remanier les personnalisations liées pour les adapter aux fonctionnalités et capacités plus récentes compatibles avec AEM as a Cloud Service. Les clientes et clients peuvent utiliser les outils de modernisation AEM existants afin de faciliter la modernisation des implémentations AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Outils de modernisation d’AEM"

* L’interface utilisateur classique n’est plus disponible dans AEM as a Cloud Service. L’interface standard pour la création est l’interface utilisateur tactile.
* S’appuyer sur des composants personnalisés classiques peut augmenter les coûts de maintenance au fil du temps.
* Les templates de fragment de contenu ont remplacé les modèles de fragment de contenu dans AEM 6.3. La migration des fragments de contenu basés sur des modèles hérités vers AEM as a Cloud Service conserve la fonctionnalité de ces fragments, mais il n’est pas possible de créer des fragments basés sur le template hérité. Il est impossible aussi de diffuser ces fragments à l’aide d’AEM GraphQL, qui nécessite des modèles de fragments de contenu en tant que schémas.
* /apps est non modifiable au moment de l’exécution et translator.html ne serait plus disponible dans AEM as a Cloud Service. Ces dictionnaires `I18n` doivent provenir de Git par l’intermédiaire du pipeline CI/CD.

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Outils et ressources"
>abstract="Grâce aux outils de modernisation AEM, les clients peuvent convertir les boîtes de dialogue Classic(ExtJS) en boîtes de dialogue Coral. L’objectif est d’aider les clients à abandonner les fonctionnalités non prises en charge ou héritées pour adopter les fonctionnalités AEM, plus efficaces et modernes. Ces outils sont configurables, s’adaptent à leur configuration et offrent de nombreuses possibilités d’extension. Vous pouvez également envisager de remplacer les composants personnalisés par un jeu de composants principaux normalisés afin d’accélérer le temps de développement et de réduire les coûts de maintenance de vos applications."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Convertisseur de composants"
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-core-components/using/introduction" text="Composants principaux"

* Pour faciliter la modernisation de vos implémentations AEM Sites, utilisez la [suite d’outils de modernisation d’AEM](https://opensource.adobe.com/aem-modernize-tools/). Ces outils incluent la conversion :
   * des boîtes de dialogue classiques (ExtJS) vers les boîtes de dialogue Coral ;
   * des composants de base en composants principaux ;
   * des modèles statiques et de contrôle des colonnes en modèles modifiables et en grille réactive ;
   * des conceptions et boîtes de dialogue de conception en politiques de modèles modifiables.
* Si possible, examinez la bibliothèque de composants personnalisés et la transition de votre projet, en fonction de l’ensemble de [composants principaux](https://experienceleague.adobe.com/fr/docs/experience-manager-core-components/using/introduction) normalisés afin d’accélérer le temps de développement et de réduire les coûts de maintenance de vos applications.
* Créez des modèles de fragment de contenu avec des fonctionnalités équivalentes aux modèles hérités et utilisez ces modèles pour la création future de fragments de contenu. Pour plus d’informations, voir [Modèles de fragment de contenu](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models).
* Les dictionnaires `I18n` doivent provenir de Git par l’intermédiaire du pipeline CI/CD. [Documentation](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Contactez l’[équipe d’assistance AEM](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos préoccupations.
