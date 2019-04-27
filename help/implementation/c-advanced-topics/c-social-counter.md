---
description: Zählen Sie die Anzahl der kuratierten sozialen Elemente.
seo-description: Zählen Sie die Anzahl der kuratierten sozialen Elemente.
seo-title: Social-Zähler
solution: Experience Manager
title: Social-Zähler
uuid: fa 9 aa 1 a 8-6 a 04-4 bc 1-9 bfe-e 42 c 1250 fd 48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Social-Zähler{#social-counter}

Zählen Sie die Anzahl der kuratierten sozialen Elemente. Eine vollständige Liste der verfügbaren Endpunkte finden Sie im Abschnitt &quot;Livefyre [-API-Referenz](https://api.livefyre.com/docs) &quot; .

Die Social-Zähler-API gibt in einer bestimmten Sammlung für Intervalle über einen bestimmten Zeitraum Zählungen für übereinstimmende Kuratierungsregeln zurück.

>[!NOTE]
>
>Diese API ist nur für Twitter-Hashtags verfügbar.

Social-Zähler-API:

* Ressource
* Regeltypen
* Antwort

## Ressource {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **Networkname:** Ihr Livefyre-bereitgestellter Netzwerkname. Beispiel: *in*`labs.fyre.co`.
* **Abfrage:** Der URL-sichere Base 64-kodierte Hash aller Site, Artikel-ID, Regeltyp-Tupel, für die Zählinformationen abgerufen werden sollen (vorkodiert)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >Die Abfrage ist auf 10 Site, Artikel-ID, Richtlinientypen für Regeln beschränkt. (Das vorherige Beispiel würde 3 Tupfel enthalten.)

* **gibt** `(optional)` den relativen oder absoluten Zeitraum für das Diagramm an. &quot; von&quot; gibt den Anfang und Standardwert vor 24 Stunden an, wenn nicht angegeben.
* **bis zur** `(optional)` Angabe des relativen oder absoluten Zeitraums zum Diagramm; bis zur Angabe des Beginns und der Standardeinstellung bis zur aktuellen Zeit (jetzt), wenn nicht angegeben.

### Relative Zeit

| Abkürzung | Einheit |
|---|---|
| s | Sekunden |
| min | Minuten |
| h | Stunden |
| d | Tage |
| w | Wochen |
| mo | 30 Tage (Monat) |
| y | 365 Tage (Jahr) |

Beispiel:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Absolute Zeit {#section_xqr_jgc_11b}

FORMAT: HH: MM_ YYYYMMDD

| Abkürzung | Bedeutung |
|---|---|
| HH | Stunden (im 24 h Uhrzeitformat) |
| MM | Minuten |
| YYYY | Vierstellige Jahreszahl |
| MM | Monat |
| DD | Tag |

Beispiel:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## Regeltypen {#section_v53_xqb_11b}

| Wert | Typ |
|---|---|
| 2 | Twitter |

Beispiel:

So erhalten Sie Zählungen über die letzte Minute für Site `123456` und Artikel-ID `some-article-id` und Regeltyp `2`, z. B.: `123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

Beispielantwort:

```
{ 
    "status": "ok", 
    "code": 200, 
    "data": { 
        "123456": { 
            "some-article-id": { 
                "2": [ 
                    [ 
                        2, 
                        1374770460 
                    ], 
                    [ 
                        4, 
                        1374770470 
                    ], 
                    [ 
                        3, 
                        1374770480 
                    ], 
                    [ 
                        1, 
                        1374770490 
                    ], 
                    [ 
                        0, 
                        1374770500 
                    ], 
                    [ 
                        7, 
                        1374770510 
                    ] 
                ] 
            } 
        } 
    } 
}
```
