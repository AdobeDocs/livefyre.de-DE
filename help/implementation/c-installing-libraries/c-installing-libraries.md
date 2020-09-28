---
description: Bibliotheken für serverseitige Aufgaben von Livefyre installieren
seo-description: Bibliotheken für serverseitige Aufgaben von Livefyre installieren
seo-title: Installation
solution: Experience Manager
title: Installation
uuid: f60b4cc7-178f-4a16-ba75-f1d0d171c52f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Installation{#installation}


## Java {#section_yd3_3zk_rz}

Um die Java-Bibliothek zu installieren, fügen Sie dem POM Ihres Projekts diese Abhängigkeit hinzu:

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

Die Java-Bibliothek ist von den folgenden Modulen abhängig:

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

Weitere Informationen finden Sie in den Java-Dokumenten oder in der Quelle auf [GitHub](https://github.com/Livefyre/livefyre-java-utils).

## NodeJS {#section_swj_pwq_rz}

Führen Sie folgende Zeile aus, um die NodeJS-Bibliothek zu installieren:

`$ npm install livefyre`

Die NodeJS-Bibliothek ist von den folgenden Modulen abhängig:

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

Weitere Informationen finden Sie im Dokument NodeJs oder in der Quelle auf [GitHub](https://github.com/Livefyre/livefyre-nodejs-utils).

Links: [Restler](https://github.com/danwrong/restler), [Validator](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Um die PHP-Bibliothek mit Composer zu installieren, fügen Sie Ihrer composer.json Folgendes hinzu:

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

Installieren Sie anschließend mithilfe von:

```
composer.phar install 
```

Wenn Sie Composer **nicht** verwenden, können Sie die neueste Version der Bibliothek wie folgt abrufen:

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

Um die Bibliothek zu verwenden, fügen Sie dem PHP-Skript Folgendes hinzu:

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

Die PHP-Bibliothek ist von den folgenden Modulen abhängig:

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

For more information, read the PHP docs or see the source on [GitHub](https://github.com/Livefyre/livefyre-php-utils).

Links: [ext-json](https://php.net/manual/en/book.json.php), [Requests](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Um die Python-Bibliothek zu installieren, führen Sie folgende Zeile aus:

`$ pip install livefyre`

Die Python-Bibliothek ist von den folgenden Modulen abhängig:

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

Weitere Informationen finden Sie in den Python-Dokumenten oder in der Quelle auf [GitHub](https://github.com/Livefyre/livefyre-python-utils).

Links: [PyJWT](https://github.com/progrium/pyjwt), [Requests](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum34](https://pypi.python.org/pypi/enum34), [OrderedDict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

Um die Ruby-Bibliothek zu installieren, fügen Sie die folgende Zeile zur Gemfile Ihrer Anwendung hinzu:

```
gem 'livefyre' 
```

Oder installieren Sie es selbst:

`$ gem install livefyre`

Die Ruby-Bibliothek ist von den folgenden Modulen abhängig:

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

Weitere Informationen finden Sie in den Ruby-Dokumenten oder in der Quelle auf [GitHub](https://github.com/Livefyre/livefyre-ruby-utils).

Links: [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST Client](https://github.com/rest-client/rest-client/), [Addressable](https://github.com/sporkmonger/addressable)
