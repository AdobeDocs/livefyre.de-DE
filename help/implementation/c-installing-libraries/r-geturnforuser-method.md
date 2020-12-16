---
description: Diese Methode gibt die URN für den Benutzer dieses Netzwerks zurück.
seo-description: Diese Methode gibt die URN für den Benutzer dieses Netzwerks zurück.
seo-title: getUrnForUser-Netzwerkmethode
solution: Experience Manager
title: getUrnForUser-Netzwerkmethode
uuid: b70b8b0f-2b3a-4a1d-90d0-93a97a137ad4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---


# getUrnForUser-Netzwerkmethode{#geturnforuser-network-method}

Diese Methode gibt die URN für den Benutzer dieses Netzwerks zurück.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| userId | Zeichenfolge | Die in der URL zu verwendende userId. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Beispielausgabe:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

Beispielausgabe:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

Beispielausgabe:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Python-Beispiel {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

Beispielausgabe:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

Beispielausgabe:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
