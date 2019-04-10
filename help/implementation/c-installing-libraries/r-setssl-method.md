---
description: Setzt SSL für API-Aufrufe ein oder aus.
seo-description: Setzt SSL für API-Aufrufe ein oder aus.
seo-title: Setssl Network-Methode
solution: Experience Manager
title: Setssl Network-Methode
uuid: 8 d 989 e 63-c 859-456 a -99 ca -8 d 87933913 ba
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Setssl Network-Methode{#setssl-network-method}

Setzt SSL für API-Aufrufe ein oder aus.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| ssl | Boolescher Wert | Der Standardwert ist "true" . Wenn SSL aktiviert ist, andernfalls false. <br><ul><li>True - SSL </li><li>False - SSL deaktiviert</li></ul> |

## Java-Beispiel {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Python Example {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
network.ssl = false 
```
