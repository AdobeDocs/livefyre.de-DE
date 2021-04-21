---
description: Erstellen Sie den Pull-Endpunkt, um Anfragen nach Zugriff auf Ihr Benutzeridentitätssystem zu empfangen und zu beantworten.
title: Pull-Endpunkt erstellen
exl-id: cc66365b-0d5f-4a0b-954f-ee014e75d4a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# Pull-Endpunkt{#build-the-pull-endpoint} erstellen

Erstellen Sie den Pull-Endpunkt, um Anfragen nach Zugriff auf Ihr Benutzeridentitätssystem zu empfangen und zu beantworten.

1. Erstellen Sie einen HTTPS-Endpunkt, der Livefyre-Anforderungen empfängt und mit einem JSON-Objekt antwortet, das die neuesten Benutzerdaten enthält.

   >[!NOTE]
   >
   >Auf diesen Endpunkt muss zugegriffen werden können. Es wird außerdem dringend empfohlen, sowohl Anforderungen als auch Antworten über das HTTPS-Protokoll zu senden.

1. Registrieren Sie den Endpunkt mit Studio.
