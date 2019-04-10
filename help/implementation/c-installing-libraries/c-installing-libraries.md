---
description: Bibliotheken für Livefyre-serverseitige Aufgaben installieren
seo-description: Bibliotheken für Livefyre-serverseitige Aufgaben installieren
seo-title: Installation
solution: Experience Manager
title: Installation
uuid: f 60 b 4 cc 7-178 f -4 a 16-ba 75-f 1 d 0 d 171 c 52 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Installation{#installation}


## Java {#section_yd3_3zk_rz}

Um die Java-Bibliothek zu installieren, fügen Sie diese Abhängigkeit dem Projektpom hinzu:

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

Die Java-Bibliothek hat Abhängigkeiten zu den folgenden Modulen:

```
<dependency> 
   <groupId>com.sun.jersey</groupId> 
   <artifactId>jersey-client</artifactId> 
   <version>[1.18.1,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.code.gson</groupId> 
   <artifactId>gson</artifactId> 
   <version>[2.3,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.guava</groupId> 
   <artifactId>guava</artifactId> 
   <version>[18.0,)</version> 
</dependency> 
<dependency> 
   <groupId>org.apache.commons</groupId> 
   <artifactId>commons-lang3</artifactId> 
   <version>[3.0.1,)</version> 
</dependency> 
<dependency> 
   <groupId>org.bitbucket.b_c</groupId> 
   <artifactId>jose4j</artifactId> 
   <version>[0.4.1,)</version> 
</dependency> 
```

Weitere Informationen finden Sie unter Java-Dokumente oder die Quelle auf [github](https://github.com/Livefyre/livefyre-java-utils).

## Nodejs {#section_swj_pwq_rz}

Führen Sie folgende Zeile aus, um die nodejs-Bibliothek zu installieren:

`$ npm install livefyre`

Die nodejs-Bibliothek hat Abhängigkeiten zu den folgenden Modulen:

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

Weitere Informationen finden Sie unter nodejs-Dokumente oder die Quelle auf [github](https://github.com/Livefyre/livefyre-nodejs-utils).

Links: [Restler](https://github.com/danwrong/restler), [Validator](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Um die PHP-Bibliothek mit Composer zu installieren, fügen Sie dies Ihrem Composer. json hinzu:

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

Installieren Sie anschließend mit:

```
composer.phar install 
```

Wenn Sie den Composer **nicht** verwenden, rufen Sie die neueste Version der Bibliothek auf:

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

Um die Bibliothek zu verwenden, fügen Sie Ihrem PHP-Skript Folgendes hinzu:

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

Die PHP-Bibliothek hat Abhängigkeiten zu den folgenden Modulen:

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

Weitere Informationen finden Sie in den PHP-Dokumenten oder in der Quelle auf [github](https://github.com/Livefyre/livefyre-php-utils).

Links: [ext-json](https://php.net/manual/en/book.json.php), [Requests](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Führen Sie folgende Zeile aus, um die Python-Bibliothek zu installieren:

`$ pip install livefyre`

Die Python-Bibliothek hat die folgenden Abhängigkeiten:

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

Weitere Informationen finden Sie unter Python-Dokumente oder die Quelle auf [github](https://github.com/Livefyre/livefyre-python-utils).

Links: [Pyjwt](https://github.com/progrium/pyjwt), [Requests](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum 34](https://pypi.python.org/pypi/enum34), [ordereddict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

Um die Ruby-Bibliothek zu installieren, fügen Sie diese Zeile Ihrer Anwendung hinzu:

```
gem 'livefyre' 
```

Oder Sie selbst installieren:

`$ gem install livefyre`

Die Ruby-Bibliothek hat Abhängigkeiten zu den folgenden Modulen:

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

Weitere Informationen finden Sie unter Ruby-Dokumente oder die Quelle auf [github](https://github.com/Livefyre/livefyre-ruby-utils).

Links: [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST Client](https://github.com/rest-client/rest-client/), [Addressable](https://github.com/sporkmonger/addressable)
