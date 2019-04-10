---
description: Gibt ein Collection-Objekt zurück, das als Blog-Typ instanziiert wird.
  Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-description: Gibt ein Collection-Objekt zurück, das als Blog-Typ instanziiert
  wird. Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-title: Buildblogcollection-Site-Methode
solution: Experience Manager
title: Buildblogcollection-Site-Methode
uuid: 6 a 5 ec 6 b 9-bc 32-467 a-abe 6-a 57 c 6 defe 67
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Buildblogcollection-Site-Methode{#buildblogcollection-site-method}

Gibt ein Collection-Objekt zurück, das als Blog-Typ instanziiert wird. Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess abzuschließen.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| Titel | Zeichenfolge | Der Titel für die Sammlung. |
| Articleid | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung innerhalb Ihrer Site auswählen. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildBlogCollection(title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildBlogCollection(title, articleId, url); 
```

## Python Example {#section_dwg_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

