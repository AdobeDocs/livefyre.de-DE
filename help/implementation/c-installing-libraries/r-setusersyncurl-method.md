---
description: Informiert Livefyre, die Benutzersynchronisierung des Netzwerks mit dem bereitgestellten zu aktualisieren. Gibt einen Booleschen Wert zurück.
seo-description: Informiert Livefyre, die Benutzersynchronisierung des Netzwerks mit dem bereitgestellten zu aktualisieren. Gibt einen Booleschen Wert zurück.
seo-title: Setusersyncurl Network-Methode
solution: Experience Manager
title: Setusersyncurl Network-Methode
uuid: cd 067 e 90-a 2 da -4 e 3 d -8 e 60-7 eabfd 86 fc 7 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Setusersyncurl Network-Methode{#setusersyncurl-network-method}

Informiert Livefyre, die Benutzersynchronisierung des Netzwerks mit dem bereitgestellten zu aktualisieren. Gibt einen Booleschen Wert zurück.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| Urltemplate | Zeichenfolge | Die URL zur Registrierung bei Livefyre für die Synchronisierung von Benutzer-IDs. Erfordert &quot;`{id}`«als Teil der angegebenen URL-Zeichenfolge. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Beispielausgabe:

```
true
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Beispielausgabe:

```
true
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Beispielausgabe:

```
true
```

## Python Example {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Beispielausgabe:

```
True
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Beispielausgabe:

```
True
```
