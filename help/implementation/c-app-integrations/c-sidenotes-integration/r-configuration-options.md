---
description: Das Confiotes-Konfigurationsobjekt ist ein JSON-Objekt, mit dem der Inhalt
  angegeben wird, den die Livefyre-App auf der Seite wiedergibt.
seo-description: Das Confiotes-Konfigurationsobjekt ist ein JSON-Objekt, mit dem der
  Inhalt angegeben wird, den die Livefyre-App auf der Seite wiedergibt.
seo-title: Optionen für die Konfiguration von Gruppen
solution: Experience Manager
title: Optionen für die Konfiguration von Gruppen
uuid: 067 e 51 e 6-9720-4226-a 805-c 7 a 07 c 8 cdaa 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Optionen für die Konfiguration von Gruppen{#sidenotes-configuration-options}

Das Confiotes-Konfigurationsobjekt ist ein JSON-Objekt, mit dem der Inhalt angegeben wird, den die Livefyre-App auf der Seite wiedergibt.

Das Objekt enthält die folgenden Parameter:

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| Authdelegate | *Erforderliches* Objekt | Neue oder alte Stilisierungsdelegierungsupdate. |
| Collectionmeta | *Erforderliches* Objekt | Weitere Informationen finden Sie unter collectionmeta-Token. |
| Customicon | *optionale* Zeichenfolge | Legt die URL eines benutzerdefinierten Starter-Symbols fest. Die Standardeinstellung ist "Livefyre-Bubble" . |
| Customstyles | *Optionales* Objekt | Fügt benutzerdefinierte Stile hinzu, um das Erscheinungsbild von Sidenotes zu ändern. Weitere Informationen finden Sie unter Benutzerdefinierte Stile. |
| Disablestream | *Optionales* Boolescher Wert | Wenn "true" , wird das Echtzeit-Streaming in dieser" Sidenotes" -Instanz deaktiviert (nicht in anderen Kommentarstreams). Der Standardwert ist "false" . |
| Umgebung | *optionale* Zeichenfolge | Gibt die Livefyre-UIN-Umgebung an. Der einzige mögliche Wert `t402.livefyre.com`ist. Für die Produktion muss dieser Parameter entfernt werden. |
| Iconvisibility | *optionales* Objekt oder eine optionale Zeichenfolge | Definiert, ob das Symbol "Sidenotes" beim Mauszeiger oder statisch sichtbar ist. Ist dies eine Zeichenfolge, wird sie für beide Versionen des Blocksymbols verwendet (leer und hat "Sidenotes" ). Bei einem Objekt müssen Sie jeden Typ angeben: {empty: ' hover ', num: ' static '}. Der Standardwert ist statisch. |
| Inlinethreads | *Optionales* Boolesches Zeichen | Wenn "true" , werden Mohamote threads direkt nach dem Block eingefügt, mit dem sie verknüpft sind. Der Standardwert ist "false" . |
| Numsidenotesel | *optionales* Objekt, Zeichenfolge oder Array | Gibt an, welches Element das Widget "Sidenotes" dekorieren soll. (Dieses Widget zeigt die Anzahl der Follower auf der Seite und Informationen zu den Autoren.) Wenn die Zeichenfolgenauswahl mehr als ein Element entspricht, wird das erste Element ausgewählt. (Verwendet CSS 3 DOM Selector spec.) |
| position | *optionale* Zeichenfolge | Legt die Position des Popupfensters fest, wenn auf ein Element geklickt wird, auf das die "Sidenotes" aktiviert ist. Mögliche Werte sind "smart" ," left" , "right" und" bottom" . Der Standardwert ist "smart" , der das Popup rechts von der Seite ausrichten wird, sofern nicht ausreichend Leerzeichen vorhanden sind (in diesem Fall wird er unter den Inhalt verschoben). |
| Selektoren | *Erforderliches* Objekt, Zeichenfolge oder Array | Gibt die Elemente an, auf denen Starter-Symbole angezeigt werden sollen. (Verwendet CSS 3 DOM Selector spec.) Wenn das Objekt den Abschnitt "enthält" enthält und der Abschnitt" Schließt" den CSS-Selektor für jede Übereinstimmung anwendet, und entfernen Sie alle Elemente, die den Ausschluss-Elementen entsprechen. Bei der Zeichenfolge werden alle übereinstimmenden Elemente auf der Seite eingeschlossen. Wenn Array, werden die einzuschließenden Elemente aufgelistet. |
| Zeichenfolgen | *Optionales* Objekt | Fügt benutzerdefinierte Textzeichenfolgen hinzu, um eine Sprache oder einen Text in der gesamten Anwendung zu ändern. Weitere Informationen finden Sie unter Benutzerdefinierte Zeichenfolgen. |
| Threadcontainerel | *optionales* Objekt, Zeichenfolge oder Array | Gibt ein Element an, in dem der Thread-Thread angezeigt wird. Mit diesem Parameter können Sie den Thread neu positionieren. Wenn die Zeichenfolgenauswahl mehr als ein Element entspricht, wird das erste Element ausgewählt. (Verwendet CSS 3 DOM Selector spec.) |

