---
description: Erstellen Sie den Pull-Endpunkt, um Anfragen nach Zugriff auf Ihr Benutzeridentitätssystem zu empfangen und zu beantworten.
seo-description: Erstellen Sie den Pull-Endpunkt, um Anfragen nach Zugriff auf Ihr Benutzeridentitätssystem zu empfangen und zu beantworten.
seo-title: Pull-Endpunkt erstellen
solution: Experience Manager
title: Pull-Endpunkt erstellen
uuid: 1703152f-aaa7-4a88-aa33-d9f8957ad42b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Pull-Endpunkt{#build-the-pull-endpoint} erstellen

Erstellen Sie den Pull-Endpunkt, um Anfragen nach Zugriff auf Ihr Benutzeridentitätssystem zu empfangen und zu beantworten.

1. Erstellen Sie einen HTTPS-Endpunkt, der Livefyre-Anforderungen empfängt und mit einem JSON-Objekt antwortet, das die neuesten Benutzerdaten enthält.

   >[!NOTE]
   >
   >Auf diesen Endpunkt muss zugegriffen werden können. Es wird außerdem dringend empfohlen, sowohl Anforderungen als auch Antworten über das HTTPS-Protokoll zu senden.

1. Registrieren Sie den Endpunkt mit Studio.
