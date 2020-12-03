# Adventskalender

Die zuvor erlernten HTML- und CSS-Kenntnisse möchten wir in diesem Projekt praktisch anwenden.
Passend zur Vorweihnachtszeit kannst du dir nachfolgend einen digitalen Adventskalender bauen.

Der Adventskalender soll wie üblich 24 Türchen enthalten. Wie du die Webseite mit dem Adventskalender
gestaltest, darfst du selbst entscheiden. Welche Inhalte du hinter den Türchen versteckst, darfst du
auch selbst entscheiden. Entweder du platzierst hinter jedes Türchen ein Bild oder ein Text.

## Ziel des Projekts

Für den Adventskalender kannst du alles verwenden, was du bereits in der Einführung gelernt hast.
* Texte mit `<p>`, `<h1>`, `<h2>`, `<h3>`
* Verwendung von `<div></div>`
* Verwendung von Links (`<a href=""></a>`)
* Bilder mit `<img src="name-der-bilddatei.jpg" alt="Alternativer Text bei Fehlern" />`

Eine gute Übersicht über CSS bietet dir zum Beispiel die englischsprachige Seite [https://www.w3schools.com/cssref](https://www.w3schools.com/cssref).

Ansonsten kannst du auch immer in den `cheatsheet`s nachschauen.

## Zusätzliche Gestaltungsmöglichkeiten

### Grid-Layout

Für die Anordnung der Türchen kannst du das "CSS Grid Layout Module" verwenden.
Mit diesem CSS-Modul kannst du die `<div>`-Elemente schnell und einfach in einem Raster anordnen.

Für jedes Türchen ist ein `<div>` vorgesehen. Im nachfolgenden Codebeispiel sind exemplarisch nur die Türchen 1 bis 3 aufgelistet.
Alle Türchen werden anschließend in ein `<div>` gepackt, das wir mit der Klasse `grid` versehen.

```html
<div class="grid">
    <div>1</div>
    <div>2</div>
    <div>3</div>
</div>
```

In CSS kannst du anschließend die Formatierung für das Raster einstellen. Mit `grid-template-columns` kannst du
angeben, wie viele Spalten du haben möchtest. In Beispiel sind es 4 Spalten, die alle gleich groß sind.
Falls du die Abstände zwischen den Spalten und Zeilen verändern möchtest, kannst du dies mit `grid-column-gap`
für die Spalten und `grid-row-gap` für die Zeilen machen.

```css
.grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: auto;
    grid-column-gap: 0.5em;     /* Abstände zwischen den Spalten */
    grid-row-gap: 0.5em;        /* Abstände zwischen den Zeilen */
}
```

### Schriften

Falls du ausgefallenere Schriften verwenden möchtest, kannst auch mal auf [https://fonts.google.com/](https://fonts.google.com/) nachschauen.
Die Webseite *Google Fonts* bietet dir eine große Auswahl an kostenlosen Schriften.
Die Schriften kannst du kostenlos in deine Webseite einbinden.

Du musst dazu nur einen Link zur Schrift in den Header der HTML-Datei einfügen.
Falls der Name deiner Schrift Leerzeichen enthält ersetzt du diese mit einem `+`-Zeichen.

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Nothing+You+Could+Do">
```

In der CSS-Datei steht dir nun diese Schriftart zur Verfügung.
Falls die Schriftart einmal nicht geladen werden kann, empfiehlt es sich immer eine alternative Schriftart anzugeben.
Die Alternative wird mit einem Komma getrennt dahinter angegeben.

```css
p {
font-family: 'Nothing You Could Do', serif;
}
```

### Rechtefreie Bilder aus dem Internet

Im Internet stehen dir ganz viele Bilder zur Verfügung. Du musst aber aufpassen welche Bilder du verwendest.
Nicht alle Bilder, die du einfach so herunterladen kannst, sind auch wirklich kostenlos.
Meistens hat der Urheber des Bildes die Rechte an dem Bild. Falls du dieses Bild verwenden möchtest, musst du zuerst den Urheber um Erlaubnis fragen.

Freie Bilder, bei denen keine Namesnennung des Urhebers erforderlich ist, findest du auf Seiten, die "Free Stock Images" anbieten.
Beispiele für solche Seiten sind:
* [https://unsplash.com/](https://unsplash.com/)
* [https://pixabay.com/de/](https://pixabay.com/de/)

### Ganzseitiges Hintergrundbild

Wenn du für deinen Adventskalender ein Hintergrundbild verwenden möchtest, kannst du das wie im nachfolgenden Beispiel machen.
Vom Bild wird dabei immer so viel wie möglich dargestellt.

```css
html {
    background: url(images/winter-landscape.jpg);   /* link zur Bilddatei. Pfad zur Bilddatei ausgehend von der Position der CSS-Datei */
    background-repeat: no-repeat;                   /* wiederholung des Bildes */
    background-position: center center;             /* horizontale und vertikale Position des Bildes auf der Webseite */
    background-attachment: fixed;                   /* das Bild scrollt nicht mit dem Inhalt der Seite mit */
    background-size: cover;                         /* Bild wird vergrößert, bzw. verkleinert, um die gesamte Seite auszufüllen */
}
```

## Erweiterungen

### Türchen lassen sich nicht im Voraus öffnen

Du hast wahrscheinlich schon festgestellt, dass sich das Türchen vom 24. bereits öffnen lässt, obwohl noch gar nicht der 24. Dezember ist.
Mit etwas JavaScript ist möglich, dass sich die Türchen nicht vor dem eigentlichen Tag öffnen lassen.

Füge dazu bei allen Türchen in den Link das Attribut `onclick` ein. Mit diesem Attribut wird beim Klick auf den Link
die angegebene JavaScript-Funktion ausgeführt. Im nachfolgenden Beispiel wird somit `openDoor(24)` ausgeführt.
An die Funktion `openDoor()` wird dabei der Wert `24` übergeben. In der Funktion `openDoor()` kannst du anschließend
überprüfen, ob heute auch wirklich der 24.12 ist. Erst dann wird der Link zum Türchen geöffnet.

```html
<a href="#" onclick="openDoor(24)">24</a>
```

Damit du es etwas einfacher hast, findest du nachfolgend die JavaScript-Funktion `openDoor()`.
Füge den kompletten Code inklusive den beiden `<script>`-Tags in den Header deiner HTML-Datei.

```html
<script>
function openDoor(inputDay) {
    let date = new Date();
    let current_day = date.getDay();
    let current_month = date.getMonth();

    if (current_month === 12 && inputDay <= current_day && inputDay > 0) {
        window.location.replace("door-" + inputDay + ".html")   /* evtl. noch den Link zur HTML-Datei ändern */
    } else {
        alert("Du kannst das Türchen erst am " + inputDay + ". aufmachen.")
    }
}
</script>
```

Wenn du möchtest, kannst du die Funktion auch noch beliebig anpassen und erweitern.
Du kannst z.B. die Nachricht ändern, die angezeigt, sobald jemand zu früh ein Türchen öffnet.
Ändere dazu den Text, der an die `alert()`-Funktion übergeben wird.
Falls du deine HTML-Dateien für die Türchen in einem anderen Ordner abgelegt hast oder
die Dateien anders benannt hast, musst du den Namen der HTML-Datei in `window.location.replace()` anpassen.

### Weitere Ideen

* `Zurück`-Links als Button umsetzen. Für die Erstellung der Buttons kann z. B. [https://www.bestcssbuttongenerator.com/](https://www.bestcssbuttongenerator.com/) verwendet werden.
* Zusätzliche Icons einfügen z. B. mit [https://www.w3schools.com/icons/](https://www.w3schools.com/icons/).
* Weihnachtliche gifs einbinden, z. B. von [https://giphy.com/](https://giphy.com/).

## Weihnachtskarte mit Freunden teilen

In `repl.it` hast du die Möglichkeit deine Webseite auch in einem separaten Tab zu öffnen.
Die URL des neuen Tab kannst du kopieren und an Freunde und Familie verschicken.
Den Button zum Öffnen im neuen Tab findest oben rechts, direkt unter dem `+`-Zeichen.

**Wichtig:** Damit deine Webseite auch von deinen Freunden angeschaut werden kann, musst du die Sichtbarkeit deines `repls` auf öffentlich (`public`) stellen.
Die Sichtbarkeit ist in `repl.it` standardmäßig auf `public` eingestellt.
