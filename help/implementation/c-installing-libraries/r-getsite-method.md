---
description: Gibt ein neues Site-Objekt zurück.
seo-description: Gibt ein neues Site-Objekt zurück.
seo-title: getSite-Netzwerkmethode
solution: Experience Manager
title: getSite-Netzwerkmethode
uuid: 67de781e-5240-4be5-9e93-c614828e0bb5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getSite-Netzwerkmethode{#getsite-network-method}

Gibt ein neues Site-Objekt zurück.
|Variable|Typ|Beschreibung||—|—|—||siteId|String|Die Livefyre-angegebene ID für die Website oder Anwendung, zu der die Sammlung gehört. Beispiel: 303617.  ||siteKey|String|Der von Livefyre bereitgestellte geheime Schlüssel für siteId.  |

## Java-Beispiel {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Python-Beispiel {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

