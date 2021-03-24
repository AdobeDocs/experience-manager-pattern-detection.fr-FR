---
title: Forms
description: Page d’aide du code du détecteur de schémas
translation-type: tm+mt
source-git-commit: a6ba6e93c89644160650882ecbf17028bec35068
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---


# [!DNL FORMS] {#forms}

[!DNL Adobe Experience Manager Forms]

## Arrière-plan {#background}

`FORMS` identifie les problèmes potentiels liés à la migration d’Adobe Experience Manager Forms vers Adobe Experience Manager Forms en tant que Cloud Service. Résolvez ces problèmes avant de migrer vers le Cloud Service.

Les sous-types suivants vous aident à identifier les différents types de problèmes :

* `modified.feature`: Ces fonctionnalités, ressources ou API ont été mises à jour ou modifiées pour le Cloud Service. Avant de migrer vers le Cloud Service, exécutez l’utilitaire de migration pour rendre ces fonctions et ressources compatibles avec le Cloud Service.
* `unavailable.feature`: Votre environnement comporte des fonctions et des ressources qui ne sont pas disponibles ou supprimées du Cloud Service. Ne migrez pas ces fonctions ou ressources vers un environnement Cloud Service.
* `unsupported.feature`: Votre environnement utilise certaines fonctionnalités qui ne sont pas encore prises en charge sur le Cloud Service. Ne migrez pas ces fonctions ou ressources vers un environnement Cloud Service. Surveillez les notes de mise à jour mensuelles pour connaître la disponibilité des fonctionnalités.
* `unsupported.api`: Votre environnement comporte des API qui ne sont pas encore prises en charge par le Cloud Service. Avant de migrer vers le Cloud Service, désactivez, remplacez ou supprimez ces API de votre code. Surveillez les notes de mise à jour mensuelles pour connaître la disponibilité des fonctionnalités.

Pour plus d&#39;informations sur les remplacements et autres actions nécessaires pour rendre certaines fonctions et API compatibles avec le Cloud Service, consultez les sections [Enjeux et risques possibles](#implications-and-risks) et [Solutions possibles](#solutions).

## Incidences possibles et risques {#implications-and-risks}

Résolvez les problèmes suivants avant de migrer en tant que Cloud Service vers Adobe Experience Manager Forms. Lorsque les implications et les risques énumérés ci-dessous ne sont pas pris en compte, certaines caractéristiques ne fonctionnent pas comme prévu dans l&#39;environnement Cloud Service.

* La fonctionnalité d&#39;éditeur de code de la fonction d&#39;éditeur de règles n&#39;est pas disponible. (CODE_EDITOR)

* Par défaut, la prise en charge du courrier électronique (port SMTP) est désactivée. (EMAIL_SERVICE_CONFIGURATION)

* L’action d’envoi **[!UICONTROL Envoyer le PDF par courrier électronique]** n’est pas disponible.(EMAIL_PDF_SUBMIT_ACTION)

* Les formulaires adaptatifs basés sur XDP ne sont pas encore pris en charge. (XDP_BASED_FORM)

* Une action d’envoi est appelée immédiatement lors de l’envoi du formulaire au lieu d’attendre que tous les signataires terminent la signature. Par conséquent, le document de signature du formulaire adaptatif (PDF de l’accord de Adobe Sign envoyé aux signataires) n’est pas disponible pour les actions d’envoi à utiliser ou à traiter. (FORM_SIGN_INTEGRATION)

* L&#39;étape Signature n&#39;est pas disponible. (SIGNATURE_STEP)

* L&#39;étape Vérifier n&#39;est pas disponible. (VERIFY_STEP)

* La fonction de portail Forms et l&#39;**[!UICONTROL action d&#39;envoi du portail Forms]** ne sont pas disponibles. Vous ne pouvez pas utiliser Forms Portal pour liste de formulaires, enregistrer des brouillons ou afficher des formulaires envoyés. Vous ne pouvez pas envoyer (utiliser **[!UICONTROL l’action d’envoi du portail Forms]**) de données envoyées à un formulaire adaptatif à un portail Forms. [!UICONTROL Les fonctions Enregistrer en tant que ] brouillon et   Enregistrement automatique des formulaires adaptatifs ne sont pas prises en charge pour le moment. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* L&#39;action d&#39;envoi **[!UICONTROL Processus Envoyer à Forms]** n&#39;est pas disponible. Dans AEM version 6.5 de Forms et les versions précédentes, l’action d’envoi a été utilisée pour envoyer des données de formulaire adaptatif aux Workflows et LiveCycles Workflow hérités de AEM Forms on JEE. (LC_WORKFLOW_SUBMISSION)

* La fonctionnalité de communications interactives n&#39;est pas disponible.  (FP_PROFIL_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL Les fonctions Enregistrer en tant que]** brouillon et  **** Enregistrement automatique des formulaires adaptatifs ne sont pas prises en charge pour le moment. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* L’accordéon de métadonnées n’est pas disponible. (METADATA_ACCORDION_FORM_CONTENEUR)

* Le composant CAPTCHA utilise maintenant le service Google reCAPTCHA pour valider CAPTCHA, par défaut. L&#39;option permettant d&#39;utiliser Adobe Experience Manager pour valider CAPTCHA n&#39;est pas disponible. (FORMS_CAPTCHA)

## Solutions possibles {#solutions}

* Utilisez l’utilitaire de migration pour convertir tous les scripts de règle de votre environnement en fonctions réutilisables. Vous pouvez utiliser les fonctions réutilisables avec l’éditeur de règles visuelles pour continuer à obtenir les résultats obtenus avec les scripts de règles. (CODE_EDITOR)

* Contactez l’équipe d’assistance pour activer la fonctionnalité de courrier électronique (ouvrez le port SMTP) pour votre environnement. Par défaut, seules les connexions HTTP et HTTPS sortantes sont activées. (EMAIL_SERVICE_CONFIGURATION)

* Utilisez l’action d’envoi **[!UICONTROL Courriel]** au lieu de **[!UICONTROL Envoyer le PDF]** par courriel. L&#39;action d&#39;envoi **[!UICONTROL Courrier électronique]** fournit des options pour envoyer des pièces jointes et joindre un Document d&#39;enregistrement (DE) par courrier électronique. (EMAIL_PDF_SUBMIT_ACTION)

* Ne migrez pas les formulaires adaptatifs basés sur XDP vers un environnement Cloud Service. Surveillez les notes de mise à jour mensuelles pour connaître la disponibilité des fonctionnalités. (XDP_BASED_FORM)

* Les données envoyées contiennent l’identifiant d’accord de signature. Si nécessaire, vous pouvez utiliser l’ID d’accord de signature pour récupérer un PDF d’accord de signature.  (FORM_SIGN_INTEGRATION)

* Remplacez l’étape Signature de vos formulaires adaptatifs par l’option Signature d’un formulaire adaptatif après envoi, dans la même fenêtre. Il vous permet de continuer à fournir une [expérience de signature dans le navigateur](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). (SIGNATURE_STEP)

* Supprimez l’étape de vérification de vos formulaires adaptatifs existants avant de déplacer ces formulaires vers un environnement Cloud Service. (VERIFY_STEP)

* Il n’existe aucune alternative à l’**[!UICONTROL action d’envoi du portail Forms]**. Vous pouvez utiliser cette action d’envoi une fois que la fonction Forms Portal est disponible pour le Cloud Service. Surveillez les notes de mise à jour mensuelles pour connaître la disponibilité des fonctionnalités. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL)

* Il n’existe pas d’autre action d’envoi pour les actions d’envoi **[!UICONTROL Envoyer à Forms workflow]**. Vous pouvez développer une action d’envoi personnalisée pour envoyer des données, des pièces jointes ou un Document d’enregistrement (DE) à un processus de LiveCycle. (LC_WORKFLOW_SUBMISSION)

* Ne migrez pas vos communications interactives, lettres et dictionnaires associés vers un environnement Cloud Service. (FP_PROFIL_INTERACTIVE_COMMUNICATIONS)

* Désactivez l’option **[!UICONTROL Enregistrer en tant que brouillon]** et **[!UICONTROL Activer l’enregistrement automatique]** dans vos formulaires adaptatifs avant de les migrer vers le Cloud Service. Vous pouvez activer ces options une fois que la fonction Forms Portal est disponible pour le Cloud Service. Surveillez les notes de mise à jour mensuelles pour connaître la disponibilité des fonctionnalités. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Il n’existe aucun remplacement pour l’accordéon de métadonnées. Supprimez-le de vos formulaires avant de les migrer vers le Cloud Service.(METADATA_ACCORDION_FORM_CONTENEUR)

* Utilisez Google reCaptcha au lieu du service CAPTCHA fourni par Adobe Experience Manager. (FORMS_CAPTCHA)

Contactez le [Support aux Adobes](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) pour obtenir des éclaircissements ou pour répondre aux préoccupations.
