---
description: 'null '
seo-description: 'null '
seo-title: buildCollection-Site-Methode
solution: Experience Manager
title: buildCollection-Site-Methode
uuid: 52abc42a-9506-4492-b219-f2e05eb79c5f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildCollection-Site-Methode{#buildcollection-site-method}

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| type | CollectionType | Der Typ der Sammlung. |
| title | Zeichenfolge | Der Titel der Sammlung. |
| articleId | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung auf Ihrer Site gewählt haben. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Python-Beispiel {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
