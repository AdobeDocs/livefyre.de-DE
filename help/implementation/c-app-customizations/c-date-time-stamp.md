---
description: Datum und Zeitstempel mit Livefyre. js anpassen.
seo-description: Datum und Zeitstempel mit Livefyre. js anpassen.
seo-title: Datum und Zeitstempel anpassen
solution: Experience Manager
title: Datum und Zeitstempel anpassen
uuid: 632 ea 405-56 b 7-4664-8 d 2 b -0 dd 0 a 7611 bd 8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Datum und Zeitstempel anpassen{#customize-the-date-and-time-stamp}

Datum und Zeitstempel mit Livefyre. js anpassen.

Livefyre-Apps geben den opetimeformat-Parameter &quot;datetimeformat&quot; an, um das Datumsformat anzugeben, wie nachfolgend beschrieben.

* [Terminologie](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formatierung](#c_date_time_stamp/section_ynx_gn4_xz)
* [Symbolbenennung](#c_date_time_stamp/section_inq_2n4_xz)

## Terminologie {#section_xsk_jn4_xz}

* **Absolute Zeitstempel** werden als exakt und spezifische Zeiten definiert (z. B. 1. Januar 2012 214:00 Uhr)
* **Relative Zeitstempel** werden als allgemein und weniger genau definiert (vor 25 Minuten, vor 14 Minuten, vor 1 Jahr usw.)

## Formatierung {#section_ynx_gn4_xz}

Der datetimeformat-Parameter hat das folgende Standardverhalten, wenn kein Argument angegeben wird:

* Dateuhrzeitformat von: MMMM yyyy (für den 8. Januar 2012)
* 20160 Minuten (14 Tage) bis absolute Zeit (14 Tage bis zur absoluten Zeitstempel)

Der datetimeformat-Parameter akzeptiert drei mögliche Argumenttypen: datetime, format und string.

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

Ein Objekt, das absoluteformat und/oder minutesuntilabsolutetime angibt. Eine minutesuntilabsolutetime mit dem Wert -1 macht die Zeit sofort sofort.

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

Eine Funktion, die als Argument ein Date-Objekt akzeptiert und eine Datums-Uhrzeit-Zeichenfolge zurückgibt, die angezeigt werden soll

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

## Symbolbenennung {#section_inq_2n4_xz}

Funktionen für die Datumsformatierung folgen der Musterspezifikation gemäß der Definition in JDK, ICU und CLDR mit geringfügigen Änderungen in der JS-Nutzung. Weitere Informationen finden Sie in der [Google-Abschlussbibliotheksdokumentation](https://developers.google.com/closure/library/docs/overview).

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

Mit &#39; *&#39; markierte Elemente werden noch nicht unterstützt.

Mit &#39; #&#39; markierte Elemente unterscheiden sich anders als Java.

Die Anzahl der Musterbuchstaben bestimmt das Format.

* **Text:** 4 oder mehr, verwenden Sie das vollständige Formular. Weniger als 4, verwenden Sie kurze oder abgekürzte Formulare, wenn sie vorhanden sind. (Beispiel: &quot; EEEE&quot; erzeugt &quot;Montag&quot; ,&quot; EEE&quot; erzeugt &quot;Mo&quot; .)
* **Nummer:** die Mindestanzahl an Stellen. Kürzere Zahlen werden mit 0 aufgefüllt (z. B.: Wenn &quot;m&quot; den Wert&quot; 6&quot; ergibt, erzeugt &quot;mm&quot; den Wert&quot; 06&quot; .) Jahr wird speziell verarbeitet; das heißt, wenn die Anzahl von&#39;y &#39; 2 beträgt, wird das Jahr auf 2 Stellen gekürzt. (Beispiel: wenn &quot;yyyy&quot; &quot; 1997&quot; ergibt, erzeugt &quot;yy&quot; &quot; 97&quot; .) Im Gegensatz zu anderen Feldern werden die Bruchteile auf der rechten Seite mit null aufgefüllt.
* **Text &amp; Nummer:** 3 oder darüber, verwenden Sie Text. Weniger als 3, verwenden Sie die Nummer. (Beispiel: &quot; M&quot; erzeugt &quot;1&quot; ,&quot; MM&quot; erzeugt &quot;01&quot; ,&quot; MMM&quot; erzeugt &quot;Jan&quot; und&quot; MMMM&quot; erzeugt &quot;Januar&quot; .)

Alle Zeichen im Muster, die sich nicht in den Bereichen [&quot;a&quot; befinden. &#39;z&#39;] und [&#39;A &#39;. &#39;Z&#39;] wird als benannter Text behandelt. Beispielsweise Zeichen wie &#39;: &#39;,&#39;. &#39;,&#39;&#39;,&#39; #&#39; und &#39; @&#39; werden im resultierenden Zeittext angezeigt, auch wenn sie nicht innerhalb von einfachen Anführungszeichen stehen.
