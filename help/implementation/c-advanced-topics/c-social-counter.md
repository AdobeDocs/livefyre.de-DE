---
description: Zählen Sie die Anzahl der kuratierten sozialen Elemente.
title: Social-Zähler
exl-id: def7fba4-1c2e-4c7b-84f7-f9ede592d675
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 10%

---

# Social-Zähler{#social-counter}

Zählen Sie die Anzahl der kuratierten sozialen Elemente. Eine vollständige Liste der verfügbaren Endpunkte finden Sie im Abschnitt Livefyre [API-Referenz](https://api.livefyre.com/docs).

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

* **networkName:** Ihr Livefyre-Netzwerkname. Beispiel: *labs* in `labs.fyre.co`.
* **Abfrage:** Der url-sichere base64-kodierte Hash aller Seiten, Artikel-ID- und Regeltypen, für die Zählungsinformationen abgerufen werden sollen (vorkodiert)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >Die Abfrage ist auf 10 Site-, Artikel-ID- und Regeltypen beschränkt. (Das vorherige Beispiel würde 3 Tupel enthalten.)

* **&quot;** `(optional)` form&quot;gibt den relativen oder absoluten Zeitraum für das Diagramm an; from gibt den Anfang an und ist standardmäßig auf vor 24 Stunden eingestellt, wenn kein Wert angegeben wird.
* **gibt** `(optional)` nicht den relativen oder absoluten Zeitraum für das Diagramm an; bis gibt den Anfang an und standardmäßig die aktuelle Zeit (jetzt) an, wenn kein Wert angegeben wird.

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
