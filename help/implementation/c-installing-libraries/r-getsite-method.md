---
description: Gibt ein neues Site-Objekt zurück.
seo-description: Gibt ein neues Site-Objekt zurück.
seo-title: Getsite-Netzwerkmethode
solution: Experience Manager
title: Getsite-Netzwerkmethode
uuid: 67 de 781 e -5240-4 be 5-9 e 93-c 614828 e 0 bb 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Getsite-Netzwerkmethode{#getsite-network-method}

Gibt ein neues Site-Objekt zurück.
| Variable | Typ | Beschreibung|
|— |— |— |
| Siteid | String | Die Livefyre-bereitgestellte ID für die Website oder Anwendung, zu der die Sammlung gehört. Beispiel: 303617. |
| Sitekey | String | Die Geheimer geheimer Schlüssel für siteid. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Python Example {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

