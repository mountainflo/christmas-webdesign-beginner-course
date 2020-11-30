# HTML, CSS und JavaScript lernen

**Kursbeschreibung:**

In diesem Kurs lernt ihr die Grundlagen zur Gestaltung einer Webseite.
Mit HTML, CSS und JavaScript bauen wir schöne weihnachtliche Webseiten. 

**Voraussetzungen:**

Account auf [https://repl.it/](https://repl.it/)

**Dokumentation:**

* Tutorials und Dokumentation zu HTML/CSS/JS: [https://wiki.selfhtml.org/wiki](https://wiki.selfhtml.org/wiki)
* Alle wichtigen HTML-Elemente: [https://wiki.selfhtml.org/wiki/HTML#Elemente](https://wiki.selfhtml.org/wiki/HTML#Elemente)
* Kurz und kompat alle HTML-Befehle und CSS-Eigenschaften (auf Englisch): [https://www.w3schools.com/](https://www.w3schools.com/)
    * CSS-Referenz: [https://www.w3schools.com/cssref](https://www.w3schools.com/cssref)
    * HTML-Referenz: [https://www.w3schools.com/tags](https://www.w3schools.com/tags)
    
* Tolle Projektideen für HTML und CSS vom Code-Club der Raspberrypi-Foundation mit Schritt-für-Schritt Anleitungen (auf Englisch):
    * [HTML & CSS: Module 1](https://projects.raspberrypi.org/en/codeclub/webdev-module-1)
    * [HTML & CSS: Module 2](https://projects.raspberrypi.org/en/codeclub/webdev-module-2)

## HTML

Um deine eigene Webseite zu bauen braucht es nicht viel. Es genügt ein einfacher Texteditor und ein Browser.
Erstelle als erstes eine neue Datei im Texteditor oder auf [https://repl.it/](https://repl.it/) mit der Endung `.html`.

Wenn du auf `repl.it` arbeitest, wählst du als Sprache `HTML, CSS, JS` aus.
Den in der Datei `index.html` enthaltenen Code kannst du löschen, da wir komplett von vorne anfangen mit der Erstellung einer Webseite.
In `repl.it` siehst du links alle deine standardmäßig erstellten Dateien (`index.html`, `script.js`, `style.css`).
In der Mitte siehst du den Code der aktuell geöffneten Datei. 
Ein Browser kann diesen Code lesen und dir daraus eine schöne Webseite generieren, wie sie auf der rechten Seite zusehen ist.
Die Ansicht auf der rechten Seite wird aktualisiert, sobald du auf den grünen `Run`-Button oben in der Mitte geklickt hast.

### Grundgerüst einer HTML-Seite

Du kannst du den nachfolgenden HTML-Code für eine einfache Webseite in die Datei `index.html` einfügen.
Sobald du auf den grünen `Run`-Button geklickt hast, sollte auf der rechten Seite `Hallo Welt!` stehen.

```html
<!doctype html> <!--TODO doctype weglassen oder noch erklären-->
<html lang="de"> <!--TODO lang weglassen oder noch erklären-->
  <head>
    <title>Titel der Webseite</title>
  </head>
  <body>
    Hallo Welt!
  </body>
</html>
```

Schauen wir uns nun den HTML-Code genauer an. HTML verwendet sogenannte *Tags*, mit denen die Webseite aufgebaut wird.
Ein Tag wäre zum Beispiel `<title>`. Zwischen den zwei `title`-Tags, dem öffnenden `<title>` und dem schließenden `</title>`
befindet sich der Titel der Webseite. Die *Tags* strukturieren die Webseite und der Browser weiß dadurch,
wie er den Text zwischen zwei Tags darstellen soll.

> Aufgabe: Welche weiteren Tags findest du noch im HTML-Code? Wo beginnen sie und werden sie wieder geschlossen?

Wie du siehst, muss ein geöffnetes Tag nicht gleich wieder geschlossen werden.
Innerhalb eines Tags können auch weitere neue Tags geöffnet werden.

#### Die wichtigsten Tags für deine erste Webseite

* `<html>` und `</html>`: Enthält die komplette den kompletten HTML-Code der Webseite.
* `<head>` und `</head>`: Enthält wichtige Metadaten, wie z.B. den Titel der Webseite oder später der Link zur CSS- und JS-Datei.
* `<title>` und `</title>`: Enthält den Titel der Webseite, der im Browsertab angezeigt wird. 
* `<body>` und `</body>`: Enthält den Text, der im Browser angezeigt wird.

> Aufgabe: Verändere den Titel oder den Body der Webseite und schau dir an was passiert, wenn du die Seite neu lädst.

### Erste Inhalte in deine Webseite einfügen



## CSS

TODO:
* Browser Inspection
* container with margin, border and padding (maybe not so many details, only the important things)
* units (em, px) and what the difference is
