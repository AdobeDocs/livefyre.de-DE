---
description: 'null '
seo-description: 'null '
seo-title: Buildcollection-Site-Methode
solution: Experience Manager
title: Buildcollection-Site-Methode
uuid: 52 abc 42 a -9506-4492-b 219-f 2 e 05 eb 79 c 5 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Buildcollection-Site-Methode{#buildcollection-site-method}

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| type | Collectiontype | Der Typ der Sammlung. |
| Titel | Zeichenfolge | Der Titel für die Sammlung. |
| Articleid | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung innerhalb Ihrer Site auswählen. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Python Example {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
