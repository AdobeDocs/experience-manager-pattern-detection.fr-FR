---
title: FORM
description: Page d’aide du code de l’outil de détection des motifs.
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 73%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Arrière-plan {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="FORMS"
>abstract="FORMS identifie les problèmes potentiels liés à la migration d’Adobe Experience Manager Forms vers Adobe Experience Manager Forms as a Cloud Service. Examinez les implications et les risques possibles associés et apportez une réponse à ces problèmes avant de migrer vers Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-pattern-detection/table-of-contents/forms#implications-and-risks" text="Enjeux et risques possibles"

`FORMS`  Identifie les problèmes potentiels liés à la migration depuis [!DNL Adobe Experience Manager Forms] to [!DNL Adobe Experience Manager Forms] as a [!DNL Cloud Service]. Résolvez ces problèmes avant de migrer vers [!DNL Cloud Service].

Les sous-types suivants vous aident à identifier les différents types de problèmes :

* `modified.feature` : ces fonctionnalités, ressources ou API ont été mises à jour ou modifiées pour Cloud Service. Avant de migrer vers Cloud Service, exécutez l’utilitaire de migration pour rendre ces fonctionnalités et ces ressources compatibles avec Cloud Service.
* `unavailable.feature` : votre environnement comporte des fonctionnalités et des ressources qui ne sont pas disponibles ou supprimées de Cloud Service. Ne migrez pas ces fonctionnalités ou ressources vers un environnement Cloud Service.
* `unsupported.feature` : votre environnement utilise certaines fonctionnalités qui ne sont pas encore prises en charge sur Cloud Service. Ne migrez pas ces fonctionnalités ou ressources vers un environnement Cloud Service. Consultez les notes de mise à jour mensuelles pour en savoir plus sur la disponibilité des fonctionnalités.
* `unsupported.api` : votre environnement comporte des API qui ne sont pas encore prises en charge par Cloud Service. Avant de migrer vers Cloud Service, désactivez, remplacez ou supprimez ces API de votre code. Consultez les notes de mise à jour mensuelles pour en savoir plus sur la disponibilité des fonctionnalités.

Pour plus d’informations sur les remplacements et autres actions nécessaires pour rendre certaines fonctionnalités et API compatibles avec Cloud Service, consultez les sections [Enjeux et risques possibles](#implications-and-risks) et [Solutions possibles](#solutions).

## Enjeux et risques possibles {#implications-and-risks}

Traitez les problèmes suivants avant de migrer vers [!DNL Adobe Experience Manager Forms as a Cloud Service]. Lorsque les enjeux et les risques listés ci-dessous ne sont pas résolus, certaines fonctionnalités ne fonctionnent pas comme prévu dans l’environnement Cloud Service.

* La fonctionnalité d’éditeur de code de la fonctionnalité d’éditeur de règles n’est pas disponible. (CODE_EDITOR)

* La prise en charge des emails (port SMTP) est désactivée par défaut. (EMAIL_SERVICE_CONFIGURATION)

* L’action d’envoi de **[!UICONTROL PDF par e-mail]** n’est pas disponible. (EMAIL_PDF_SUBMIT_ACTION)

* Les formulaires adaptatifs basés sur XFA ne sont pas encore pris en charge. (XFA_BASED_FORM, XDP_BASED_FORM)

* Une action d’envoi est immédiatement invoquée lors de l’envoi d’un formulaire au lieu d’attendre que tous les signataires signent. Par conséquent, le PDF de l’accord Adobe Sign envoyé aux signataires n’est pas disponible pour utilisation ou pour traitement dans le cadre des actions d’envoi. (FORM_SIGN_INTEGRATION)

* L’étape de signature n’est pas disponible. (SIGNATURE_STEP)

* L’étape de vérification n’est pas disponible. (VERIFY_STEP)

* L’action d’envoi **[!UICONTROL Envoyer vers Forms Workflow]** n’est pas disponible. Dans AEM Forms version 6.5 et les versions précédentes, l’action d’envoi était utilisée pour envoyer des données de formulaires adaptatifs aux workflows LiveCycle et JEE AEM Forms hérités. (LC_WORKFLOW_SUBMISSION)

* La fonctionnalité de communications interactives n’est pas disponible. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* L’accordéon de métadonnées n’est pas disponible. (METADATA_ACCORDION_FORM_CONTAINER)

* Le composant CAPTCHA utilise maintenant le service Google reCAPTCHA pour valider le CAPTCHA, par défaut. L’option permettant d’utiliser Adobe Experience Manager pour valider le CAPTCHA est obsolète. (FORMS_CAPTCHA)

* L’application [!DNL AEM Forms] n’est pas disponible pour [!DNL Cloud Services]. (AEM_FORMS_APP)

* [Services de document](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/forms/install-aem-forms/osgi-installation/install-configure-document-services#deployment-topology) Les étapes ne sont pas disponibles dans AEM Workflows. (WORKFLOW_DOCSERVICES)

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Guide de mise en œuvre"
>abstract="Les informations exposées dans le code de FORMS peuvent fournir des conseils sur les remplacements et les autres actions nécessaires pour rendre certaines fonctionnalités et API compatibles avec le Cloud Service. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Utilisez l’utilitaire de migration pour convertir tous les scripts de règle de votre environnement en fonctions réutilisables. Vous pouvez utiliser les fonctions réutilisables avec l’éditeur de règles visuelles pour continuer à accéder aux résultats obtenus avec les scripts de règles. (CODE_EDITOR)

* Contactez l’équipe d’assistance afin qu’elle puisse activer la fonctionnalité de courrier électronique (ouvrez le port SMTP) pour votre environnement. Seules les connexions HTTP et HTTPS sortantes sont activées par défaut. (EMAIL_SERVICE_CONFIGURATION, étape de l’e-mail)

* Utilisez l’action d’envoi **[!UICONTROL Envoyer par courrier électronique]** au lieu de **[!UICONTROL Envoyer le PDF par courrier électronique]**. L’action d’envoi **[!UICONTROL Envoyer par courrier électronique]** fournit des options permettant d’envoyer des pièces jointes et de joindre un document d’enregistrement (DoR) à l’e-mail. (EMAIL_PDF_SUBMIT_ACTION)

* Les données envoyées contiennent l’ID d’accord Adobe Sign. Si nécessaire, vous pouvez utiliser l’identifiant de signature d’accord pour récupérer un PDF de signature d’accord. (FORM_SIGN_INTEGRATION)

* Supprimez l’étape Signature d’un formulaire adaptatif existant. Configurez votre formulaire adaptatif pour utiliser [l’expérience de signature dans le navigateur](https://blog.developer.adobe.com/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Il affichera ainsi l’accord Adobe Sign permettant de signer l’accord dans le navigateur lors de l’envoi d’un formulaire adaptatif. L’expérience de signature dans le navigateur permet d’accélérer le processus et de faire gagner du temps au signataire. (SIGNATURE_STEP)

* Supprimez l’étape de vérification de votre Forms adaptatif existant avant de déplacer ces formulaires vers une [!DNL Cloud Service] environnement. (VERIFY_STEP)

* Modifier vos formulaires adaptatifs existants pour pouvoir utiliser [Envoyer vers le point de fin REST](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-to-rest-endpoint), [Envoyer un email](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#send-email), [Envoyer à l’aide du modèle de données de formulaire](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-using-form-data-model), et [Appeler un workflow d’AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) Actions Envoyer.

* Vous pouvez développer un processus d’AEM et modifier vos formulaires adaptatifs existants pour utiliser [Processus AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) Action Envoyer pour envoyer des données à un workflow AEM au lieu d’utiliser la variable **[!UICONTROL Envoyer au Forms Workflow]** Action Envoyer. Vous pouvez développer une action d’envoi personnalisée pour envoyer des données, des pièces jointes ou un document d’enregistrement (DoR) à un processus LiveCycle au lieu d’utiliser [!UICONTROL Envoyer au Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Consultez les notes de mise à jour mensuelles pour en savoir plus sur la disponibilité de la fonction Communications interactives. N’effectuez pas la migration de vos communications interactives, lettres et dictionnaires associés vers un environnement Cloud Service tant que la fonction n’est pas disponible. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Il n’existe aucun remplacement pour l’accordéon de métadonnées. Supprimez-le de vos formulaires avant de les migrer vers Cloud Service. (METADATA_ACCORDION_FORM_CONTAINER)

* Utilisez Google reCAPTCHA au lieu du service CAPTCHA fourni par Adobe Experience Manager. (FORMS_CAPTCHA)

* Ne migrez pas un modèle de processus d’AEM qui utilise une étape de processus de services de document. De plus, ne migrez pas ou ne mettez pas à jour les Forms adaptatives qui envoient des données utilisateur à un modèle de processus qui utilise les étapes de processus des services de document ou ne modifiez pas la variable `Submit Action` à [compatible](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions) avant de migrer le formulaire. (WORKFLOW_DOCSERVICES)

* Les formulaires adaptatifs offrent un design réactif. Ces formulaires changent d’aspect, de conception et d’interactivité en fonction de l’appareil concerné. Vous pouvez continuer à utiliser les formulaires adaptatifs sur un appareil mobile. Consultez les notes de mise à jour mensuelles pour en savoir plus sur la disponibilité de l’application [!DNL AEM Forms]. (AEM_FORMS_APP)

* La prise en charge des formulaires adaptatifs basés sur XFA n’est pas disponible sans configuration supplémentaire. Si vous envisagez d’utiliser des formulaires adaptatifs basés sur XFA, contactez l’assistance Adobe pour connaître votre cas d’utilisation et ses exigences spécifiques.(XFA_BASED_FORM, XDP_BASED_FORM)

Contact [Prise en charge des Adobes](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) pour des clarifications ou pour répondre à des préoccupations.
