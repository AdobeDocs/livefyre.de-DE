---
description: Gibt ein verschlüsseltes benutzerauthentifiziertes Token für das Netzwerk
  zurück, von dem es aufgerufen wird.
seo-description: Gibt ein verschlüsseltes benutzerauthentifiziertes Token für das
  Netzwerk zurück, von dem es aufgerufen wird.
seo-title: Builduserauthtoken Network-Methode
solution: Experience Manager
title: Builduserauthtoken Network-Methode
uuid: 8828 d 356-c 3 c 6-46 a 6-91 bf -83 bd 59 e 35050
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Builduserauthtoken Network-Methode{#builduserauthtoken-network-method}

Gibt ein verschlüsseltes benutzerauthentifiziertes Token für das Netzwerk zurück, von dem es aufgerufen wird.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| Userid | Zeichenfolge | Die Benutzer-ID für den Benutzer, zu dem dieses Token gehört. |
| Displayname | Zeichenfolge | Der Anzeigename für den Benutzer. |
| läuft ab | Double | Wenn das Token in Sekunden ablaufen soll. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Beispielausgabe:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

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

## Python Example {#section_dwg_gds_rz}

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
