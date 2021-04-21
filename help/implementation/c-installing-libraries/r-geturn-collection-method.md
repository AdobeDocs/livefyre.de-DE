---
description: Diese Methode gibt die URN für diese Sammlung zurück. Sie müssen createOrUpdate() ausführen, bevor Sie diese Methode ausführen.
title: getUrn-Erfassungsmethode
exl-id: bea04805-8f02-4c06-9a1a-6b057de831ab
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# getUrn-Erfassungsmethode{#geturn-collection-method}

Diese Methode gibt die URN für diese Sammlung zurück. Sie müssen createOrUpdate() ausführen, bevor Sie diese Methode ausführen.

## Java-Beispiel {#section_nyl_ycs_rz}

```
collection.getUrn(); 
```

Beispielausgabe:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
collection.getUrn(); 
```

Beispielausgabe:

```
<span class="str">"urn:livefyre:network=`example.fyre.co`:site=1:collection=1"</span>
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$collection->getUrn(); 
```

Beispielausgabe:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Python-Beispiel {#section_dwg_gds_rz}

```
collection.urn() 
```

Beispielausgabe:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
collection.urn
```

Beispielausgabe:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```
