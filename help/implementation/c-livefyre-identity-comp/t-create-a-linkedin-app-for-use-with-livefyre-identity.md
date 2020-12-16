---
description: Sie können Livefyre Identity mit LinkedIn verwenden, um Benutzern zu ermöglichen, ihre LinkedIn-Anmeldungen zu verwenden, um Apps auf Ihrer Site zu interagieren.
seo-description: Sie können Livefyre Identity mit LinkedIn verwenden, um Benutzern zu ermöglichen, ihre LinkedIn-Anmeldungen zu verwenden, um Apps auf Ihrer Site zu interagieren.
seo-title: Erstellen einer LinkedIn-App zur Verwendung mit Livefyre-Identität
solution: Experience Manager
title: Erstellen einer LinkedIn-App zur Verwendung mit Livefyre-Identität
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Erstellen einer LinkedIn-App zur Verwendung mit Livefyre-Identität{#create-a-linkedin-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit LinkedIn verwenden, um Benutzern zu ermöglichen, ihre LinkedIn-Anmeldungen zu verwenden, um Apps auf Ihrer Site zu interagieren.

Zum Aktivieren der LinkedIn-Anmeldung erfordert Livefyre die folgenden LinkedIn-App-Informationen:

* Consumer key (API-Schlüssel)
* Consumer secret (API-geheimer Schlüssel)

So erstellen Sie eine LinkedIn-App zur Verwendung mit Livefyre-Identität:

1. Wechseln Sie zu https://www.linkedin.com/secure/developer und melden Sie sich bei Ihrem LinkedIn-Konto an, um eine neue zu erstellen oder eine vorhandene App zur Verwendung mit Livefyre Identity auszuwählen.
1. Klicken **[!UICONTROL Create Application]**.
1. Füllen Sie das Formular aus, um die Anwendung zu erstellen.
1. Aktivieren Sie unter **[!UICONTROL Default Application Permissions]** die App-Berechtigungen **[!UICONTROL r_basicprofile]** und **[!UICONTROL r_emailaddress]**.
1. Geben Sie **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** als `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre` ein.
1. Speichern Sie die App.
1. Wechseln Sie in **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]** den Umschalter **[!UICONTROL Enable LinkedIn Login]** zu **[!UICONTROL On]**.
1. Geben Sie die LinkedIn-Client-ID und den geheimen LinkedIn-Clientschlüssel ein.
1. Klicken **[!UICONTROL Save Settings]**.

Nach Abschluss des Vorgangs wird auf der Seite mit den App-Details der App der API-Schlüssel (Consumer key) und der API-Geheimhaltungsschlüssel (Consumer secret) für die Verwendung auf der Seite &quot;Integrationseinstellungen&quot;von Studio Liste.
