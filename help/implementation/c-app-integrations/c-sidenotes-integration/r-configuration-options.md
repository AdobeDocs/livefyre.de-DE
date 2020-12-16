---
description: Das Config-Objekt "SiHiermit"ist ein JSON-Objekt, mit dem der von der Livefyre-App auf der Seite wiedergegebene Inhalt angegeben wird.
seo-description: Das Config-Objekt "SiHiermit"ist ein JSON-Objekt, mit dem der von der Livefyre-App auf der Seite wiedergegebene Inhalt angegeben wird.
seo-title: Sidebar-Konfigurationsoptionen
solution: Experience Manager
title: Sidebar-Konfigurationsoptionen
uuid: 067e51e6-9720-4226-a805-c7a07c8cdaa0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 2%

---


# Siegels-Konfigurationsoptionen{#sidenotes-configuration-options}

Das Config-Objekt &quot;SiHiermit&quot;ist ein JSON-Objekt, mit dem der von der Livefyre-App auf der Seite wiedergegebene Inhalt angegeben wird.

Das Objekt enthält die folgenden Parameter:

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| authDelegate | ** requirementsObject | Initialisierter Authentifizierungs-Delegate für neuen oder alten Stil. |
| collectionMeta | ** requirementsObject | Weitere Informationen finden Sie unter collectionMeta-Token. |
| customIcon | ** optionale Zeichenfolge | Legt die URL eines benutzerdefinierten Startersymbols fest. Der Standardwert ist Livefyre-Blase. |
| customStyles | *optionalobject*  | Fügt benutzerdefinierte Stile hinzu, um das Erscheinungsbild von Siegels zu ändern. Weitere Informationen finden Sie unter Benutzerdefinierte Stile. |
| disableStream | ** optionalBoolean | Wenn &quot;true&quot;, wird das Echtzeit-Streaming in dieser Instanz des Siegels deaktiviert (nicht in anderen Kommentarstreams). Standard ist „false“. |
| Umgebung | ** optionale Zeichenfolge | Gibt die Livefyre UAT-Umgebung an. Der einzige mögliche Wert ist `t402.livefyre.com`. Für die Produktion muss dieser Parameter entfernt werden. |
| iconVisibility | *optionales* Objekt oder Zeichenfolge | Legt fest, ob das Siegels-Symbol beim Bewegen des Mauszeigers oder bei einem statischen Symbol sichtbar sein soll. Wenn es sich um eine Zeichenfolge handelt, wird sie für beide Versionen des Blocksymbols verwendet (leer und hat Sir). Bei einem Objekt müssen Sie jeden Typ angeben: {leer: &quot;hover&quot;, num: &quot;statisch&quot;}. Die Standardeinstellung ist statisch. |
| inlineThreads | ** optional | Wenn &quot;true&quot;, werden Sidenote-Threads direkt nach dem Block eingefügt, mit dem sie verknüpft sind. Standard ist „false“. |
| numSigibtEl | *optionales* Objekt, String oder Array | Gibt an, welches Element das Widget &quot;Sikennzeichenanzahl&quot;verzieren soll. (Dieses Widget zeigt die Anzahl der Präsidentschaften auf der Seite und Informationen zu Siegels an.) Wenn der String-Selektor mit mehr als einem Element übereinstimmt, wird das erste Element ausgewählt. (Verwendet CSS3-DOM-Selektorspezifikationen.) |
| position | ** optionale Zeichenfolge | Bestimmt die Position des Popups, wenn auf ein Element geklickt wird, für das &quot;Siegels&quot;aktiviert ist. Mögliche Werte sind &quot;smart&quot;, &quot;left&quot;, &quot;right&quot;, &quot;bottom&quot;. Der Standardwert ist &quot;smart&quot;, wodurch das Popup rechts von der Seite ausgerichtet wird, es sei denn, es ist nicht genügend Platz vorhanden (in diesem Fall wird es unter den Inhalt verschoben). |
| Selektoren | ** requireObject, string oder array | Gibt die Elemente an, auf denen Startersymbole angezeigt werden sollen. (Verwendet CSS3-DOM-Selektorspezifikationen.) Enthält ein Objekt den Abschnitt &quot;Includes&quot;und den Abschnitt &quot;Ausschluss&quot;, der den CSS-Selektor auf alle übereinstimmenden Einschlüsse anwendet, und entfernt alle Elemente, die mit den Ausschlüssen übereinstimmen. Wenn eine Zeichenfolge vorhanden ist, werden alle passenden Elemente auf der Seite eingefügt. Bei Array werden die einzuschließenden Elemente Liste. |
| Strings | *optionalobject*  | Fügt benutzerdefinierte Textzeichenfolgen hinzu, um eine beliebige Sprache oder Text in der Anwendung zu ändern. Weitere Informationen finden Sie unter Benutzerdefinierte Zeichenfolgen. |
| threadContainerEl | *optionales* Objekt, String oder Array | Gibt ein Element an, in dem der Thread von &quot;sidences&quot;angezeigt wird. Mit diesem Parameter können Sie den Thread neu positionieren. Wenn der String-Selektor mit mehr als einem Element übereinstimmt, wird das erste Element ausgewählt. (Verwendet CSS3-DOM-Selektorspezifikationen.) |

