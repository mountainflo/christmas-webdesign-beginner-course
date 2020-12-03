![santa]
# Secret Santa (Wichtel Paar Generator)
Wenn du dich schon ein bisschen mit html und css auskennst kannst du etwas schwereres versuchen.

Wichteln, wer kennt es nicht, zu Weihnachten schreibt man die Namen der Familie und freunde auf 
kleine Zettel mischt Sie in einer Schüssel und jeder zieht einen Namen. Der gezogene wird dann heimlich beschenkt.

In den heutigen Zeiten wird es aber immer schwerer sich zu treffen um Namen aus der Schüssel zu ziehen.
Zum glück kannst du programmieren. Jetzt kannst du eine Seite schreiben die Wichtelpartner zuordnet.
Das funktioniert auch in Skype und Teams.

Mehr infos zum Wichteln: [Geschenke.de - Wichteln](https://www.geschenke.de/magazin-wichteln/)

### Die Regeln
1. Jeder der mitspielt wird beschenkt und beschenkt jemand anderen
2. Niemand darf sich selbst beschenken

## Ziel des Projektes
In diesem Projekt benutzen wir JavaScript um Namen die auf einer HTML Seite eingegeben wurden auszulesen.
Diese namen ordnen wir dann zufällig einander zu, so das jeder einem anderen aus der Gruppe etwas schenkt.
Zu Beginn testen wir auf der Konsole, bauen unsere Seite aber nach und nach aus.

Wenn du alle Aufgaben gemeistert hast sollte deine Seite
* Die Paare auf der Seite ausgeben
* Belibig viele Teilnehmer unterstützen
* Keine leeren Namen akzeptieren

Du wirst hier viel JavaScript brauchen also halte besser eine JavaScript Dokumentation bereit:  
[MDN JavaScript Dokumentation](https://developer.mozilla.org/de/docs/Web/JavaScript)  
[W3Schools.com JavaScript](https://www.w3schools.com/js/default.asp)


## Zuordnen von 4 Teilnehmern

Als ersten Schritt wollen wir 4 Namen sammeln und jedem einen partner aus der Gruppe zulosen.

**Beispiel :**  
Eingabe: Anna, Bert, Ernie, Lisa
Ausgabe: {"Anna" => "Bert", "Bert" => "Anna", "Ernie" => "Lisa", "Lisa" => "Ernie"}

### Anfang
Um zu beginnen, erstellt ein neues repl auf repl.it. Die Sprache sollte `HTML, CSS, JS` sein.
Den inhalt der `index.html` kannst du mit dem inhalt der [index.html](templates/index.html) im `templates` ordner ersetzen. Das gleiche machst du mit der [style.css](templates/style.css) datei. In den beiden Dateien habe ich das Grundgerüst schon vorbereitet, du must dir nur noch einen netten Text ausdenken und in das HTML schreiben.

### Namen lesen
Benutze JavaScript um nach dem klicken auf den Butten unten die Namen aus den input-Elementen zu lesen und gebe Sie in der Konsole unten rechts aus.

<details>
  <summary>Tip 1</summary>

  Die `querySelector` Funktion und einen `EventListener` könnten bei dieser Aufgabe hilfreich sein.

  ### querySelector
  Die `querySelector` Funktion gibt dir das erste Element das zu deiner Suche passt. Als parameter übergibst du dabei einen [CSS Selector](https://www.w3schools.com/cssref/css_selectors.asp) als String. Falls 
  ```html
  <button calss="myButton">Drück mich</button>
  ```

  ```javascript
  const button = document.querySelector(".myButton");
  ```

  ### EventListener
  Ein EventListener wird aufgerufen wenn du bestimmte Aktionen auf deiner Seite machst. So kannst du fest legen das eine Funktion aufgerufen wird wenn du auf etwas clickst. 
  EventListener funktionieren nicht nur mit Buttons sondern mit allen HTML Elementen.  
  Der erste Parameter gibt die Aktion an z.b. "click" für einen Mausclick.  
  Der zweite Parameter gibt die funktion an, die dann aufgerufen wird.
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
  
  ### value und Array
  Um die Namen zu lesen kanst du die `value` Eigenschaft von input-Elementen nutzen. 
  Denke daran das du mehrere Namen sameln must, dafür ist ein einem `Array` gut geeignet.
  ```javascript
  let alleWichtelNamen = []; // Array inizialisieren
  // ... dein code ...
  let wichtelName = myInput.value; // Namen auslesen
  alleWichtelNamen.push(wichtelName); // Namen an Array anhängen
  ```
</details>
<details>
  <summary>Tip 3</summary>

  ### Konsolen Ausgabe
  Mit `console.log(...)` kannst du etwas in die schwarze Konsole unten rechts schreiben. damit kannst du schnell testen ob dein JavaScript funktioniert.
  ```javascript
  console.log("Der name des wichtels ist " + wichtelName);
  ```
</details>

### Paare finden
Wenn du erfolgreich deine Wichtel-Teilnehmer auf der Konsole ausgegeben hast, kannst du dir überlegen wie du die Teilnehmer einander zuordnest. 
Dafür brauchst du einen Algorithmus der die beiden Regeln befolgt die oben beschrieben sind. Wenn du keine Idee hast kannst du dir meinen anschauen:
<details>
  <summary>Algorithmus</summary>

  ### Konsolen Ausgabe
  Mit `console.log(...)` kannst du etwas in die schwarze Konsole unten rechts schreiben. damit kannst du schnell testen ob dein JavaScript funktioniert.
  ```
  Input : teilnehmerliste
  Inizialisiere MAP;
  Inizialisiere TEILNEHMERLISTEKOPIE;
  
  FÜR TEILNEHMER in teilnehmerliste  
    Inizialisiere INDEX;
    Inizialisiere ZÄHLER = 0;
    Inizialisiere PARTNER;
    TUE
      INDEX = zufallszahl 0 - TEILNEHMERLISTEKOPIE.anzahl
      PARTNER = TEILNEHMERLISTEKOPIE[index]
      ZÄHLER + 1
    SOLANGE PARTNER == TEILNEHMER && ZÄHLER <= 100
    entferne PARTNER von TEILNEHMERLISTEKOPIE
  ENDE
  
  WENN einerÜbrig
    nochmalVonVorne
  ```
</details>

### Einer ist übrig

## Wir sind mehr als 4

## Deinen Namen kenn ich nicht


###### Anmerkungen

Santa Bild von [Radoan Tanvir](https://pixabay.com/de/users/radoan_tanvir-866268/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=5668363) 

[santa]: https://cdn.pixabay.com/photo/2020/10/19/17/03/santa-claus-5668363_960_720.png
