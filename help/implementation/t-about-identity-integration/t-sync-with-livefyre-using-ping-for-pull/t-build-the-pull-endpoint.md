---
description: Erstellen Sie den Pull-Endpunkt, um die Anforderungen für den Zugriff
  auf Ihr Benutzeridentitätssystem zu erhalten und zu beantworten.
seo-description: Erstellen Sie den Pull-Endpunkt, um die Anforderungen für den Zugriff
  auf Ihr Benutzeridentitätssystem zu erhalten und zu beantworten.
seo-title: Erstellen des Pull-Endpunkts
solution: Experience Manager
title: Erstellen des Pull-Endpunkts
uuid: 1703152 f-aaa 7-4 a 88-aa 33-d 9 f 8957 ad 42 b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Erstellen des Pull-Endpunkts{#build-the-pull-endpoint}

Erstellen Sie den Pull-Endpunkt, um die Anforderungen für den Zugriff auf Ihr Benutzeridentitätssystem zu erhalten und zu beantworten.

1. Erstellen Sie einen HTTPS-Endpunkt, der Livefyre-Anforderungen empfängt und mit einem JSON-Objekt antwortet, das die neuesten Benutzerdaten enthält.

   >[!NOTE]
   >
   >Dieser Endpunkt muss verfügbar sein. Es wird außerdem dringend empfohlen, sowohl Anforderungen als auch Antworten über das HTTPS-Protokoll zu senden.

1. Registrieren Sie den Endpunkt mit Studio.
