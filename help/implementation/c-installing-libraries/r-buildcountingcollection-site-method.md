---
description: Gibt ein Collection-Objekt zurück, das als Zähltyp instanziiert wird.
  Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-description: Gibt ein Collection-Objekt zurück, das als Zähltyp instanziiert wird.
  Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-title: Buildcountingcollection-Site-Methode
title: Buildcountingcollection-Site-Methode
uuid: e 293 d 66 a -0025-4230-997 e -295 ce 4625713
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Buildcountingcollection-Site-Methode{#buildcountingcollection-site-method}

Gibt ein Collection-Objekt zurück, das als Zähltyp instanziiert wird. Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess abzuschließen.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| Titel | Zeichenfolge | Der Titel für die Sammlung. |
| Articleid | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung innerhalb Ihrer Site auswählen. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildCountingCollection(title, articleId, url); 
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildCountingCollection(title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildCountingCollection(title, articleId, url); 
```

## Python Example {#section_dwg_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

