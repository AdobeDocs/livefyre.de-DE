---
description: Gibt ein Collection-Objekt zurück, das als ein Sistat-Typ instanziiert wurde. Führen Sie create_or_update() vom Collection-Objekt aus, um den Build-Prozess abzuschließen.
title: buildSitenotesCollection-Site-Methode
exl-id: c722baf2-91d4-4c05-97e1-ea585e91c416
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 7%

---

# buildSitenotesCollection-Site-Methode{#buildsitenotescollection-site-method}

Gibt ein Collection-Objekt zurück, das als ein Sistat-Typ instanziiert wurde. Führen Sie create_or_update() vom Collection-Objekt aus, um den Build-Prozess abzuschließen.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| title | Zeichenfolge | Der Titel der Sammlung. |
| articleId | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung auf Ihrer Site gewählt haben. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildSidenotesCollection(title, articleId, url); 
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildSidenotesCollection(title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildSidenotesCollection(title, articleId, url); 
```

## Python-Beispiel {#section_dwg_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```
