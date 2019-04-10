---
description: Erfahren Sie, wie Sie mithilfe der Sprache "C
seo-description: Erfahren Sie, wie Sie mithilfe der Sprache "C
seo-title: Erstellen von Livefyre Tokens'C
solution: Experience Manager
title: Erstellen von Livefyre Tokens'C
uuid: c 5 e 05625-8550-4 b 51-9211-134600 e 20 ec 7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Erstellen von Livefyre Tokens C\ # {#creating-livefyre-tokens-c}

Erfahren Sie, wie Sie mithilfe der Sprache ``C#`` Livefyre-Token erstellen.

Sie können ältere Dokumentation und Beispielcode nutzen, um Methoden `C#.NET` zum Erstellen von Token zu verwenden.

Verwenden Sie die [Java-Bibliothek](https://github.com/Livefyre/livefyre-java-utils) als Ausgangspunkt für `C#` Entwickler, um die offiziellen Bibliotheken von Livefyre zu referenzieren.

Sie können auch erwägen, die [Node. js-Bibliothek](https://github.com/Livefyre/livefyre-nodejs-utils) aus der Befehlszeile zu verwenden, um Referenztoken für sich zu generieren und sich mit der Methodenstruktur vertraut zu machen.

* [Aufrufen des Sammlungs-Meta-Token](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Aufrufen des Authentifizierungstokens](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Abhängigkeiten {#section_c15_fnh_xz}

* Sie benötigen das [JWT-Nuget-Paket](https://www.nuget.org/packages/JWT) in Ihrem Projekt, um die Token zu generieren.
* Codebeispiele auf dieser Seite verwenden das [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/) -Paket.

## Collectionmeta Token {#section_dzt_4mh_xz}

Das collectionmeta Token wird an Livefyre übergeben, wenn Sie Kommentare auf einer Seite einbetten und unser System die erforderlichen Metadaten für die neue Sammlung bereitstellen. Darüber hinaus erstellen Sie eine MD 5 `checksum` dieser Daten, die Livefyre überprüft, um zu prüfen, ob sich die Metadaten geändert haben. (z. B. wenn der Titel oder die URL des Artikels bearbeitet wurde).

Dieses Token wird mit Ihrem `Site Key`Token signiert, das Ihnen von Ihrem technischen Kundenbetreuer bei Livefyre bereitgestellt wurde.

Siehe auch:

* Offizielle collectionmeta Token Docs
* [Beispielgist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Erstellen Sie ein Wörterbuch mit den Metadaten für die Sammlung. Wir werden in diesem Schritt nur einige der erforderlichen Felder hinzufügen. Behease wir möchten eine Prüfsumme dieses Objekts erstellen, BEVOR wir die articleid hinzufügen.

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

   * **Titel** *erforderlich*: Der Titel der Sammlung, normalerweise der Titel des Artikels. Die maximale Länge beträgt 255 Zeichen. Unterstützt keine HTML-Entitäten. Bitte Sonderzeichen mit UTF -8 kodieren.
   * **URL** *erforderlich*: Die kanonische URL Ihres Artikels. Dies wird von den Funktionen für Kommentare und Social-Synchronisierung sowie von Links zu Ihrem Artikel vom Admin-Dashboard verwendet. Wenn Sie lokal testen, beachten Sie, dass Livefyre "localhost" nicht als Domäne akzeptiert.
   * **Tags** *optional*: Eine kommagetrennte Liste von Tags, die Sie der Sammlung im Livefyre-Dashboard hinzufügen möchten. Tags dürfen keine Leerzeichen enthalten. Verwenden Sie Unterstriche, wenn im Admin-Dashboard ein Leerzeichen angezeigt werden soll.
   * **type** *optional*: Eine Zeichenfolge, die angibt, welche Art von Sammlung erstellt werden soll. Gültige Werte sind:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      Falls nicht angegeben, wird eine livecomments-Sammlung standardmäßig erstellt.


1. JSON kodiert dieses Wörterbuch und generiert eine md 5-Prüfsumme.

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

1. Fügen Sie die **articleid** dem Wörterbuch hinzu. Die **Prüfsumme** wird nicht in das collectionmeta-Token aufgenommen, sollte aber als Seapratenparameter im contconfig js-Objekt gesendet werden.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **Articleid** *erforderlich*: Ein eindeutiger Identifikator für Ihre Sammlung auf Ihrer Livefyre-Site. Normalerweise wird der eindeutige articleid in Ihrem CMS verwendet. (z. B. Ihre wordpress-Post-ID) Dieser Wert sollte sich nie ändern. Livefyre identifiziert eindeutige Sammlungen anhand der Kombination aus siteid und articleid.

1. Generieren Sie ein signiertes JWT-Token des Wörterbuchs mit dem Site-Schlüssel, der Ihnen von Livefyre bereitgestellt wird. Bitte beachten Sie, dass Sie den richtigen Hash-Algorithmus angeben müssen, da das JWT-Paket standardmäßig HS 256 nicht verwendet.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## Das Benutzerauthentifizierungstoken {#section_g1d_43h_xz}

Das Benutzerauthentifizierungstoken wird verwendet, um einen Benutzer in Livefyre zu signieren. Wenn sich ein Benutzer bei Ihrer Site anmeldet, generiert die Site ein Benutzerauthentifizierungstoken, das auf der Seite an das Livefyre-Widget übergeben wird. (Weitere Informationen zum Authentifizierungsprozess finden Sie unter Remote Profile.)

Für dieses Token ist Ihr Netzwerkname (network. fyre. co) erforderlich und mit Ihrem Netzwerkschlüssel signiert, der Ihnen von Ihrem Technical Account Manager bei Livefyre bereitgestellt wird.

Siehe auch:

* Offizielle Authentifizierungs-Token
* [Beispielgist](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

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

   * **Domäne:** Der Name Ihres Netzwerks (von Livefyre bereitgestellt). z. B. mynetwork. fyre. co
   * **user_ id:** Die eindeutige Benutzer-ID für den Benutzer im Profilsystem Ihrer Site. Muss nur alphanumerische Zeichen sein (A-Z, a-z, 0-9). Wenn die Benutzer-ids Ihrer Systeme ungültige Charaacters enthalten, sollten Sie Livefyre an einen md 5-Hash der Benutzer-ID oder eine base 64-kodierte Version davon senden. (Lassen Sie Ihren Kundenbetreuer wissen, ob Sie dies tun.)
   * **läuft ab:** Das Datum (in der Epoche), ab dem das Token abläuft. Dies sollte mit der Sitzungszeit der Anmeldungen auf Ihrer Site übereinstimmen, sodass der angemeldete Status von Livefyre synchronisiert mit dem angemeldeten Status Ihrer Site bleibt.
   * **display_ name:** Der Anzeigename des Benutzers in Ihrem Profilsystem, wie er im Kommentarstream angezeigt werden soll.

1. Generieren Sie ein signiertes JWT-Token des Wörterbuchs mit dem Netzwerkschlüssel, den Livefyre Ihnen bereitstellt. Bitte beachten Sie, dass Sie den richtigen Hash-Algorithmus angeben müssen, da das JWT-Paket standardmäßig HS 256 nicht verwendet.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
