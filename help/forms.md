---
title: FORMULAIRE
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: aa44c3ce87496f412191000f1980a7ebbde386cd
workflow-type: tm+mt
source-wordcount: '1143'
ht-degree: 0%

---


# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Arrière-plan {#background}

`FORMS` Identifie les problèmes potentiels liés à la migration  [!DNL Adobe Experience Manager Forms] vers  [!DNL Adobe Experience Manager Form]s en tant que  [!DNL Cloud Service]problème. Résolvez ces problèmes avant de migrer vers [!DNL Cloud Service].

Les sous-types suivants vous aident à identifier les différents types de problèmes :

* `modified.feature`: Ces fonctionnalités, ressources ou API ont été mises à jour ou modifiées pour le Cloud Service. Avant de migrer vers le Cloud Service, exécutez l’utilitaire de migration pour rendre ces fonctions et ressources compatibles avec le Cloud Service.
* `unavailable.feature`: Votre environnement comporte des fonctions et des ressources qui ne sont pas disponibles ou supprimées du Cloud Service. Ne migrez pas ces fonctions ou ressources vers un environnement Cloud Service.
* `unsupported.feature`: Votre environnement utilise certaines fonctionnalités qui ne sont pas encore prises en charge sur le Cloud Service. Ne migrez pas ces fonctions ou ressources vers un environnement Cloud Service. Surveillez les notes de mise à jour mensuelles pour connaître la disponibilité des fonctionnalités.
* `unsupported.api`: Votre environnement comporte des API qui ne sont pas encore prises en charge par le Cloud Service. Avant de migrer vers le Cloud Service, désactivez, remplacez ou supprimez ces API de votre code. Surveillez les notes de mise à jour mensuelles pour connaître la disponibilité des fonctionnalités.

Pour plus d&#39;informations sur les remplacements et autres actions nécessaires pour rendre certaines fonctions et API compatibles avec le Cloud Service, consultez les sections [Enjeux et risques possibles](#implications-and-risks) et [Solutions possibles](#solutions).

## Incidences possibles et risques {#implications-and-risks}

Résolvez les problèmes suivants avant de migrer vers [!DNL Adobe Experience Manager Forms as a Cloud Service]. Lorsque les implications et les risques énumérés ci-dessous ne sont pas pris en compte, certaines caractéristiques ne fonctionnent pas comme prévu dans l&#39;environnement Cloud Service.

* La fonctionnalité d&#39;éditeur de code de la fonction d&#39;éditeur de règles n&#39;est pas disponible. (CODE_EDITOR)

* Par défaut, la prise en charge du courrier électronique (port SMTP) est désactivée. (EMAIL_SERVICE_CONFIGURATION)

* L&#39;action d&#39;envoi **[!UICONTROL Envoyer le PDF par courriel]** n&#39;est pas disponible.(EMAIL_PDF_SUBMIT_ACTION)

* La Forms adaptative basée sur XFA n’est pas encore prise en charge. (XFA_BASED_FORM, XDP_BASED_FORM)

* Une action Envoyer est appelée immédiatement lors de l’envoi du formulaire au lieu d’attendre que tous les signataires terminent la signature. Par conséquent, le PDF de l’accord Adobe Sign envoyé aux signataires n’est pas disponible pour que les actions d’envoi soient utilisées ou traitées. (FORM_SIGN_INTEGRATION)

* L&#39;étape Signature n&#39;est pas disponible. (SIGNATURE_STEP)

* L&#39;étape Vérifier n&#39;est pas disponible. (VERIFY_STEP)

* La fonction Portail Forms et l&#39;**[!UICONTROL Action d&#39;envoi du portail Forms]** ne sont pas encore disponibles. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* L&#39;action d&#39;envoi **[!UICONTROL Envoyer au Forms Workflow]** n&#39;est pas disponible. Dans [!DNL AEM 6.5 Forms] et les versions précédentes, l’action Envoyer a été utilisée pour envoyer des données de formulaire adaptatif aux Workflows et LiveCycles Workflow [!DNL AEM Forms on JEE] hérités. (LC_WORKFLOW_SUBMISSION)

* La fonctionnalité de communications interactives n&#39;est pas disponible.  (FP_PROFIL_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL Les fonctions Enregistrer en tant que]** brouillon et  **** Enregistrement automatique des formulaires adaptatifs ne sont pas prises en charge pour le moment. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* L’accordéon de métadonnées n’est pas disponible. (METADATA_ACCORDION_FORM_CONTENEUR)

* Le composant CAPTCHA utilise maintenant le service Google reCAPTCHA pour valider CAPTCHA, par défaut. L&#39;option permettant d&#39;utiliser Adobe Experience Manager pour valider CAPTCHA est obsolète. (FORMS_CAPTCHA)

* [!DNL AEM Forms] n’est pas disponible pour  [!DNL Cloud Services]. (AEM_FORMS_APP)

* [Les étapes ](https://experienceleague.adobe.com/docs/experience-manager-65/forms/install-aem-forms/osgi-installation/install-configure-document-services.html?lang=en#deployment-topology) de document Services ne sont pas disponibles dans les Workflows AEM. (WORKFLOW_DOCSERVICES)

## Solutions possibles {#solutions}

* Utilisez l’utilitaire de migration pour convertir tous les scripts de règle de votre environnement en fonctions réutilisables. Vous pouvez utiliser les fonctions réutilisables avec l’éditeur de règles visuelles pour continuer à obtenir les résultats obtenus avec les scripts de règles. (CODE_EDITOR)

* Contactez l’équipe d’assistance pour activer la fonctionnalité de courrier électronique (ouvrez le port SMTP) pour votre environnement. Par défaut, seules les connexions HTTP et HTTPS sortantes sont activées. (EMAIL_SERVICE_CONFIGURATION, étape E-mail)

* Utilisez **[!UICONTROL Courrier électronique]** Action d’envoi au lieu de **[!UICONTROL Courriel PDF]**. L&#39;action d&#39;envoi **[!UICONTROL Courrier électronique]** fournit des options pour envoyer des pièces jointes et joindre un Document d&#39;enregistrement (DE) par courrier électronique. (EMAIL_PDF_SUBMIT_ACTION)

* Les données envoyées contiennent l’identifiant de l’accord Adobe Sign. Si nécessaire, vous pouvez utiliser l’ID d’accord de signature pour récupérer un PDF d’accord de signature.  (FORM_SIGN_INTEGRATION)

* Supprimez l’étape Signature d’un formulaire adaptatif existant. Configurez votre formulaire adaptatif pour qu’il utilise [l’expérience de signature dans le navigateur](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Il affiche l’accord Adobe Sign pour signer l’accord dans le navigateur lors de l’envoi d’un formulaire adaptatif. L’expérience de signature dans le navigateur permet d’accélérer la signature et de gagner du temps pour le signataire. (SIGNATURE_STEP)

* Supprimez l’étape de vérification de votre Forms adaptatif existant avant de déplacer ces formulaires vers un environnement [!DNL Cloud Service]. (VERIFY_STEP)

* Modifiez vos formulaires adaptatifs existants afin d’utiliser [Envoyer au point de terminaison REST](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-to-rest-endpoint), [Envoyer un courrier électronique](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#send-email), [Envoyer à l’aide du modèle de données de formulaire](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-using-form-data-model) et [Appeler un processus d’AEM](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Envoyer des actions. Forms Portal et l’action d’envoi de Forms Portal ne sont pas encore disponibles. Surveillez les notes de mise à jour mensuelles pour connaître la disponibilité des fonctionnalités. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL)

* Vous pouvez développer un flux de travail AEM et modifier vos formulaires adaptatifs existants afin d’utiliser [AEM flux de travail](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Action d’envoi pour envoyer des données à un flux de travail d’AEM au lieu d’utiliser l’action d’envoi **[!UICONTROL Envoyer à l’Forms Workflow]**. Vous pouvez développer une action Envoyer personnalisée pour envoyer des données, des pièces jointes ou un Document d’enregistrement (DE) à un processus de LiveCycle au lieu d’utiliser [!UICONTROL Envoyer au Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Surveillez les notes de mise à jour mensuelles pour connaître la disponibilité de la fonction Communications interactives. N’effectuez pas la migration de vos communications interactives, lettres et dictionnaires associés vers un environnement Cloud Service tant que la fonction n’est pas disponible. (FP_PROFIL_INTERACTIVE_COMMUNICATIONS)

* Désactivez l’option **[!UICONTROL Enregistrer en tant que brouillon]** et **[!UICONTROL Activer l’enregistrement automatique]** dans votre Forms adaptatif avant de les migrer vers le Cloud Service. Vous pouvez activer ces options une fois que la fonction Forms Portal est disponible pour le Cloud Service. Surveillez les notes de mise à jour mensuelles pour connaître la disponibilité des fonctionnalités. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Il n’existe aucun remplacement pour l’accordéon de métadonnées. Supprimez-le de vos formulaires avant de les migrer vers le Cloud Service.(METADATA_ACCORDION_FORM_CONTENEUR)

* Utilisez Google reCaptcha au lieu du service CAPTCHA fourni par Adobe Experience Manager. (FORMS_CAPTCHA)

* Offre Forms adaptative une conception adaptée. Ces formulaires modifient l’aspect, la conception et l’interactivité en fonction du périphérique sous-jacent. Vous pouvez continuer à utiliser Adaptive Forms sur un périphérique mobile tout en surveillant les notes de mise à jour mensuelles concernant la disponibilité de l&#39;application [!DNL AEM Forms]. (AEM_FORMS_APP)

* Ne migrez pas un modèle de flux de travail AEM qui utilise une étape de flux de travail Document Services. En outre, ne migrez pas ou ne mettez pas à jour Adaptive Forms qui envoie des données utilisateur à un modèle de flux de travail qui utilise les étapes de flux de travail de Document Services ou ne modifiez pas l’action Envoyer en une [prise en charge](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html) avant de migrer le formulaire. (WORKFLOW_DOCSERVICES)

* La prise en charge de Forms adaptatif basé sur XFA n’est pas disponible en standard. Si vous envisagez d’utiliser une Forms adaptative basée sur XFA, contactez l’assistance Adobe pour connaître votre cas d’utilisation et les exigences spécifiques.((XFA_BASED_FORM, XDP_BASED_FORM)

Contactez le [Support aux Adobes](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
