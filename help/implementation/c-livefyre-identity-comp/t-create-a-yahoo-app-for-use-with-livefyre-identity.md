---
description: Sie können die Livefyre-Identität mit Yahoo! So können Benutzer ihr Yahoo! für die Interaktion mit Apps auf Ihrer Site.
seo-description: Sie können die Livefyre-Identität mit Yahoo! So können Benutzer ihr Yahoo! für die Interaktion mit Apps auf Ihrer Site.
seo-title: Erstellen Sie ein Yahoo! App für die Verwendung mit Livefyre-Identität
solution: Experience Manager
title: Erstellen Sie ein Yahoo! App für die Verwendung mit Livefyre-Identität
uuid: 6863 cd 2 e-eb 0 d -465 b-b 706-88 ecaccf 41 bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Erstellen Sie ein Yahoo! App für die Verwendung mit Livefyre-Identität{#create-a-yahoo-app-for-use-with-livefyre-identity}

Sie können die Livefyre-Identität mit Yahoo! So können Benutzer ihr Yahoo! für die Interaktion mit Apps auf Ihrer Site.

Damit Ihre Benutzer sich mit ihren Yahoo-Anmeldeinformationen anmelden können, erfordert Livefyre die folgenden Yahoo App-Informationen:

* Client-ID (Consumer-Schlüssel)
* Geheimer Clientschlüssel (geheimer Verbraucher)

So erstellen Sie ein Yahoo! App für die Verwendung mit Livefyre-Identität:

1. Rufen Sie [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)auf und melden Sie sich bei Yahoo! an! , um eine neue zu erstellen oder eine vorhandene App für die Verwendung mit Livefyre-Identität auszuwählen.
1. Wählen **[!UICONTROL Application Type: Web Application]** Sie.
1. Eingeben **[!UICONTROL Callback Domain:]**`https://identity.livefyre.com`
1. Wählen **[!UICONTROL API Permissions: Profiles (Social Directory)]** Sie und **[!UICONTROL Read Public]**.

   Wenn Sie fertig sind, listet die App-Detailseite von Yahoo die Client-ID (Consumer-ID) der App und den geheimen Clientschlüssel (Consumer-Secret) für die Verwendung auf der Seite Integration von Studio auf.

   >[!NOTE]
   >
   >Wenn Sie Yahoo! aktivieren Anmelden ohne Yahoo! App und wenn Sie die Felder Client-ID und geheimer Clientschlüssel in Studio leer lassen, verwendet Livefyre openid, um diese Benutzer in Ihren Livefyre-Apps zu protokollieren. In diesem Fall sind oauth und benutzerdefiniertes Branding nicht verfügbar.