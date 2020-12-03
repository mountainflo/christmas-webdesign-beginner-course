![santa]
# Secret Santa (Wichtel Paar Generator)
Wenn ihr euch schon ein bisschen mit html und css auskennt könnt ihr etwas schwereres versuchen.

Wichteln, wer kennt es nicht, zu Weihnachten schreibt man die Namen der Familie und freunde auf 
kleine Zettel mischt Sie in einer Schüssel und jeder zieht einen Namen. Der gezogene wird dann heimlich beschenkt.

In den heutigen Zeiten wird es aber immer schwerer sich zu treffen um Namen aus der Schüssel zu ziehen.
Zum glück könnt ihr programmieren. Jetzt könnt ihr eine Seite schreiben die Wichtelpartner zuordnet.
Das funktioniert auch in Skype und Teams.

Mehr infos zum Wichteln: [Geschenke.de - Wichteln](https://www.geschenke.de/magazin-wichteln/)

### Die Regeln
1. Jeder der mitspielt wird beschenkt und beschenkt jemand anderen
2. Niemand darf sich selbst beschenken

## Ziel des Projektes
In diesem Projekt benutzen wir JavaScript um Namen die auf einer HTML Seite eingegeben wurden aus zu lesen.
Diese namen ordnen wir dann zufällig einander zu, so das jeder einem anderen aus der Gruppe etwas schenkt.
Zu begin testen wir auf der Konsole, bauen unsere Seite aber nach und nach aus.

Wenn ihr alle aufgaben gemeistert habt sollte eure Seite
* Die Paare auf der Seite ausgeben
* Belibig viele Teilnehmer unterstützen
* Keine leeren Namen akzeptieren

Ihr werdet hier viel JavaScript brauchen also haltet besser eine JavaScript Dokumentation bereit:  
[MDN JavaScript Dokumentation](https://developer.mozilla.org/de/docs/Web/JavaScript)  
[W3Schools.com JavaScript](https://www.w3schools.com/js/default.asp)


## Zuordnen von 4 Teilnehmern

Als ersten Schritt wollen wir 4 Namen sammeln und jedem einen partner aus der Gruppe zulosen.

**Beispiel :**  
Eingabe: Anna, Bert, Ernie, Lisa
Ausgabe: {"Anna" => "Bert", "Bert" => "Anna", "Ernie" => "Lisa", "Lisa" => "Ernie"}

### Anfang
Um zu beginnen, erstellt ein neues repl auf repl.it. Die Sprache sollte `HTML, CSS, JS` sein.
Den inhalt der `index.html` könnt ihr mit dem inhalt der [index.html](templates/index.html) im `templates` ordner ersetzen. Hier habe ich das Grundgerüst schon vorbereitet. Das gleiche macht ihr mit der [style.css](templates/style.css) datei.

### Namen lesen
Benutze JavaScript um nach dem klicken auf den Butten unten die Namen aus den input-Elementen zu lesen und gebe Sie in der Konsole unten rechts aus.

<details>
    <summary>Tip 1</summary>

    Dazu wirst du die `querySelector` Funktion und einen `EventListener` brauchen.

    ### querySelector Beispiel
    ```html
    <button calss="myButton">Drück mich</button>
    ```

    ```javascript
    const button = document.querySelector(".myButton");
    ```

    ### EventListener Beispiel    
    ```javascript
    button.addEventListener("click", tueEtwas);

    function tueEtwas(event){
        event.preventDefault();
        // hier dein code
    }
    ```
</details><br>
<details>
    <summary>Tip 2</summary>

    Um die Namen zu lesen kanst du die `value` Eigenschaft von input-Elementen nutzen

    ### value Beispiel    
    ```javascript
    button.addEventListener("click", tueEtwas);

    function tueEtwas(event){
        event.preventDefault();
        // hier dein code
    }
    ```
</details>


### Paare finden

### Einer ist übrig

## Wir sind mehr als 4

## Deinen Namen kenn ich nicht


###### Anmerkungen

Santa Bild von [Radoan Tanvir](https://pixabay.com/de/users/radoan_tanvir-866268/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=5668363) 

[santa]: https://cdn.pixabay.com/photo/2020/10/19/17/03/santa-claus-5668363_960_720.png
