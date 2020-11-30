# Weihnachtskarte

Die zuvor erlernten HTML- und CSS-Kenntnisse möchten wir in diesem Projekt praktisch anwenden.
Passend zur Weihnachtszeit gestalten wir eine Weihnachtskarte, die du am Ende digital verschicken kannst.

## Ziel dieses Projekts

Für deine Weihnachtskarte kannst du HTML und CSS verwenden. Versuche auch Links in die Weihnachtskarte einzubauen.

Hier eine Übersicht, was wir bereits mit HTML alles gemacht haben:
* Texte mit `<p>`, `<h1>`, `<h2>`, `<h3>`
* Container (Boxen, Schachteln) mit `<div>`
* Links mit `<a href="hier-steht-der-link"></a>`
* Bilder mit `<img src="name-der-bilddatei.jpg" alt="Alternativer Text bei Fehlern" />`

Eine gute Übersicht über CSS bietet dir zum Beispiel die englischsprachige Seite [https://www.w3schools.com/cssref](https://www.w3schools.com/cssref).

Ansonsten kannst du auch immer in den `cheatsheet`s nachschauen.

## Zusätzliche Gestaltungsmöglichkeiten

Hier noch ein paar Gestaltungsideen für deine Weihnachtskarte:

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

Im Internet stehen dir ganz viele Bilder zur Verfügung. Du musst aber aufpassen, welche Bilder du verwendest.
Nicht alle Bilder, die du einfach so herunterladen kannst, sind auch wirklich kostenlos.
Meistens hat der Urheber des Bildes die Rechte an dem Bild. Falls du dieses Bild verwenden möchtest, musst du zuerst den Urheber um Erlaubnis fragen.

Freie Bilder, bei denen keine Namesnennung des Urhebers erforderlich ist, findest du auf Seiten, die "Free Stock Images" anbieten.
Beispiele für solche Seiten sind:
* [https://unsplash.com/](https://unsplash.com/)
* [https://pixabay.com/de/](https://pixabay.com/de/)

Das Bild der Beispiel-Weihnachtskarte ist von [https://www.freepik.com/](https://www.freepik.com/).
Wenn du Bilder von dieser Seite verwenden möchtest, musst aber einen Link einfügen.

### Ganzseitiges Hintergrundbild

Wenn du für deine Weihnachtskarte ein Hintergrundbild verwenden möchtest, kannst du das wie im nachfolgenden Beispiel machen.
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

## Weihnachtskarte mit Freunden teilen

In `repl.it` hast du die Möglichkeit deine Webseite auch in einem separaten Tab zu öffnen.
Die URL des neuen Tab kannst du kopieren und an Freunde und Familie verschicken.

**Wichtig:** Damit deine Webseite auch von deinen Freunden angeschaut werden kann, musst du die Sichtbarkeit deines `repls` auf öffentlich stellen.
Die Sichtbarkeit ist in `repl.it` standardmäßig auf `public` eingestellt.
