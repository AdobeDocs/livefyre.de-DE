---
description: Zählen Sie die Anzahl der kuratierten sozialen Elemente.
seo-description: Zählen Sie die Anzahl der kuratierten sozialen Elemente.
seo-title: Social-Zähler
solution: Experience Manager
title: Social-Zähler
uuid: fa9aa1a8-6a04-4bc1-9bfe-e42c1250fd48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Social-Zähler{#social-counter}

Zählen Sie die Anzahl der kuratierten sozialen Elemente. Eine vollständige Liste der verfügbaren Endpunkte finden Sie im Abschnitt zur Livefyre- [API-Referenz](https://api.livefyre.com/docs) .

Die Social-Zähler-API gibt für eine bestimmte Sammlung für Intervalle über einen bestimmten Zeitraum Zählungen für übereinstimmende Kurationsregeln zurück.

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

* **** networkName:Ihr Livefyre hat den Netzwerknamen angegeben. Beispiel: *Laboratorien* in `labs.fyre.co`.
* **** query: Der url-sichere base64-kodierte Hash aller Seiten, Artikel-ID- und Regeltypen, für die Zählungsinformationen abgerufen werden sollen (vorkodiert)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >Die Abfrage ist auf 10 Site-, Artikel-ID-, Regel-Typ-Tupel beschränkt. (Das vorherige Beispiel würde 3 Tupel enthalten.)

* **from** gibt den relativen oder absoluten Zeitraum bis zum Diagramm an `(optional)` ; from gibt den Anfang an und ist standardmäßig auf vor 24 Stunden eingestellt, wenn kein Wert angegeben wird.
* **bis** `(optional)` der relative oder absolute Zeitraum für das Diagramm angegeben ist; bis gibt den Anfang an und standardmäßig die aktuelle Zeit (jetzt) an, falls nicht angegeben.

### Relative Zeit

| Abkürzung | Einheit |
|---|---|
| s- | Sekunden |
| min | Minuten |
| h | Stunden |
| d | Tage |
| w | Wochen |
| mon | 30 Tage (Monat) |
| y | 365 Tage (Jahr) |

Beispiel:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Absolute Zeit {#section_xqr_jgc_11b}

FORMAT: HH:MM_JJJMMTT

| Abkürzung | Beschreibung |
|---|---|
| HH | Stunden (im 24-Stunden-Format) |
| MM | Minuten |
| YYYY | 4-stelliges Jahr |
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

So erhalten Sie Zählungen über die letzte Minute für die Site- `123456` und Artikel-ID `some-article-id` und den Regeltyp `2`, z. B.: `123456:some-article-id;2:`

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
