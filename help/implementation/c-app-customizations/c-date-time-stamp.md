---
description: Passen Sie Datums- und Uhrzeitstempel mit Livefyre.js an.
title: Anpassen des Datums- und Uhrzeitstempels
exl-id: 77130793-00ba-4a5c-8318-4221d971da6c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---

# Anpassen des Datums- und Uhrzeitstempels{#customize-the-date-and-time-stamp}

Passen Sie Datums- und Uhrzeitstempel mit Livefyre.js an.

Livefyre-Apps bieten den Optionsparameter datetimeFormat, um das Datumsformat wie unten beschrieben anzugeben.

* [Terminologie](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formatierung](#c_date_time_stamp/section_ynx_gn4_xz)
* [Symbolbezeichnung](#c_date_time_stamp/section_inq_2n4_xz)

## Terminologie {#section_xsk_jn4_xz}

* **Absolute** Zeitstempel werden als genaue und spezifische Zeiten definiert (z. B. 1. Januar 2012, 12:00 Uhr)
* **Relative** Zeitstempel werden als allgemeine und weniger präzise Zeiten definiert (z. B. vor 25 Sekunden, vor 14 Minuten, vor 1 Tag, vor einem Jahr usw.)

## Formatieren {#section_ynx_gn4_xz}

Der Parameter datetimeFormat hat das folgende Standardverhalten, wenn kein Argument angegeben wird:

* Datumsformat von: MMMM JJJJ (8. Januar 2012)
* 20160 Minuten (14 Tage) bis zur absoluten Zeit (14 Tage, bis relative Zeitstempel zu absoluten Zeitstempeln werden)

Der Parameter datetimeFormat akzeptiert drei mögliche Argumenttypen: datetime, format und string.

```
// Example 1 (Datetime format string)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": 'MMM d y Ka' 
}; 
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Ein Objekt, das absoluteFormat und/oder minutesBeforeAbsoluteTime angibt. Eine minuteToAbsoluteTime mit dem Wert -1 macht die absolute Zeit sofort.

```
// Example 2 (Object)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": { 
      minutesUntilAbsoluteTime: 10, 
      absoluteFormat: 'MMM d y Ka' 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Eine Funktion, die ein Date-Objekt als Argument akzeptiert und eine anzuzeigende Datums-Uhrzeit-Zeichenfolge zurückgibt

```
// Example 3 (Function accepting a Date object, returning a datetime string to display) 
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": function(theDateInput) { 
      return +theDateInput; 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

## Symbolbezeichnung {#section_inq_2n4_xz}

Die Formatierungsfunktionen für die Datenzeit folgen der Musterspezifikation, wie in JDK, ICU und CLDR definiert, mit geringfügigen Änderungen für die typische Verwendung in JS. Weitere Informationen finden Sie unter [Google Closure Library Documentation](https://developers.google.com/closure/library/docs/overview).

```
  Symbol Meaning Presentation        Example 
  ------   -------                 ------------        ------- 
  G        era designator          (Text)              AD 
  y#       year                    (Number)            1996 
  Y* year (week of year)     (Number)            1997 
  u* extended year           (Number)            4601 
  M        month in year           (Text & Number)     July & 07 
  d        day in month            (Number)            10 
  h        hour in am/pm (1~12)    (Number)            12 
  H        hour in day (0~23)      (Number)            0 
  m        minute in hour          (Number)            30 
  s        second in minute        (Number)            55 
  S        fractional second       (Number)            978 
  E        day of week             (Text)              Tuesday 
  e* day of week (local 1~7) (Number)            2 
  D* day in year             (Number)            189 
  F* day of week in month    (Number)            2 (2nd Wed in July) 
  w* week in year            (Number)            27 
  W* week in month           (Number)            2 
  a        am/pm marker            (Text)              PM 
  k        hour in day (1~24)      (Number)            24 
  K        hour in am/pm (0~11)    (Number)            0 
  z        time zone               (Text)              Pacific Standard Time 
  Z        time zone (RFC 822)     (Number)            -0800 
  v        time zone (generic)     (Text)              Pacific Time 
  g* Julian day              (Number)            2451334 
  A* milliseconds in day     (Number)            69540000 
  '        escape for text         (Delimiter)         'Date=' 
  ''       single quote            (Literal)           'o''clock'
```

Mit &quot;*&quot;markierte Elemente werden noch nicht unterstützt.

Mit &quot;#&quot;markierte Elemente funktionieren anders als Java.

Das Format wird durch die Anzahl der Musterbuchstaben bestimmt.

* **Text:** 4 oder mehr, vollständiges Formular verwenden. Verwenden Sie weniger als 4, wenn vorhanden, ein kurzes oder abgekürztes Formular. (Beispiel: &quot;EEEE&quot;produziert &quot;Montag&quot;, &quot;EEE&quot;produziert &quot;Mon&quot;.)
* **Zahl:** die Mindestanzahl der Ziffern. Kürzere Zahlen werden diesem Betrag Null hinzugefügt (Beispiel: Wenn &quot;m&quot;&quot;6&quot;ergibt, erzeugt &quot;mm&quot;&quot;06&quot;.) Jahr wird besonders behandelt; Wenn also &quot;y&quot;gleich 2 ist, wird das Jahr auf 2 Stellen gekürzt. (Beispiel: Wenn &quot;yyyy&quot;den Wert &quot;1997&quot;ergibt, erzeugt &quot;yy&quot;den Wert &quot;97&quot;.) Im Gegensatz zu anderen Feldern werden auf der rechten Seite Bruchteile mit Null aufgefüllt.
* **Text und Zahl:** 3 oder höher, verwenden Sie Text. Weniger als 3, Nummer verwenden. (Beispiel: &quot;M&quot;erzeugt &quot;1&quot;, &quot;MM&quot;produziert &quot;01&quot;, &quot;MMM&quot;produziert &quot;Jan&quot;, und &quot;MMMM&quot;produziert &quot;Januar&quot;.)

Alle Zeichen im Muster, die sich nicht in den Bereichen von [&quot;a&quot;befinden.&quot;z&quot;] und [&quot;A&quot;..&quot;Z’] wird als zitierter Text behandelt. Zeichen wie &quot;:&quot;, &quot;.&quot;, &quot;, &quot;#&quot;und &quot;@&quot;werden im resultierenden Zeittext angezeigt, auch wenn sie nicht in einfache Anführungszeichen gesetzt werden.
