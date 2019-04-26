---
description: Gibt ein Collection-Objekt zurück, das als Chat-Typ instanziiert wird.
  Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-description: Gibt ein Collection-Objekt zurück, das als Chat-Typ instanziiert
  wird. Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-title: Buildchatcollection-Site-Methode
solution: Experience Manager
title: Buildchatcollection-Site-Methode
uuid: 39 ee 32 d 0-29 c 9-47 a 8-a 458-a 3 cf 7 a 96 db 30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d

---


# Buildchatcollection-Site-Methode{#buildchatcollection-site-method}

Gibt ein Collection-Objekt zurück, das als Chat-Typ instanziiert wird. Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess abzuschließen.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| Titel | Zeichenfolge | Der Titel für die Sammlung. |
| Articleid | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung innerhalb Ihrer Site auswählen. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Python Example {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
