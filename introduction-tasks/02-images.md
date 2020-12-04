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
