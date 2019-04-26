---
description: Gibt ein Collection-Objekt zurück, das als Überprüfungstyp instanziiert
  wird. Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-description: Gibt ein Collection-Objekt zurück, das als Überprüfungstyp instanziiert
  wird. Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-title: Buildreviewscollection-Site-Methode
solution: Experience Manager
title: Buildreviewscollection-Site-Methode
uuid: 88 af 4 c 88-57 de -4 ae 9-9394-550 c 94 off 48 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Buildreviewscollection-Site-Methode{#buildreviewscollection-site-method}

Gibt ein Collection-Objekt zurück, das als Überprüfungstyp instanziiert wird. Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess abzuschließen.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| Titel | Zeichenfolge | Der Titel für die Sammlung. |
| Articleid | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung innerhalb Ihrer Site auswählen. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |


## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildReviewsCollection(title, articleId, url); 
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildReviewsCollection(title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildReviewsCollection(title, articleId, url); 
```

## Python Example {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

