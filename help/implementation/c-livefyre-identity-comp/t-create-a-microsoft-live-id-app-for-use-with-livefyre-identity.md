---
description: Sie können Livefyre Identity mit Microsoft Live Identity verwenden, um Benutzern zu ermöglichen, ihre Facebook-Anmeldungen zu verwenden, um Apps auf Ihrer Site zu interagieren.
seo-description: Sie können Livefyre Identity mit Microsoft Live Identity verwenden, um Benutzern zu ermöglichen, ihre Facebook-Anmeldungen zu verwenden, um Apps auf Ihrer Site zu interagieren.
seo-title: Erstellen einer Microsoft Live-Identitäts-App zur Verwendung mit Livefyre-Identität
solution: Experience Manager
title: Erstellen einer Microsoft Live-Identitäts-App zur Verwendung mit Livefyre-Identität
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# Erstellen einer Microsoft Live-Identitätsanwendung zur Verwendung mit Livefyre-Identität{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit Microsoft Live Identity verwenden, um Benutzern zu ermöglichen, ihre Facebook-Anmeldungen zu verwenden, um Apps auf Ihrer Site zu interagieren.

Damit Benutzer sich mit ihren Microsoft Live-Identitätsberechtigungen anmelden können, benötigt Livefyre die folgenden Microsoft Live-Identitätsinformationen:

* Client-ID (privater Schlüssel)
* geheimer Clientschlüssel (Kennwort)

So erstellen Sie eine Microsoft Live Identity-App zur Verwendung mit Livefyre Identity:

1. Erstellen oder melden Sie sich bei einem Microsoft Live-Konto unter [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/) an
1. Erstellen Sie eine neue oder wählen Sie eine vorhandene App zur Verwendung mit Livefyre Identity aus.
1. Klicken Sie auf **[!UICONTROL Add Platform]** und wählen Sie dann Web als Plattformtyp aus.
1. Vergewissern Sie sich, dass die Option **[!UICONTROL Allow Implicit Flow]** aktiviert ist, und geben Sie die Umleitungs-URL unter Verwendung Ihres Netzwerknamens anstelle von {network-name} ein: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Erstellen Sie ein neues Kennwort-/Schlüsselpaar, um den privaten Schlüssel abzurufen.
1. Wechseln Sie in **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]** den Umschalter **[!UICONTROL Enable Microsoft Live Login]** zu **[!UICONTROL On]**.
1. Geben Sie die Microsoft Live Client-ID und den geheimen Microsoft Live Client ein.
1. Klicken **[!UICONTROL Save Settings]**.

Nach Abschluss des Vorgangs wird auf der Seite mit den App-Details von Microsoft Live Identity die Client-ID (Consumer key) und der geheime Clientschlüssel (Consumer secret) der App zur Verwendung auf der Seite &quot;Integrationseinstellungen&quot;von Studio Liste.
