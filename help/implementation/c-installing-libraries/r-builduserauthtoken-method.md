---
description: Gibt ein vom Benutzer authentifiziertes verschlüsseltes Token für das Netzwerk zurück, aus dem es aufgerufen wird.
seo-description: Gibt ein vom Benutzer authentifiziertes verschlüsseltes Token für das Netzwerk zurück, aus dem es aufgerufen wird.
seo-title: buildUserAuthToken-Netzwerkmethode
solution: Experience Manager
title: buildUserAuthToken-Netzwerkmethode
uuid: 8828d356-c3c6-46a6-91bf-83bd59e35050
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildUserAuthToken-Netzwerkmethode{#builduserauthtoken-network-method}

Gibt ein vom Benutzer authentifiziertes verschlüsseltes Token für das Netzwerk zurück, aus dem es aufgerufen wird.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| userId | Zeichenfolge | Die Benutzer-ID des Benutzers, dem dieses Token angehört. |
| displayName | Zeichenfolge | Der Anzeigename des Benutzers. |
| expires | Double | Wenn das Token in Sekunden abläuft. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Beispielausgabe:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Beispielausgabe:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

Beispielausgabe:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Python-Beispiel {#section_dwg_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Beispielausgabe:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Beispielausgabe:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
