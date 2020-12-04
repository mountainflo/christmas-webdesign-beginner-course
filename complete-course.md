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

> **Aufgabe:** Welche weiteren Tags findest du noch im HTML-Code? Wo beginnen sie und werden sie wieder geschlossen?

Wie du siehst, muss ein geöffnetes Tag nicht gleich wieder geschlossen werden.
Innerhalb eines Tags können auch weitere neue Tags geöffnet werden.

#### Die wichtigsten Tags für deine erste Webseite

* `<html>` und `</html>`: Enthält den kompletten HTML-Code der Webseite.
* `<head>` und `</head>`: Enthält wichtige Metadaten, wie z.B. den Titel der Webseite oder später den Link zur CSS- und JS-Datei.
* `<title>` und `</title>`: Enthält den Titel der Webseite, der im Browsertab angezeigt wird. 
* `<body>` und `</body>`: Enthält den Text, der im Browser angezeigt wird.

> **Aufgabe:** Verändere den Titel oder den Body der Webseite und schau dir an was passiert, wenn du die Seite neu lädst.

### Erste Inhalte in deine Webseite einfügen

Vielleicht hast du bereits versucht ganze viele Leerzeichen hintereinander oder Leerzeilen einzufügen.
Dir wird aufgefallen sein, dass der Browser die Zeilenumbrüche ignoriert hat.
Als Nächstes verwenden wir deshalb das `<p>`-Tag. `<p>` steht für "paragraph" (Absatz).
Du kannst Texte zwischen `<p>`-Tags platzieren, um sie als eigenständigen Absatz darzustellen.
Zwischen zwei Absätzen wird automatisch ein Leerzeile als Abstand eingefügt.

Neben dem `<p>`-Tag für Absätze gibt es auch noch Tags für Überschriften.
Hier stehen dir insgesamt 6 verschiedene Überschriften (`<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`) zur Verfügung.
Vom `<h1>`-Tag der größten Überschrift, bis zu `<h6>`.

> **Aufgabe:** Verwende verschiedene Überschriften und platziere zwischen 2 Überschriften immer mindestens einen Absatz.
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

> **Aufgabe:** Gehe auf die Seite [https://unsplash.com/](https://unsplash.com/) und lade dir ein frei nutzbares Bild herunter.
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

> **Aufgabe:** Erstelle in repl eine zweite html-Seite. Baue in der ersten Seite einen Link ein, der auf die zweite Seite verweist.
> In der neu erstellten, zweiten html-Seite fügst du auch einen Link ein, mit dem wieder zurück zur Startseite gesprungen werden kann.

Mit dem `<a>`-Tag kannst du auch Links zu anderen Webseiten erstellen, z. B. zu deinem Instagram Account.
Für die Hackerschool würde der Link wie folgt aussehen:

```html
<a href="https://www.instagram.com/hckr_schl/">Hacker School Instagram</a>
``` 

## CSS (Cascading Style Sheets)

Du hast dich wahrscheinlich schon die seit einiger Zeit gefragt, wie kann die Webseite jetzt noch schön bunt gestaltet werden.
HTML ist nur für die Strukturierung der Inhalte zuständig. Um die Inhalte schön bunt zu gestalten brauchen wir CSS.
Der Inhalt und das Design der Webseite sind somit voneinander getrennt. Sinn dahinter ist, dass es eine CSS-Datei gibt,
die in mehreren HTML-Seiten verwendet wird. Die Inhalte ändern sich über die einzelnen HTML-Seiten, aber das Design bleibt
für die gesamte Webseite mit allen Unterseiten gleich.
Mit CSS kannst du Abstände definieren, Schriftgrößen/Schriftarten ändern, Farben anpassen und vieles mehr.

### Link zu einer CSS-Datei einfügen

Idealerweise befinden sich alle CSS-Formatierungen in einer separaten Datei, die mit `.css` endet.
Den Link zur CSS-Datei musst du in den Header deiner HTML-Datei einfügen (siehe nachfolgendes Beispiel).

```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```

Du kannst einen ersten Test vornehmen, ob dein Browser die CSS-Datei auch wirklich findet.
Schreibe dazu in deine CSS-Datei folgenden Code und lade die HTML-Seite anschließend neu.
Der Hintergrund deiner Seite sollte danach komplett gelb sein.

```css
body {
    background-color: yellow;
}
```

### Texte formatieren

Im vorherigen Abschnitt hast du bereits gesehen, wie mit CSS Formatierungen vorgenommen werden.
Das Schema ist immer das gleiche. Zuerst gibst du den HTML-Tag an, den du mit CSS verändern möchtest.
Anschließend folgen in geschweiften Klammern die einzelnen Formatierungen.
Jede Formatierung besteht aus einer Eigenschaft (z.B. Farbe, Schriftart) und einem Wert (z.B. blau, Arial).
Eigenschaft und Wert sind durch einen Doppelpunkt `:` getrennt und werden mit einem Semikolon `;` abgeschlossen.

```
HTML-TAG {
    EIGENSCHAFT-1: WERT;
    EIGENSCHAFT-2: WERT;
    EIGENSCHAFT-3: WERT;
}
``` 

Lass uns nun ein Beispiel für eine CSS-Definition anschauen und welche Eigenschaften zur Verfügung stehen.
Keine Sorge, du musst die einzelnen Eigenschaften nicht auswendig können.
Du kannst jeder Zeit im Cheatsheet nachschauen, das wir dir zu Beginn gegeben haben.
Oder schaust z. B. auf der Webseite [https://www.w3schools.com/cssref](https://www.w3schools.com/cssref) nach.

Deine Webseite sollte noch aus einer der vorherigen Aufgaben `<p>`-Tags und diverse html-Überschriften enthalten.
Die Formatierung der Absätze und Überschriften möchten wir nun mit CSS verändern.
Füge dazu für den `<h1>`-Tag die folgenden CSS-Eigenschaften ein.

```css
h1 {
    color: red;                 // Farbe: z.B. blue, yellow, green, ...
    text-align: center;         // Ausrichtung: Der Absatz wird zentriert ausgerichtet
    font-family: sans-serif;    // Schriftart: sans-serif oder serif
}
p {
    color: blue;                // Farbe
    text-align: left;           // Ausrichtung: Der Absatz wird linksbündig ausgerichtet
}
```

### CSS Eigenschaften

Hier nun eine Übersicht der wichtigsten CSS-Eigenschaften.
Das tolle bei der Gestaltung von Webseiten mit HTML und CSS ist, du kannst die Gestaltung verändern und siehst sofort das Resultat.
Probiere eine CSS-Eigenschaft aus und lade die HTML-Seite neu. Verändere den Wert der Eigenschaft und lade erneut die HTML-Seite.

#### Schriftformatierung

*Schriftgröße:* (`font-size: 1em`)
Mit `font-size` definierst du die Schriftgröße. `1em` entspricht dabei der normalen Schriftgröße im Browser.
Soll der Text kleiner verwenden kannst du z.B. `0.8em` oder `0.75em` verwenden. 
Für Überschriften verwendest du Schriftgrößen wie `2em`, `3em` oder `4em`.
Probiere einfach aus, mit welcher Schriftgröße die am besten gefällt bist.

*Schriftart:* (`font-family: sans-serif`)
Für die Schriftart gibt es `sans-serif` (z. B. für Überschriften) und `serif` (z. B. für Fließtexte).

*Fett/Bold:* (`font-weight: bold`)

*Kursiv/Italic:* (`font-weight: italic`)

*Farbe:* (`color: red`)
Du kannst für die Farbe folgende bekannte Farben werden:
`pink`, `red`, `orange`, `yellow`, `gold`, `brown`, `olive`, `green`, `cyan`, `blue`, `violet`, `magenta`, `purple`, `white`, `black`

*Textausrichtung:* (`text-align: left`)
Die Textausrichtung ist standardmäßig linksbündig (`left`). Es gibt aber noch rechtsbündig (`right`) und zentriert (`center`).

#### Außenabstände (margin)

Für Texte (`p`), Überschriften (`h1`, `h2`, ...) aber auch für Bilder (`img`) kannst du Abstände angeben.
Es gibt einen Abstand nach oben (`margin-top`), nach unten (`margin-bottom`), sowie nach links (`margin-left`) und nach rechts (`margin-right`).
Die Abstände kannst du auch in der Einheit `em` angeben.

`````css
p {
    margin-top: 1.5em;
    margin-left: 3em;
}
`````

> **Aufgabe:** Probiere dich nun an den CSS-Eigenschaften aus. Versuche Absätze und Überschriften zu formatieren.
> Du kannst die Außenabstände auch auf Bilder anwenden.
> Versuche alle der eben gelernten Eigenschaften einmal auszuprobieren.

### Selektoren

Bisher haben mir mit CSS alle Absätze gleich formatiert. Du möchtest z. B. einen Absatz besonders hervorheben und in zusätzlich Grün einfärben.
Alle anderen Absätze sollen aber weiterhin die CSS-Formatierungen behalten, die für das `<p>`-Tag gelten.
Um dieses Problem zu lösen, gibt es Selektoren. Du kannst einem HTML-Element eine eindeutige `id` geben, die es nur einmal
in der gesamten HTML-Datei gibt. Das HTML-Element kann dadurch eindeutig zugeordnet werden.


```html
<p>Das ist normaler Text</p>
<p id="important-text">Das ist besonders hervorgehobener Text</p>
```

Die `id` ist ein weiteres Attribut, dass du einem html-Tag geben kannst.
Im obigen Beispiel hat der zweite Absatz die id `important-text`.
Im nachfolgenden CSS kannst du mit dem Raute-Zeichen `#` und der id genau dieses eine Element formatiern.
Für den zweiten Absatz mit der id wäre es somit `#important-text` gefolgt von geschweiften Klammern.

```css
p {
    font-size: 1em;
    margin-top: 1.5em;
}

#important-text {
    color: green;
}
```

Sehen wir uns das obige CSS genauer an. Mit `p` werden alle Absätze mit der Schriftgröße `1em` und
einem Abstand nach oben von `1.5em` formatiert. 

Mit dem Selektor `#important-text` wird nur der eine Absatz mit der id `important-text` grün eingefärbt.
Wichtig hierbei ist: Alle Formatierungen, die für das `<p>`-Tag gelten werden auch für den Absatz
mit der id `important-text` übernommen.
Also `important-text` ist am Ende nicht nur grün eingefärbt, sondern auch die Schriftgröße `1em`
und einen Abstand nach oben von `1.5em`.

> **Aufgabe:** Probiere dich nun an den CSS-Eigenschaften aus. Versuche einzelne Absätze und Überschriften
> etwas anders zu formatieren als die übrigen.
> Versuche alle der eben gelernten Eigenschaften einmal auszuprobieren.

### Strukturierung mit Containern/Boxen

Mit dem HTML-Element `<div>` (engl. "division" für Abteilung/Bereich) kannst du leicht ganze Bereiche
auf deiner Webseite verschieben oder mit Formatierungen versehen.
Beim Adventskalender wird jedes Türchen aus einem `<div>` bestehen.

Du kannst für die Boxen Außenabstände definieren (`margin`) und auch eine Hintergrundfarbe (`background-color`).
Zudem ist es möglich der Box eine Breite `width` und/oder eine Höhe `height` zu geben.

Um ein `<div>` mittig auf der Seite zu platzieren, kannst du bei den Außenabständen `auto` verwenden.
Die horizontalen, bzw. vertikalen Außenabstände werden dabei gleichmäßig aufgeteilt.

> **Aufgabe:** Platziere eine Box mit Inhalt horizontal mittig auf der Seite.
> Verwende dazu den Wert `auto` anstatt eines festen Wertes für den linke und den rechten Abstand.
> Gebe der Box eine Breite von `75%` und noch einen Abstand nach oben (`margin-top`).

