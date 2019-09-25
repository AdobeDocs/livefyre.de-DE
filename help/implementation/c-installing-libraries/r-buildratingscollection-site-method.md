---
description: Gibt ein Collection-Objekt zurück, das als Ratings-Typ instanziiert wurde. Führen Sie create_or_update() vom Collection-Objekt aus, um den Build-Prozess abzuschließen.
seo-description: Gibt ein Collection-Objekt zurück, das als Ratings-Typ instanziiert wurde. Führen Sie create_or_update() vom Collection-Objekt aus, um den Build-Prozess abzuschließen.
seo-title: buildRatingsCollection-Site-Methode
title: buildRatingsCollection-Site-Methode
uuid: 5eea2ba3-48e1-4cd2-aa73-ea81788af1df
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildRatingsCollection-Site-Methode{#buildratingscollection-site-method}

Gibt ein Collection-Objekt zurück, das als Ratings-Typ instanziiert wurde. Führen Sie create_or_update() vom Collection-Objekt aus, um den Build-Prozess abzuschließen.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| title | Zeichenfolge | Der Titel der Sammlung. |
| articleId | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung auf Ihrer Site gewählt haben. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildRatingsCollection(title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildRatingsCollection(title, articleId, url); 
```

## Python-Beispiel {#section_dwg_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

