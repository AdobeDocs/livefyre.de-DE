---
description: Sie können Livefyre Identity mit LinkedIn verwenden, um Benutzern zu ermöglichen, ihre LinkedIn-Anmeldungen zu verwenden, um mit Apps auf Ihrer Site zu interagieren.
title: LinkedIn-App zur Verwendung mit Livefyre-Identität erstellen
exl-id: e77eca6a-1698-414e-994e-1189f780ada1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# Erstellen einer LinkedIn-App zur Verwendung mit Livefyre-Identität{#create-a-linkedin-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit LinkedIn verwenden, um Benutzern zu ermöglichen, ihre LinkedIn-Anmeldungen zu verwenden, um mit Apps auf Ihrer Site zu interagieren.

Zum Aktivieren der LinkedIn-Anmeldung benötigt Livefyre die folgenden LinkedIn-App-Informationen:

* Consumer key (API-Schlüssel)
* Consumer secret (API-geheimer Schlüssel)

So erstellen Sie eine LinkedIn-App zur Verwendung mit Livefyre Identity:

1. Wechseln Sie zu https://www.linkedin.com/secure/developer und melden Sie sich bei Ihrem LinkedIn-Konto an, um eine neue zu erstellen oder eine vorhandene App zur Verwendung mit Livefyre Identity auszuwählen.
1. Klicken **[!UICONTROL Create Application]**.
1. Füllen Sie das Formular aus, um die Anwendung zu erstellen.
1. Aktivieren Sie unter **[!UICONTROL Default Application Permissions]** die App-Berechtigungen **[!UICONTROL r_basicprofile]** und **[!UICONTROL r_emailaddress]**.
1. Geben Sie **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** als `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre` ein.
1. Speichern Sie die App.
1. Wechseln Sie in **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]** den Umschalter **[!UICONTROL Enable LinkedIn Login]** zu **[!UICONTROL On]**.
1. Geben Sie die LinkedIn Client-ID und den LinkedIn Client Secret ein.
1. Klicken **[!UICONTROL Save Settings]**.

Nach Abschluss des Vorgangs wird auf der Seite mit den App-Details der API der API-Schlüssel (Consumer key) und der API-Geheimhaltungsschlüssel (Consumer secret) für die Verwendung auf der Seite &quot;Integrationseinstellungen&quot;von Studio Liste.
