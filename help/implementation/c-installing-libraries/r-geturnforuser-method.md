---
description: Diese Methode gibt die URN für den Benutzer dieses Netzwerks zurück.
seo-description: Diese Methode gibt die URN für den Benutzer dieses Netzwerks zurück.
seo-title: Geturnforuser-Netzwerkmethode
solution: Experience Manager
title: Geturnforuser-Netzwerkmethode
uuid: b 70 b 8 b 0 f -2 b 3 a -4 a 1 d -90 d 0-93 a 97 a 137 ad 4
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Geturnforuser-Netzwerkmethode{#geturnforuser-network-method}

Diese Methode gibt die URN für den Benutzer dieses Netzwerks zurück.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| Userid | Zeichenfolge | Die in der URN zu verwendende userid. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Beispielausgabe:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

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

## Python Example {#section_dwg_gds_rz}

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
