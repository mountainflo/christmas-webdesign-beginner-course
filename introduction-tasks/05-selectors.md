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
