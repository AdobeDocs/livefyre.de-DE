---
description: Legt SSL fest, damit API-Aufrufe ein- oder ausgeschaltet werden.
title: setSSL-Netzwerkmethode
exl-id: 5682b84a-0b4d-479b-af40-60d2c6c38155
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# setSSL-Netzwerkmethode{#setssl-network-method}

Legt SSL fest, damit API-Aufrufe ein- oder ausgeschaltet werden.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| ssl | Boolesch | Der Standardwert ist &quot;true&quot;. wenn SSL aktiviert sein soll, andernfalls false. <br><ul><li>True - SSL unter </li><li>False - SSL deaktiviert</li></ul> |

## Java-Beispiel {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Python-Beispiel {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
network.ssl = false 
```
