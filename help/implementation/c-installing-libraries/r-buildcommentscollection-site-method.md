---
description: Gibt ein Collection-Objekt zurück, das als Kommentartyp instanziiert
  wird. Führen Sie createorupdate () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-description: Gibt ein Collection-Objekt zurück, das als Kommentartyp instanziiert
  wird. Führen Sie createorupdate () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-title: Buildcommentscollection-Site-Methode
solution: Experience Manager
title: Buildcommentscollection-Site-Methode
uuid: 0 e 5 c 062 e -960 d -4 ab 0-ba 32-0965731 a 1571
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Buildcommentscollection-Site-Methode{#buildcommentscollection-site-method}

Gibt ein Collection-Objekt zurück, das als Kommentartyp instanziiert wird. Führen Sie createorupdate () aus dem Collection-Objekt aus, um den Build-Prozess abzuschließen.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| Titel | Zeichenfolge | Der Titel für die Sammlung. |
| Articleid | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung innerhalb Ihrer Site auswählen. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Python Example {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
