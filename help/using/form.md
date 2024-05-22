---
title: FORM
description: Page d’aide sur le code de détection des motifs.
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 85%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Contexte {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="FORMS"
>abstract="Le code Forms identifie les problèmes potentiels liés à la migration d’AEM (Adobe Experience Manager) Forms vers AEM Forms as a Cloud Service. Examinez les enjeux et les risques potentiels associés et traitez ces questions avant de migrer vers Cloud Service."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-manager-pattern-detection/table-of-contents/forms#implications-and-risks" text="Enjeux et risques possibles"

`FORMS` : identifie les problèmes potentiels liés à la migration d’[!DNL Adobe Experience Manager Forms] vers [!DNL Adobe Experience Manager Forms] as a [!DNL Cloud Service]. Résolvez ces problèmes avant de migrer vers [!DNL Cloud Service].

Les sous-types suivants vous aident à identifier les différents types de problèmes :

* `modified.feature` : ces fonctionnalités, ressources ou API ont été mises à jour ou modifiées pour Cloud Service. Avant de migrer vers Cloud Service, exécutez l’utilitaire de migration pour rendre ces fonctionnalités et ces ressources compatibles avec Cloud Service.
* `unavailable.feature` : votre environnement comporte des fonctionnalités et des ressources qui ne sont pas disponibles ou supprimées de Cloud Service. Ne migrez pas ces fonctionnalités ou ressources vers un environnement Cloud Service.
* `unsupported.feature` : votre environnement utilise certaines fonctionnalités qui ne sont pas encore prises en charge sur Cloud Service. Ne migrez pas ces fonctionnalités ou ressources vers un environnement Cloud Service. Consultez les notes de mise à jour mensuelles pour en savoir plus sur la disponibilité des fonctionnalités.
* `unsupported.api` : votre environnement comporte des API qui ne sont pas encore prises en charge par Cloud Service. Avant de migrer vers Cloud Service, désactivez, remplacez ou supprimez ces API de votre code. Consultez les notes de mise à jour mensuelles pour en savoir plus sur la disponibilité des fonctionnalités.

Pour plus d’informations sur les remplacements et autres actions nécessaires pour rendre certaines fonctionnalités et API compatibles avec Cloud Service, consultez les sections [Enjeux et risques possibles](#implications-and-risks) et [Solutions possibles](#solutions).

## Enjeux et risques possibles {#implications-and-risks}

Traitez les problèmes suivants avant de migrer vers [!DNL Adobe Experience Manager Forms as a Cloud Service]. Lorsque les enjeux et les risques listés ci-dessous ne sont pas résolus, certaines fonctionnalités ne fonctionnent pas comme prévu dans l’environnement Cloud Service.

* La fonctionnalité d’éditeur de code de la fonctionnalité d’éditeur de règles n’est pas disponible. (CODE_EDITOR)

* Par défaut, la prise en charge des e-mails (port SMTP) est désactivée. (EMAIL_SERVICE_CONFIGURATION)

* L’action d’envoi de **[!UICONTROL PDF par e-mail]** n’est pas disponible. (EMAIL_PDF_SUBMIT_ACTION)

* Les formulaires adaptatifs basés sur XFA ne sont pas encore pris en charge. (XFA_BASED_FORM, XDP_BASED_FORM)

* Une action d’envoi est immédiatement invoquée lors de l’envoi d’un formulaire au lieu d’attendre que tous les signataires signent. Par conséquent, le PDF de l’accord Adobe Sign envoyé aux signataires n’est pas disponible pour utilisation ou pour traitement dans le cadre des actions d’envoi. (FORM_SIGN_INTEGRATION)

* L’étape de signature n’est pas disponible. (SIGNATURE_STEP)

* L’étape de vérification n’est pas disponible. (VERIFY_STEP)

* L’action d’envoi **[!UICONTROL Envoyer vers Forms Workflow]** n’est pas disponible. Dans AEM version 6.5 de Forms et les versions précédentes, l’action Envoyer a été utilisée pour envoyer des données de formulaire adaptatif aux processus et LiveCycles Workflow AEM Forms on JEE hérités. (LC_WORKFLOW_SUBMISSION)

* La fonctionnalité Communications interactives n’est pas disponible. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* L’accordéon de métadonnées n’est pas disponible. (METADATA_ACCORDION_FORM_CONTAINER)

* Le composant CAPTCHA utilise maintenant le service Google reCAPTCHA pour valider le CAPTCHA, par défaut. L’option permettant d’utiliser Adobe Experience Manager pour valider le CAPTCHA est obsolète. (FORMS_CAPTCHA)

* L’application [!DNL AEM Forms] n’est pas disponible pour [!DNL Cloud Services]. (AEM_FORMS_APP)

* Les étapes des [services de document](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/forms/install-aem-forms/osgi-installation/install-configure-document-services#deployment-topology) ne sont pas disponibles dans les workflows AEM. (WORKFLOW_DOCSERVICES)

## Solutions possibles {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Guide de mise en œuvre"
>abstract="Les informations exposées dans le code de FORMS peuvent fournir des conseils sur les remplacements et les autres actions nécessaires pour rendre certaines fonctionnalités et API compatibles avec le Cloud Service. Contactez l’assistance Adobe pour obtenir de l’aide ou des clarifications."
>additional-url="https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html" text="Assistance Experience Cloud"

* Utilisez un utilitaire de migration pour convertir tous les scripts de règle de votre environnement en fonctions réutilisables. Vous pouvez utiliser les fonctions réutilisables avec l’éditeur de règles visuel pour continuer à obtenir les résultats obtenus avec les scripts de règle. (CODE_EDITOR)

* Contactez l’équipe d’assistance pour activer la fonctionnalité E-mail (ouverture du port SMTP) pour votre environnement. Par défaut, seules les connexions HTTP et HTTPS sortantes sont activées. (EMAIL_SERVICE_CONFIGURATION, étape de l’e-mail)

* Utilisez l’action d’envoi **[!UICONTROL Envoyer par courrier électronique]** au lieu de **[!UICONTROL Envoyer le PDF par courrier électronique]**. L’action d’envoi **[!UICONTROL Envoyer par courrier électronique]** fournit des options permettant d’envoyer des pièces jointes et de joindre un document d’enregistrement (DoR) à l’e-mail. (EMAIL_PDF_SUBMIT_ACTION)

* Les données envoyées contiennent l’ID d’accord Adobe Sign. Si nécessaire, vous pouvez utiliser l’identifiant de contrat Sign pour récupérer un PDF de contrat Sign. (FORM_SIGN_INTEGRATION)

* Supprimez l’étape Signature d’un formulaire adaptatif existant. Configurer votre formulaire adaptatif pour utiliser une [expérience de signature dans le navigateur](https://blog.developer.adobe.com/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Il affiche le contrat Adobe Sign pour signature dans le navigateur lors de l’envoi d’un formulaire adaptatif. L’expérience de signature dans le navigateur permet d’accélérer le processus et de faire gagner du temps au signataire. (SIGNATURE_STEP)

* Supprimez l’étape de vérification de vos formulaires adaptatifs existants avant de les déplacer vers un environnement [!DNL Cloud Service]. (VERIFY_STEP)

* Modifiez vos formulaires adaptatifs existants afin d’utiliser les actions d’envoi [Envoyer au point d’entrée REST](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-to-rest-endpoint), [Envoyer un e-mail](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#send-email), [Envoyer à l’aide du modèle de données de formulaire](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-using-form-data-model) et [Appeler un processus AEM](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow).

* Vous pouvez développer un workflow AEM et modifier vos formulaires adaptatifs existants afin d’utiliser l’action d’envoi [Workflow AEM](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) pour envoyer des données à un workflow AEM au lieu d’utiliser l’action d’envoi **[!UICONTROL Processus Envoyer aux formulaire]**. Vous pouvez développer une action d’envoi personnalisée pour envoyer des données, des pièces jointes ou un document d’enregistrement (DoR) à un processus LiveCycle au lieu d’utiliser [!UICONTROL Envoyer au Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Consultez les notes de mise à jour mensuelles pour en savoir plus sur la disponibilité de la fonction Communications interactives. N’effectuez pas la migration de vos communications interactives, lettres et dictionnaires associés vers un environnement Cloud Service tant que la fonction n’est pas disponible. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Il n’existe aucun remplacement pour l’accordéon de métadonnées. Supprimez-le de vos formulaires avant de les migrer vers Cloud Service. (METADATA_ACCORDION_FORM_CONTAINER)

* Utilisez Google reCaptcha au lieu du service CAPTCHA fourni par Adobe Experience Manager. (FORMS_CAPTCHA)

* Ne migrez pas vers un modèle de processus AEM qui utilise une étape de processus Document Services. De plus, ne migrez pas et ne mettez pas à jour des formulaires adaptatifs qui envoient des données d’utilisateurs et d’utilisatrices à un modèle de workflow qui utilise des étapes de workflow Services de document, et ne modifiez pas l’`Submit Action` en action [prise en charge](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions) avant de migrer le formulaire. (WORKFLOW_DOCSERVICES)

* Les formulaires adaptatifs offrent un design réactif. Ces formulaires modifient l’aspect, la conception et l’interactivité en fonction de l’appareil sous-jacent. Vous pouvez continuer à utiliser le Forms adaptatif sur un périphérique mobile. Recherchez des notes de mise à jour mensuelles pour plus d’informations sur la disponibilité du [!DNL AEM Forms] application. (AEM_FORMS_APP)

* La prise en charge des formulaires adaptatifs basés sur XFA n’est pas disponible sans configuration supplémentaire. Si vous envisagez d’utiliser des formulaires adaptatifs basés sur XFA, contactez l’assistance Adobe pour connaître votre cas d’utilisation et ses exigences spécifiques.(XFA_BASED_FORM, XDP_BASED_FORM)

Contactez l’[assistance Adobe](https://helpx.adobe.com/fr/enterprise/using/support-for-experience-cloud.html) si vous avez besoin de clarifications ou de réponses à vos questions.
