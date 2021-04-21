---
description: Sie können Livefyre Identity mit Yahoo! , damit Benutzer ihre Yahoo! sich anmelden, um mit Apps auf Ihrer Site zu interagieren.
title: Erstellen Sie ein Yahoo! App für die Verwendung mit Livefyre-Identität
exl-id: 6b4c6ea9-1cb0-4496-aabe-70811f464a3d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Erstellen Sie ein Yahoo! App zur Verwendung mit Livefyre-Identität{#create-a-yahoo-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit Yahoo! , damit Benutzer ihre Yahoo! sich anmelden, um mit Apps auf Ihrer Site zu interagieren.

Damit sich Ihre Benutzer mit ihren Yahoo-Anmeldedaten anmelden können, benötigt Livefyre die folgenden Yahoo-App-Informationen:

* Client-ID (Consumer key)
* geheimer Clientschlüssel (Consumer secret)

So erstellen Sie ein Yahoo! App zur Verwendung mit Livefyre Identity:

1. Gehen Sie zu [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/) und melden Sie sich bei Ihrem Yahoo! , um eine neue App zu erstellen oder eine vorhandene App zur Verwendung mit Livefyre Identity auszuwählen.
1. Auswählen **[!UICONTROL Application Type: Web Application]**.
1. Eingabetaste **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. Wählen Sie **[!UICONTROL API Permissions: Profiles (Social Directory)]** und **[!UICONTROL Read Public]**.

   Nach Abschluss des Vorgangs wird auf der Seite mit den App-Details die Client-ID (Consumer key) und der geheime Clientschlüssel (Consumer secret) der App für die Verwendung auf der Seite &quot;Integrationseinstellungen&quot;von Studio Liste.

   >[!NOTE]
   >
   >Wenn Sie Yahoo! anmelden, ohne Yahoo zu erstellen! und wenn Sie die Felder Client-ID und geheimer Clientschlüssel in Studio leer lassen, verwendet Livefyre OpenID, um diese Benutzer in Ihren Livefyre-Apps anzumelden. OAuth und benutzerdefinierte Branding sind in diesem Fall nicht verfügbar.
