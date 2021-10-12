---
description: Installieren der Bibliotheken für serverseitige Aufgaben für Livefyre
title: Installation
exl-id: d74f85be-14c0-4f6d-8f16-b688282c0eb0
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---

# Installation{#installation}


## Java {#section_yd3_3zk_rz}

Um die Java-Bibliothek zu installieren, fügen Sie diese Abhängigkeit zum POM Ihres Projekts hinzu:

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

Die Java-Bibliothek weist Abhängigkeiten von den folgenden Modulen auf:

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

Weitere Informationen finden Sie in den Java-Dokumenten oder in der Quelle unter [GitHub](https://github.com/Livefyre/livefyre-java-utils).

## NodeJS {#section_swj_pwq_rz}

Führen Sie folgende Zeile aus, um die NodeJS-Bibliothek zu installieren:

`$ npm install livefyre`

Die NodeJS-Bibliothek weist Abhängigkeiten von den folgenden Modulen auf:

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

Weitere Informationen finden Sie in der NodeJs-Dokumentation oder in der Quelle unter [GitHub](https://github.com/Livefyre/livefyre-nodejs-utils).

Links: [Restler](https://github.com/danwrong/restler), [Validator](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Um die PHP-Bibliothek mit Composer zu installieren, fügen Sie dies zu Ihrem Composer.json hinzu:

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

Installieren Sie anschließend mithilfe von:

```
composer.phar install 
```

Wenn Sie **nicht** den Composer verwenden, rufen Sie die neueste Version der Bibliothek mit folgendem Code ab:

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

Um die Bibliothek zu verwenden, fügen Sie Ihrem PHP-Skript Folgendes hinzu:

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

Die PHP-Bibliothek ist von den folgenden Modulen abhängig:

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

Weitere Informationen finden Sie in den PHP-Dokumenten oder in der Quelle unter [GitHub](https://github.com/Livefyre/livefyre-php-utils).

Links: [ext-json](https://www.php.net/manual/en/book.json.php), [Requests](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Führen Sie folgende Zeile aus, um die Python-Bibliothek zu installieren:

`$ pip install livefyre`

Die Python-Bibliothek weist Abhängigkeiten von den folgenden Modulen auf:

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

Weitere Informationen finden Sie in der Python-Dokumentation oder in der Quelle unter [GitHub](https://github.com/Livefyre/livefyre-python-utils).

Links: [PyJWT](https://github.com/progrium/pyjwt), [Requests](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum34](https://pypi.python.org/pypi/enum34), [OrderedDict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

Um die Ruby-Bibliothek zu installieren, fügen Sie diese Zeile zur Gemfile Ihrer Anwendung hinzu:

```
gem 'livefyre' 
```

Oder installieren Sie es selbst:

`$ gem install livefyre`

Die Ruby-Bibliothek weist Abhängigkeiten von den folgenden Modulen auf:

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

Weitere Informationen finden Sie in der Ruby-Dokumentation oder in der Quelle unter [GitHub](https://github.com/Livefyre/livefyre-ruby-utils).

Links: [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST Client](https://github.com/rest-client/rest-client/), [Addressable](https://github.com/sporkmonger/addressable)
