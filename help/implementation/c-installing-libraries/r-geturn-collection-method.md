---
description: Diese Methode gibt die URN für diese Sammlung zurück. Sie müssen createOrUpdate() ausführen, bevor Sie diese Methode ausführen.
seo-description: Diese Methode gibt die URN für diese Sammlung zurück. Sie müssen createOrUpdate() ausführen, bevor Sie diese Methode ausführen.
seo-title: getUrn-Erfassungsmethode
solution: Experience Manager
title: getUrn-Erfassungsmethode
uuid: 2f4d7796-2ae5-4b74-a958-40825c6bff16
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

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

