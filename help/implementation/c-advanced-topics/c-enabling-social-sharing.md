---
description: Richten Sie Anmeldeinformationen ein, mit denen Ihre Benutzer Inhalte für verschiedene soziale Netzwerke freigeben können.
seo-description: Richten Sie Anmeldeinformationen ein, mit denen Ihre Benutzer Inhalte für verschiedene soziale Netzwerke freigeben können.
seo-title: Social Sharing aktivieren
solution: Experience Manager
title: Social Sharing aktivieren
uuid: f584a0ae-46c7-48c1-aea4-36da9f1e259b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---


# Aktivieren von Social Sharing {#enabling-social-sharing}

Richten Sie Anmeldeinformationen ein, mit denen Ihre Benutzer Inhalte für verschiedene soziale Netzwerke freigeben können.

Um Benutzern die Freigabe von Inhalten über Social-Media-Sites zu ermöglichen, implementieren Sie Livefyres Social Sharing-Funktion und erstellen Sie ein OAuth-System, um eine ordnungsgemäße Authentifizierung für diese Sites zu gewährleisten. Mit diesem System agiert Livefyre im Namen des Benutzers, wenn er sich dafür entscheidet, Inhalte über soziale Medien zu teilen.

>[!NOTE]
>
>Verschiedene Anbieter haben unterschiedliche OAuth-Anforderungen. Bitte fragen Sie bei Ihren Anbietern nach, welche Informationen zu deren Implementierung von OAuth gehören.

## Erforderliche Social-Anmeldeinformationen {#section_gff_cjm_b1b}

Wenn Sie ein benutzerdefiniertes Benutzeridentitätssystem verwenden, müssen Sie Ihre sozialen Anmeldeinformationen angeben, damit Benutzer über eine Livefyre-App auf Twitter, Facebook oder LinkedIn zugreifen können.

>[!NOTE]
>
>Kunden, die Janrain Engage verwenden, müssen nur ihren Engage Domain- und Engage API Key angeben.

Verwenden Sie das Bedienfeld &quot;Integrationseinstellungen&quot;der Admin Console, um die folgenden Social-Anmeldedaten einzugeben oder zu aktualisieren.

### Erforderliche Berechtigungen:

* **** FacebookClient-ID-Client Geheimer OAuth-Proxy-Umleitung
* **API-Geheimnis** für LinkedInAPI-Schlüssel
* **API-Schlüssel für** TwitterAccess-Token-Zugriffstoken-Geheimnis

## Twitter {#section_qp5_1yl_b1b}

Twitter-Anmeldeinformationen sind im Twitter App-Dashboard verfügbar. So suchen Sie diese Berechtigungen:

* Öffnen Sie [Twitters App Dev Page](https://dev.twitter.com/apps) als App-Inhaber, suchen Sie Ihre Anwendung und klicken Sie auf den Titel.
* Blättern Sie nach unten zu &quot;Ihr Zugriffstoken&quot;und ziehen Sie die Werte aus &quot;Zugriffstoken&quot;und &quot;Zugriffstoken-Geheimnis&quot;ab.

Sie müssen:

* Geben Sie in der Twitter-App einen Wert für das Feld &quot;Rückruf-URL&quot;ein. Dieses Feld kann ein einfacher Platzhalter sein, darf jedoch nicht leer gelassen werden.
* Stellen Sie den Anwendungstyp so ein, dass sowohl **read** als auch **write** Zugriff haben.
* Vergewissern Sie sich, dass sich die URL der Twitter-App-Website in derselben Hostdomäne wie die Livefyre-Core-App befindet.

>[!NOTE]
>
>Alle Anwendungen, die Twitter-Inhalte anzeigen, müssen ihre Anzeigeanforderungen erfüllen. Weitere Informationen finden Sie unter [Twitter-Anzeigenrichtlinien](https://dev.twitter.com/terms/display-requirements).

## LinkedIn {#section_lfz_zxl_b1b}

LinkedIn-Anmeldedaten sind im Abschnitt &quot;OAuth-Schlüssel&quot;der API-Schlüssel der LinkedIn-Anwendung verfügbar.

* Melden Sie sich über die Seite für Entwickler von LinkedIn unter [https://developer.linkedin.com/](https://developer.linkedin.com/) bei Ihrem Konto an.
* Bewegen Sie den Mauszeiger über Ihren Namen oben rechts und wählen Sie im Dropdown-Menü die Option &quot;API-Schlüssel&quot;.
* Klicken Sie auf den Titel der Anwendung.
* Werte für den API-Schlüssel und geheime Schlüssel aus dem Abschnitt &quot;OAuth-Schlüssel&quot;abrufen

## Facebook {#section_zyb_gpl_b1b}

Facebook-Anmeldeinformationen stehen auf Ihrer Seite &quot;Developer Apps&quot;zur Verfügung.

* Öffnen Sie die Developer Apps-Seite von Facebook [als App-Inhaber, suchen Sie die Anwendung und klicken Sie auf den Titel.](https://developers.facebook.com/apps)
* Erfassen Sie die Werte für App-ID und App-geheim. Für den geheimen App-Schlüssel müssen Sie möglicherweise auf die Schaltfläche &quot;Anzeigen&quot;klicken, um ihn anzuzeigen.

Für die Freigabe auf Facebook müssen Sie eine Umleitungsseite einrichten, um Facebook-Anforderungen zu erfüllen und die Domänenpraktiken einzuhalten, die für [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/) erforderlich sind. Die Seite muss in Ihrer Domäne gehostet werden, damit Facebook überprüfen kann, ob die Anforderung von einer legitimen Quelle stammt.

### Facebook-Umleitung

Die gehostete Seite sollte den folgenden Code enthalten:

### Ruby

Dies ist ein Beispiel für die Verwendung von Ruby und Rails zur Durchführung der Facebook OAuth-Umleitung.

```ruby
require "base64" 
  
class Controller < ActionController::Base 
   def base64url_decode(str) 
      str.gsub! '-_', '+/' 
      Base64.decode64(str.ljust(str.length+str.length%4, '=')) 
   end 
  
   def index 
      lfoauth = params[:lfoauth] 
      if not lfoauth 
         render :status => :forbidden, :text => 'Missing lfoauth.' 
      end 
  
      redirect = base64url_decode lfoauth 
  
      match = /^(http:\/\/|https:\/\/)?([^\/?]+)/i.match(redirect) 
      host = match[2] 
  
         if not host.include? 'fyre.co' 
      render :status => :forbidden, :text => 'Invalid host.' 
         end 
  
         sep = (redirect.include? '?') ? '&' : '?' 
      params.delete :lfoauth 
  
         rdir = redirect + sep + params.to_query 
      redirect_to rdir 
   end 
end
```

### Python

Dies ist ein Beispiel für die Verwendung von Python und Django bei der Facebook OAuth-Umleitung.

```python
import base64, re 
from django.views.decorators.http import require_GET 
from django.http.response import HttpResponseRedirect, HttpResponseBadRequest 
  
def base64url_decode(st): 
    return base64.b64decode(re.sub("-_","+/", st).ljust(len(st)+len(st)%4, '=')) 
  
@require_GET 
def handle_lfoauth(request): 
    lfoauth = request.GET.get('lfoauth', None) 
    import pdb; pdb.set_trace() 
    if not lfoauth: 
        return HttpResponseBadRequest('Missing lfoauth.') 
     
    redirect = base64url_decode(lfoauth) 
     
    match = re.match(r"^(http:\/\/|https:\/\/)?([^\/?]+)", redirect, re.IGNORECASE) 
    host = match.group(2) 
     
    # validate the destination to secure this proxy 
    if not 'fyre.co' in host: 
        return HttpResponseBadRequest('Invalid host.') 
     
    # if params were included in the uri already, append with &, otherwise ? 
    sep = '&' if '?' in redirect else '?' 
     
    # remove lfoauth from query param 
    dict_ = request.GET.copy() 
    dict_.pop('lfoauth') 
  
    # attach remaining param to redirect 
    rdir = redirect + sep + dict_.urlencode() 
  
    # this does the actual redirection 
    return HttpResponseRedirect(rdir)
```

### NodeJS

Dies ist ein Beispiel für die Verwendung von NodeJS und Sail/Express zur Durchführung der Facebook OAuth-Umleitung.

```nodejs
/* 
 * 
 */ 
var S = require('string'), 
     querystring = require('querystring'); 
  
var base64UrlDecode = function(str) { 
     var temp = S(str.replace('-_', '+/')).padRight(str.length+(str.length%4), '=').s 
     return new Buffer(temp, 'base64').toString('utf8'); 
} 
  
module.exports = { 
  index: function(req, res) { 
     var lfoauth = req.param('lfoauth'); 
  
     if (typeof lfoauth === 'undefined') { 
        res.send(400, 'Missing lfoauth.'); 
     } 
  
     var redirect = base64UrlDecode(lfoauth); 
  
     var match = redirect.match(/^(http:\/\/|https:\/\/)?([^\/?]+)/i); 
     var host = match[2] 
  
     if (host.indexOf('fyre.co') <= -1) { 
        res.send(400, 'Invalid host.'); 
     } 
  
     var sep = redirect.indexOf('?') > -1 ? '&' : '?'; 
  
     delete req.query['lfoauth']; 
     var rdir = redirect + sep + querystring.stringify(req.query); 
  
     res.redirect(rdir); 
  }, 
  
  _config: {} 
};
```

### Java

Dies ist ein Beispiel für die Verwendung von Java- und Spring-Controllern zur Durchführung der Facebook OAuth-Umleitung.

```java
/* 
 *  
 */ 
import java.util.Collection; 
import java.util.HashMap; 
import java.util.Map; 
import java.util.regex.Matcher; 
import java.util.regex.Pattern; 
  
import org.apache.commons.codec.binary.Base64; 
import org.apache.commons.lang.StringUtils; 
import org.jboss.resteasy.spi.BadRequestException; 
import org.springframework.stereotype.Controller; 
import org.springframework.web.bind.annotation.RequestMapping; 
import org.springframework.web.bind.annotation.RequestParam; 
import org.springframework.web.servlet.View; 
import org.springframework.web.servlet.view.RedirectView; 
  
@Controller 
public class RedirectController { 
    @RequestMapping("/fbredirect") 
    public View facebook(@RequestParam Map<string,object> allRequestParams) { 
        if (!allRequestParams.containsKey("lfoauth")) { 
            throw new BadRequestException("Missing lfoauth."); 
        } 
             
        String redirect = base64UrlDecode((String) allRequestParams.get("lfoauth")); 
  
        Pattern p = Pattern.compile("^(http:\\/\\/|https:\\/\\/)?([^\\/?]+)", Pattern.CASE_INSENSITIVE); 
        Matcher m = p.matcher(redirect); 
        if (!m.find() || !m.group(2).contains("fyre.co")) { 
            throw new BadRequestException("Invalid host."); 
        } 
         
        Map<string, object=""> params = new HashMap<string, object="">(allRequestParams); 
        params.remove("lfoauth"); 
        String rdir = redirect + (redirect.contains("?") ? '&' : '?') + mapToQueryString(params); 
         
        return new RedirectView(rdir); 
    } 
     
    private String base64UrlDecode(String str) { 
        return new String(Base64.decodeBase64(StringUtils.rightPad(str.replaceAll("-_", "+/"), str.length()+(str.length()%4), '='))); 
    } 
     
    private String mapToQueryString(Map<string, object=""> map) { 
        String queryparam = ""; 
        for (String key : map.keySet()) { 
            if (map.get(key) instanceof Collection) { 
                for (Object item : (Collection) map.get(key)) { 
                    queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, item.toString())); 
                } 
            } else { 
                queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, map.get(key).toString())); 
            } 
        } 
        return StringUtils.removeEnd(queryparam, "&"); 
    } 
}
```

### PHP

```php
<?php 
/* 
Purpose: Provide a landing page for the last step of successful oAuth 
         that is on the correct (Facebook approved) domain. 
  
Location: This file should be hosted on the same domain as your  
          Facebook App's "site url". 
  
Input Parameters:  
    - (GET) lfoauth: This should be a url-safe base64-encoded URL that  
      is the "real" final redirection URL. Livefyre sets this. 
  
      For testing purposes, this can be set to a url-safe base64-encoded  
      URL of your choosing, but the domain name must end in .fyre.co in  
      order to be considered valid. 
  
    - (GET) [all other parameters]: Any other parameters should simply  
      be passed thru on the redirection URL. If the decoded URL from "lfoauth"  
      includes querystring parameters, then the additional parameters included  
      with the initial request should be appended with "&..." 
  
Output: The response should indicate that the browser redirect (302) to the  
        "real" URL which is encoded in the "lfoauth" parameter. 
  
*/ 
  
function base64url_decode($data) { 
  return base64_decode(str_pad(strtr($data, '-_', '+/'), strlen($data) % 4, '=', STR_PAD_RIGHT)); 
} 
  
if (isset($_GET['lfoauth'])) { 
    // Warning: If implemented with non-PHP, b64 may fail because we have  
    // stripped padding (trailing ='s), to comply with Facebook parameters.   
    // The decode needs to be non-strict in this sense. 
  
    $rdir = base64url_decode($_GET['lfoauth']); 
  
    // validate the destination to secure this proxy 
    preg_match("/^(https?:\/\/)?([^\/?]+)/i", $rdir, $domain_only);    
    $host = $domain_only[2]; 
    if (!strstr($host,'fyre.co')) { 
        echo "Error - this redirection is not allowed! ".$host; 
        exit; 
    } 
  
    // if params were included in the uri already, append with &, otherwise ? 
    $sep = strstr($rdir,'?') ? '&' : '?'; 
  
    // don't include this in the params we add to the redirect url 
    unset($_GET['lfoauth']); 
  
    // assemble a new querystring from the remaining inbound GET params 
    $rdir = $rdir.$sep.http_build_query($_GET); 
  
    // this does the actual redirection, PHP's implementation is weird 
    header('Location: '.$rdir); 
} 
?>
```

## Konfigurieren von &quot;An&quot;-Anbietern {#section_rdk_dpl_b1b}

Standardmäßig werden in den Livefyre-Core-Anwendungen die Schaltflächen Facebook, LinkedIn und Twitter &quot;Posten auf&quot;angezeigt. Verwenden Sie den Parameter postToButtons, um zu konfigurieren, welche Anbieter beim Einbetten der Livefyre-App angezeigt werden.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` ist ein Array mit einer beliebigen Untergruppe der folgenden Optionen:

* tw: Twitter
* fb: Facebook
* li: LinkedIn
