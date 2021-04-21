---
title: buildCollection-Site-Methode
description: buildCollection-Site-Methode
exl-id: d5c9a2fb-2d30-44f4-8ebf-24b0ec7babee
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 13%

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
