---
description: Gibt ein neues Site-Objekt zurück.
title: getSite-Netzwerkmethode
exl-id: 88782da9-88c6-4e60-9a23-e46d68675d59
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# getSite-Netzwerkmethode{#getsite-network-method}

Gibt ein neues Site-Objekt zurück.
|Variable|Typ|Beschreibung|
|— |— |— |
|siteId|String|Die Livefyre-angegebene ID für die Website oder Anwendung, zu der die Sammlung gehört. Beispiel: 303617.  |
|siteKey|String|Der von Livefyre bereitgestellte geheime Schlüssel für siteId.  |

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
