---
description: Gibt ein Collection-Objekt zurück, das als Kommentartyp instanziiert wurde. Führen Sie createOrUpdate() vom Collection-Objekt aus, um den Build-Prozess abzuschließen.
seo-description: Gibt ein Collection-Objekt zurück, das als Kommentartyp instanziiert wurde. Führen Sie createOrUpdate() vom Collection-Objekt aus, um den Build-Prozess abzuschließen.
seo-title: buildCommentsCollection-Site-Methode
solution: Experience Manager
title: buildCommentsCollection-Site-Methode
uuid: 0e5c062e-960d-4ab0-ba32-0965731a1571
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildCommentsCollection-Site-Methode{#buildcommentscollection-site-method}

Gibt ein Collection-Objekt zurück, das als Kommentartyp instanziiert wurde. Führen Sie createOrUpdate() vom Collection-Objekt aus, um den Build-Prozess abzuschließen.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| title | Zeichenfolge | Der Titel der Sammlung. |
| articleId | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung auf Ihrer Site gewählt haben. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Python-Beispiel {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
