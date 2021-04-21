---
description: Diese Methode gibt die URN für den Benutzer dieses Netzwerks zurück.
title: getUrnForUser-Netzwerkmethode
exl-id: 272e724e-d09d-4d7d-9967-a229707ff47f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

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
