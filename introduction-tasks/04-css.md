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

Keine Sorge, du musst die einzelnen Eigenschaften nicht auswendig können.
Du kannst jeder Zeit im Cheatsheet nachschauen, das wir dir zu Beginn gegeben haben.
Oder schaust z. B. auf der Webseite [https://www.w3schools.com/cssref](https://www.w3schools.com/cssref) nach.
