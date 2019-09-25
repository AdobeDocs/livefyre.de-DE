---
description: Erfahren Sie, wie Sie Livefyre-Token mit der Sprache "C#"generieren.
seo-description: Erfahren Sie, wie Sie Livefyre-Token mit der Sprache "C#"generieren.
seo-title: Erstellen von Livefyre-Token "C#"
solution: Experience Manager
title: Erstellen von Livefyre-Token "C#"
uuid: c5e05625-8550-4b51-9211-134600e20ec7
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Creating Livefyre Tokens C\# {#creating-livefyre-tokens-c}

Erfahren Sie, wie Sie mithilfe der Sprache ``C#`` Livefyre-Token erstellen.

Sie können ältere Dokumentation und Beispielcode nutzen, um Methoden zum Erstellen von Token `C#.NET` zu erstellen.

Um auf die offiziellen Bibliotheken von Livefyre zu verweisen, verwenden Sie die [Java-Bibliothek](https://github.com/Livefyre/livefyre-java-utils) als Ausgangspunkt für `C#` Entwickler.

Sie können auch die [Node.js-Bibliothek](https://github.com/Livefyre/livefyre-nodejs-utils) über die Befehlszeile verwenden, um eigene Referenztokens zu generieren und sich mit der Methodenstruktur vertraut zu machen.

* [Aufrufen des Meta-Tokens für Sammlungen](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Zu Auth-Token springen](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Abhängigkeiten {#section_c15_fnh_xz}

* Sie benötigen das [JWT-Paket](https://www.nuget.org/packages/JWT) in Ihrem Projekt, um die Token zu generieren.
* Codebeispiele auf dieser Seite verwenden das [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/) -Paket.

## CollectionMeta-Token {#section_dzt_4mh_xz}

Das CollectionMeta-Token wird an Livefyre übergeben, wenn Sie Kommentare auf einer Seite einbetten, und stellt unserem System die erforderlichen Metadaten für Ihre neue Sammlung zur Verfügung. Darüber hinaus erstellen Sie eine MD5 `checksum` dieser Daten, die Livefyre prüft, ob sich die Metadaten geändert haben. (z. B. wenn der Titel oder die URL Ihres Artikels bearbeitet wurde).

Dieses Token wird mit Ihrem Konto unterzeichnet, `Site Key`das Ihnen von Ihrem technischen Kundenbetreuer bei Livefyre zur Verfügung gestellt wurde.

Siehe auch:

* Offizielle CollectionMeta-Token-Dokumente
* [Beispielverschmelzung](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Erstellen Sie ein Wörterbuch, das die Metadaten für die Sammlung enthält. Wir werden in diesem Schritt nur einige der erforderlichen Felder hinzufügen, da wir eine Prüfsumme dieses Objekts erstellen möchten, BEVOR wir die articleId hinzufügen.

   ```
       // Site Key provided by Livefyre 
       string siteSecret = "ABCDE1234"; 
   
       var meta = new Dictionary<string, object>() { 
           {"title", "Kings win the Stanley Cup"}, 
           {"url", "https://www.website.com/kings-win-stanley-cup"}, 
           {"tags", "sports, hockey, stanley_cup"}, 
           {"type", "livecomments"} 
       };
   ```

   * **Titel** *erforderlich*:  Der Titel der Sammlung, normalerweise der Titel des Artikels. Die maximale Länge beträgt 255 Zeichen. Unterstützt keine HTML-Entitäten. Bitte kodieren Sie Sonderzeichen mit UTF-8.
   * **url** *erforderlich*:  Die kanonische URL Ihres Artikels. Dies wird von den Funktionen zum Freigeben von Kommentaren und zum Synchronisieren in sozialen Netzwerken und Links zu Ihrem Artikel über das Admin-Dashboard verwendet. Bei lokalen Tests beachten Sie bitte, dass Livefyre "localhost"nicht als Domäne akzeptiert.
   * **Tags** *optional*:  Eine kommagetrennte Liste von Tags, die Sie der Sammlung im Livefyre-Dashboard hinzufügen möchten.   Tags dürfen keine Leerzeichen enthalten. Verwenden Sie Unterstriche, wenn im Admin-Dashboard ein Leerzeichen angezeigt werden soll.
   * **type** *optional*:  Eine Zeichenfolge, die angibt, welche Art von Sammlung erstellt werden soll. Gültige Werte sind:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      Wenn keine Angabe gemacht wird, wird standardmäßig eine LiveComments-Sammlung erstellt.


1. JSON kodiert dieses Wörterbuch und generiert eine md5-Prüfsumme.

   ```
          var metaStr = JsonConvert.SerializeObject(meta); 
       byte[] hash; 
   
       using (var md5 = MD5.Create()) 
       { 
           hash = md5.ComputeHash(Encoding.UTF8.GetBytes(metaStr)); 
       } 
   
       StringBuilder sBuilder = new StringBuilder(); 
   
       // Loop through each byte of the hashed data  
       // and format each one as a hexadecimal string  
       for (int i = 0; i < hash.Length; i++) 
       { 
           sBuilder.Append(hash[i].ToString("x2")); 
       } 
   ```

1. Fügen Sie die **articleId** zum Wörterbuch hinzu. Die **Prüfsumme** wird nicht in das collectionMeta-Token übernommen, sollte jedoch als separater Parameter im convConfig-js-Objekt gesendet werden.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **articleId** *erforderlich*:  Eine eindeutige Kennung für Ihre Sammlung auf Ihrer Livefyre-Site. Normalerweise wird die eindeutige articleId in Ihrem CMS verwendet. (z.B. Ihre WordPress-Post-ID) Dieser Wert sollte sich nicht ändern. Livefyre identifiziert eindeutige Sammlungen durch die Kombination von siteId und articleId.

1. Erstellen Sie ein signiertes JWT-Token des Wörterbuchs mithilfe des Site-Schlüssels, den Sie von Livefyre erhalten haben. Bitte beachten Sie, dass Sie den richtigen Hash-Algorithmus angeben müssen, da das JWT-Paket standardmäßig nicht HS256 verwendet.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## Auth-Token des Benutzers {#section_g1d_43h_xz}

Das Auth-Token des Benutzers wird verwendet, um einen Benutzer bei Livefyre zu signieren. Wenn sich ein Benutzer bei Ihrer Site anmeldet, generiert die Site ein Benutzerauthentifizierungstoken, das an das Livefyre-Widget auf der Seite weitergeleitet wird. (Weitere Informationen zum Authentifizierungsprozess finden Sie unter Remote-Profile.)

Dieses Token erfordert Ihren Netzwerknamen (network.fyre.co) und ist mit Ihrem Netzwerkschlüssel signiert, der Ihnen von Ihrem technischen Kundenbetreuer bei Livefyre zur Verfügung gestellt wird.

Siehe auch:

* Offizielle Auth-Token-Dokumente
* [Beispielverschmelzung](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. Erstellen Sie ein Wörterbuch mit den erforderlichen Informationen.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **** domain: Der Name Ihres Netzwerks (bereitgestellt von Livefyre) z. B. mynetwork.fyre.co
   * **** user_id: Die eindeutige Benutzer-ID für den Benutzer im Profilsystem Ihrer Site. Muss nur alphanumerische Zeichen sein (A-Z, a-z, 0-9). Wenn die Benutzer-ID Ihres Systems ungültige Zeichen enthält, senden Sie Livefyre einen md5-Hash der Benutzer-ID oder eine Base64-kodierte Version davon. (Teilen Sie Ihrem Kundenbetreuer mit, wenn Sie dies tun.)
   * **** läuft ab: Das Datum (in Epochenzeit), an dem das Token abläuft. Dies sollte mit der Sitzungszeit der Anmeldungen auf Ihrer Site übereinstimmen, damit der Anmeldestatus von Livefyre mit dem Anmeldestatus Ihrer Site synchronisiert bleibt.
   * **** display_name: Der Anzeigename des Benutzers in Ihrem Profilsystem, wie er im Kommentarstream angezeigt werden soll.

1. Erstellen Sie ein signiertes JWT-Token des Wörterbuchs mithilfe des Netzwerkschlüssels, den Sie von Livefyre erhalten haben. Bitte beachten Sie, dass Sie den richtigen Hash-Algorithmus angeben müssen, da das JWT-Paket standardmäßig nicht HS256 verwendet.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
