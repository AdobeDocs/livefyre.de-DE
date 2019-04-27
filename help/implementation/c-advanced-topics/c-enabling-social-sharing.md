---
description: Richten Sie Anmeldeinformationen ein, mit denen Ihre Benutzer Inhalte für verschiedene soziale Netzwerke freigeben können.
seo-description: Richten Sie Anmeldeinformationen ein, mit denen Ihre Benutzer Inhalte für verschiedene soziale Netzwerke freigeben können.
seo-title: Aktivieren von Social Sharing
solution: Experience Manager
title: Aktivieren von Social Sharing
uuid: f 584 a 0 ae -46 c 7-48 c 1-aea 4-36 da 9 f 1 e 259 b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830

---


# Aktivieren von Social Sharing {#enabling-social-sharing}

Richten Sie Anmeldeinformationen ein, mit denen Ihre Benutzer Inhalte für verschiedene soziale Netzwerke freigeben können.

Um Benutzern das Freigeben von Inhalten über soziale Medien zu ermöglichen, implementieren Sie die Social Sharing-Funktion von Livefyre und erstellen ein oauth-System, um eine ordnungsgemäße Authentifizierung für diese Sites bereitzustellen. Bei diesem System reagiert Livefyre auf den Namen des Benutzers, wenn er Inhalte über soziale Netzwerke freigeben möchte.

>[!NOTE]
>
>Verschiedene Anbieter verfügen über unterschiedliche oauth-Anforderungen. Bitte wenden Sie sich an Ihren Anbieter, um die mit ihrer Implementierung von oauth verknüpften Informationen abzurufen.

## Erforderliche Social-Anmeldeinformationen {#section_gff_cjm_b1b}

Wenn Sie ein benutzerdefiniertes Benutzeridentitätssystem verwenden, müssen Sie Ihre Anmeldeinformationen für soziale Netzwerke bereitstellen, damit Benutzer über eine Livefyre-App für Twitter, Facebook oder linkedin freigeben können.

>[!NOTE]
>
>Kunden, die mit Janrain Interagieren, müssen nur ihre Interaktionsdomäne und den Interagieren-API-Schlüssel bereitstellen.

Verwenden Sie das Integrationseinstellungs-Bedienfeld der Admin-Konsole, um die folgenden Social-Anmeldeinformationen einzugeben oder zu aktualisieren.

### Erforderliche Anmeldeinformationen:

* **Geheimer Facebook** -Client-ID Geheimer oauth Proxy-Umleitung
* **Linkedin** API-Schlüssel-API-Schlüssel
* **Secret API Schlüssel API für Twitter** Access Token Access API

## Twitter {#section_qp5_1yl_b1b}

Twitter-Anmeldeinformationen sind über das Twitter-App-Dashboard verfügbar. So finden Sie die Anmeldeinformationen:

* Öffnen Sie [die App-Seite](https://dev.twitter.com/apps) von Twitter als App-Eigentümer, suchen Sie Ihre Anwendung und klicken Sie auf den Titel.
* Blättern Sie nach unten zu &quot;Ihr Zugriffstoken&quot; und rufen Sie die Werte von&quot; Access token&quot; und &quot;Access tokensecret&quot; auf. »

Sie müssen:

* Geben Sie in der Twitter-App einen Wert für das Feld &quot;Callback-URL&quot; ein. Dieses Feld kann ein einfacher Platzhalter sein, kann aber nicht leer sein.
* Legen Sie den Anwendungstyp so fest, dass er über **Lese** - und **Schreibzugriff** verfügt.
* Vergewissern Sie sich, dass sich die URL der Twitter-App in derselben Hostdomäne befindet wie die Livefyre-Core-App.

>[!NOTE]
>
>Alle Anwendungen, die Twitter-Inhalte anzeigen, müssen ihren Anzeigeanforderungen entsprechen. Weitere Informationen finden Sie in den [Twitter-Anzeigerichtlinien](https://dev.twitter.com/terms/display-requirements) .

## Linkedin {#section_lfz_zxl_b1b}

Linkedin-Anmeldeinformationen sind im Abschnitt oauth-Schlüssel der API-Schlüssel Ihrer linkedin-Anwendung verfügbar.

* Melden Sie sich bei Ihrem Konto von linkedin Developers Page [https://developer.linkedin.com/](https://developer.linkedin.com/)an.
* Bewegen Sie den Mauszeiger oben rechts über Ihren Namen und wählen Sie im Dropdown-Menü die Option API-Schlüssel aus.
* Klicken Sie auf den Anwendungstitel.
* Rufen Sie den API-Schlüssel und die geheimen Schlüssel aus dem oauth-Schlüssel auf.

## Facebook {#section_zyb_gpl_b1b}

Facebook-Anmeldeinformationen sind auf Ihrer Developer Apps-Seite verfügbar.

* Öffnen Sie die [Seite Developer Apps von](https://developers.facebook.com/apps) Facebook als App-Eigentümer, suchen Sie Ihre Anwendung und klicken Sie auf den Titel.
* Erfassen Sie die Werte für App-ID und App-Geheimnis. Für den App-geheimen Schlüssel müssen Sie auf die Schaltfläche &quot;Anzeigen&quot; klicken, um ihn anzuzeigen.

Für die Freigabe auf Facebook müssen Sie eine Umleitungsseite einrichten, um Facebook-Anforderungen aufzunehmen und die von [Facebook geforderten Domänen einzuhalten](https://developers.facebook.com/docs/reference/dialogs/oauth/). Die Seite muss in Ihrer Domäne gehostet werden, damit Facebook überprüfen kann, ob die Anforderung von einer rechtmäßigen Quelle stammt.

### Facebook-Umleitung

Die gehostete Seite sollte den folgenden Code enthalten:

### Ruby

Dies ist ein Beispiel für Ruby und Rails, um die Facebook oauth-Umleitung durchzuführen.

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

Dies ist ein Beispiel für Python und Django, um die Facebook oauth-Umleitung durchzuführen.

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

### Nodejs

Dies ist ein Beispiel mit nodejs und Sail/Express, um die Facebook oauth-Umleitung durchzuführen.

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

Dies ist ein Beispiel für Java und Spring Controller, um die Facebook oauth-Umleitung durchzuführen.

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

## Konfigurieren von Anbietern von Beiträgen {#section_rdk_dpl_b1b}

Standardmäßig werden Facebook-, linkedin- und Twitter-Schaltflächen &quot;Post to&quot; auf Livefyre-Core-Anwendungen angezeigt. Verwenden Sie den Parameter posttobuttons, um zu konfigurieren, welche Anbieter beim Einbetten der Livefyre-App angezeigt werden.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` ist ein Array mit einer beliebigen Untergruppe der folgenden Optionen:

* tw: Twitter
* fb: Facebook
* li: Linkedin
