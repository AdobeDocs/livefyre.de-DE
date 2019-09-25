---
description: Gibt ein Collection-Objekt zurück, das als Blog-Typ instanziiert wurde. Führen Sie create_or_update() vom Collection-Objekt aus, um den Build-Prozess abzuschließen.
seo-description: Gibt ein Collection-Objekt zurück, das als Blog-Typ instanziiert wurde. Führen Sie create_or_update() vom Collection-Objekt aus, um den Build-Prozess abzuschließen.
seo-title: buildBlogCollection-Site-Methode
solution: Experience Manager
title: buildBlogCollection-Site-Methode
uuid: 6a5ec6b9-bc32-467a-abe6-a57c6defe067
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildBlogCollection-Site-Methode{#buildblogcollection-site-method}

Gibt ein Collection-Objekt zurück, das als Blog-Typ instanziiert wurde. Führen Sie create_or_update() vom Collection-Objekt aus, um den Build-Prozess abzuschließen.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| title | Zeichenfolge | Der Titel der Sammlung. |
| articleId | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung auf Ihrer Site gewählt haben. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildBlogCollection(title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildBlogCollection(title, articleId, url); 
```

## Python-Beispiel {#section_dwg_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

