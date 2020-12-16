---
description: Legt SSL fest, damit API-Aufrufe ein- oder ausgeschaltet werden.
seo-description: Legt SSL fest, damit API-Aufrufe ein- oder ausgeschaltet werden.
seo-title: setSSL-Netzwerkmethode
solution: Experience Manager
title: setSSL-Netzwerkmethode
uuid: 8d989e63-c859-456a-99ca-8d87933913ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 7%

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
