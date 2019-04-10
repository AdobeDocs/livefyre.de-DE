---
description: Gibt ein Collection-Objekt zurück, das als "Sidenotes" -Typ instanziiert
  wird. Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-description: Gibt ein Collection-Objekt zurück, das als "Sidenotes" -Typ instanziiert
  wird. Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess
  abzuschließen.
seo-title: Buildsitenotescollection-Site-Methode
solution: Experience Manager
title: Buildsitenotescollection-Site-Methode
uuid: 2 bfbc 032-4 c 0 c -48 d 2-8 ce 6-02460 b 38 bd 6 c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Buildsitenotescollection-Site-Methode{#buildsitenotescollection-site-method}

Gibt ein Collection-Objekt zurück, das als "Sidenotes" -Typ instanziiert wird. Führen Sie create_ or_ update () aus dem Collection-Objekt aus, um den Build-Prozess abzuschließen.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| Titel | Zeichenfolge | Der Titel für die Sammlung. |
| Articleid | Zeichenfolge | Eine eindeutige Artikel-ID, die Sie zur Identifizierung einer Sammlung innerhalb Ihrer Site auswählen. |
| url | Zeichenfolge | Die kanonische absolute URL für diese Sammlung. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Collection collection = site.buildSidenotesCollection(title, articleId, url); 
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

```
var collection = site.buildSidenotesCollection(title, articleId, url); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection = site->buildSidenotesCollection(title, articleId, url); 
```

## Python Example {#section_dwg_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```
