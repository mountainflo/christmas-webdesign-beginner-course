# HTML, CSS und JavaScript lernen

**Kursbeschreibung:**

In diesem Kurs lernt ihr die Grundlagen zur Gestaltung einer Webseite.
Mit HTML, CSS und JavaScript bauen wir schöne weihnachtliche Webseiten. 

**Voraussetzungen:**

Account auf [https://repl.it/](https://repl.it/)

**Dokumentation:**

* Tutorials und Dokumentation zu HTML/CSS/JS: [https://wiki.selfhtml.org/wiki](https://wiki.selfhtml.org/wiki)
* Alle wichtigen HTML-Elemente: [https://wiki.selfhtml.org/wiki/HTML#Elemente](https://wiki.selfhtml.org/wiki/HTML#Elemente)
* Kurz und kompakt alle HTML-Befehle und CSS-Eigenschaften (auf Englisch): [https://www.w3schools.com/](https://www.w3schools.com/)
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

Du kannst den nachfolgenden HTML-Code für eine einfache Webseite in die Datei `index.html` einfügen.
Sobald du auf den grünen `Run`-Button geklickt hast, sollte auf der rechten Seite `Hallo Welt!` stehen.

```html
<!doctype html>
<html lang="de">
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
befindet sich der Titel der Webseite. Die *Tags* strukturieren die Webseite, damit der Browser weiß,
wie er den Text zwischen den Tags darstellen soll.

> Aufgabe: Welche weiteren Tags findest du noch im HTML-Code? Wo beginnen sie und werden sie wieder geschlossen?

Wie du siehst, muss ein geöffnetes Tag nicht gleich wieder geschlossen werden.
Innerhalb eines Tags können auch weitere neue Tags geöffnet werden.

#### Die wichtigsten Tags für deine erste Webseite

* `<html>` und `</html>`: Enthält den kompletten HTML-Code der Webseite.
* `<head>` und `</head>`: Enthält wichtige Metadaten, wie z.B. den Titel der Webseite oder später den Link zur CSS- und JS-Datei.
* `<title>` und `</title>`: Enthält den Titel der Webseite, der im Browsertab angezeigt wird. 
* `<body>` und `</body>`: Enthält den Text, der im Browser angezeigt wird.

> Aufgabe: Verändere den Titel oder den Body der Webseite und schau dir an was passiert, wenn du die Seite neu lädst.

### Erste Inhalte in deine Webseite einfügen

Vielleicht hast du bereits versucht ganze viele Leerzeichen hintereinander oder Leerzeilen einzufügen.
Dir wird aufgefallen sein, dass der Browser die Zeilenumbrüche ignoriert hat.
Als Nächstes verwenden wir deshalb das `<p>`-Tag. `<p>` steht für "paragraph" (Absatz).
Du kannst Texte zwischen `<p>`-Tags platzieren, um sie als eigenständigen Absatz darzustellen.
Zwischen zwei Absätzen wird automatisch ein Leerzeile als Abstand eingefügt.

Neben dem `<p>`-Tag für Absätze gibt es auch noch Tags für Überschriften.
Hier stehen dir insgesamt 6 verschiedene Überschriften (`<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`) zur Verfügung.
Vom `<h1>`-Tag der größten Überschrift, bis zu `<h6>`.

> Aufgabe: Verwende verschiedene Überschiften und platziere zwischen 2 Überschriften immer mindestens einen Absatz.
> Du musst dir keine Texte ausdenken, du kannst einfach irgendwelche Zeichenfolgen auf der Tastatur eintippen.
> Oder du lässt dir hier [https://www.loremipsum.de/](https://www.loremipsum.de/) etwas Beispieltext generieren.

### Bilder einfügen

Lass uns nun ein Bild in die Webseite einfügen. Für Bilder benötigst du wieder ein neues Tag, dass wie folgt aussieht:

```html
<img src="hacker-school.jpg" alt="Hacker School Logo" width="100px" />
```

`img` steht dabei für "image" (=Bild). Dieses Tag ist allerdings etwas anders als die bisherigen html-Tags.
Damit das Bild auch angezeigt wird werden zusätzlich noch sogenannte Attribute benötigt.
Ein Attribut für `src` (source), die Quelle, bzw. die Angabe des Ortes an dem die Bilddatei liegt.
Mit dem Attribut `alt` kannst du einen alternativen Text angeben. Dieser wird angezeigt, wenn das Bild mal aus technischen Problemen nicht geladen werden kann.
Mit `width` kannst du noch die Breite des Bildes ändern, ansonsten wird das Bild in der Originalgröße angezeigt.
Alternativ kannst du auch die Höhe mit `height` setzen. Es reicht aber eine Angabe, die andere ergibt sich automatisch
aus den Proportionen deines Bildes.

> Aufgabe: Gehe auf die Seite [https://unsplash.com/](https://unsplash.com/) und lade dir ein frei nutzbares Bild herunter.
> Lade das Bild anschließend in dein repl-Projekt. Am besten du legst dafür einen eigenen Ordner für Bilder an.
> Anschließend fügst du das `<img>`-Tag in deine Webseite ein und passt alle für das `<img>`-Tag notwendigen Attribute an.
> Achte darauf, wenn du das Bild in einen Ordner legst, auch den Namen des Ordners anzugeben (z. B. `src="images/hello.jpg"`),
> wenn sich das Bild im Ordner `images` befindet.

### Links einfügen und Seiten untereinander verlinken

Lass uns nun das Element einfügen, ohne das keine Webseite auskommt: Links. Für Links brauchst du das `<a>`-Tag.

```html
Viel Spaß mit dem <a href="advents-calender.html">Online-Adventskalender</a> von der Hacker School.
```

Alles was zwischen dem öffnenden und schließenden Tag steht, wird zu einem Link.
Wie bei den Bildern hat das `<a>`-Tag noch weitere Attribute.
Das Link-Ziel wird mit dem Attribut `href` definiert. Im obigen Beispiel würde der Browser zur Seite `advents-calender.html`
springen, sobald jemand auf den Linktext `Online-Adventskalender` klickt.

> Aufgabe: Erstelle in repl eine zweite html-Seite. Baue in der ersten Seite einen Link ein, der auf die zweite Seite verweist.
> In der neu erstellten, zweiten html-Seite fügst du auch einen Link ein, mit dem wieder zurück zur Startseite gesprungen werden kann.

Mit dem `<a>`-Tag kannst du auch Links zu anderen Webseiten erstellen, z. B. zu deinem Instagram Account.
Für die Hackerschool würde der Link wie folgt aussehen:

```html
<a href="https://www.instagram.com/hckr_schl/">Hacker School Instagram</a>
``` 

### Container/Boxen verwenden

`<div>` (engl. "division" für Abteilung/Bereich)


## CSS

TODO:
* Browser Inspection
* container with margin, border and padding (maybe not so many details, only the important things)
* units (em, px) and what the difference is
