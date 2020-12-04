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
* Beliebig viele Teilnehmer unterstützen
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
Benutze JavaScript um nach dem klicken auf den Button unten die Namen aus den input-Elementen zu lesen und gebe Sie in der Konsole unten rechts aus.

<details>
  <summary>Tip 1: querySelector</summary>

  Die `querySelector` Funktion und einen `EventListener` könnten bei dieser Aufgabe hilfreich sein.

  ### querySelector
  Die `querySelector` Funktion gibt dir das erste Element das zu deiner Suche passt. Als parameter übergibst du dabei einen [CSS Selector](https://www.w3schools.com/cssref/css_selectors.asp) als String. 
  Falls du einen Array mit allen passenden Elementen haben möchtest benutze die `querySelectorAll` Funktion.
  ```html
  <input type="text" class="wichtel"></input>
  <input type="text" class="wichtel"></input>
  <input type="text" class="wichtel"></input>
  <button class="myButton">Drück mich</button>
  ```

  ```javascript
  const button = document.querySelector(".myButton");
  const wichtel = document.querySelectorAll(".wichtel");
  ```
</details>
<details>
  <summary>Tip 2: EventListener</summary>

  ### EventListener
  Ein EventListener wird aufgerufen wenn du bestimmte Aktionen auf deiner Seite machst. So kannst du fest legen das eine Funktion aufgerufen wird wenn du auf etwas klickst. 
  EventListener funktionieren nicht nur mit Buttons sondern mit allen HTML Elementen.  
  Der erste Parameter gibt die Aktion an z.b. "click" für einen Maus-Click.  
  Der zweite Parameter gibt die funktion an, die dann aufgerufen wird.
  ```javascript
  button.addEventListener("click", tueEtwas);

  function tueEtwas(event){
    event.preventDefault();
    // hier dein code
  }
  ```
</details>
<details>
  <summary>Tip 3: Value & Array</summary>
  
  ### value und Array
  Um die Namen zu lesen kannst du die `value` Eigenschaft von input-Elementen nutzen. 
  Denke daran das du mehrere Namen sammeln must, dafür ist ein einem `Array` gut geeignet.
  ```javascript
  let alleWichtelNamen = []; // Array initialisieren
  // ... dein code ...
  let wichtelName = myInput.value; // Namen auslesen
  alleWichtelNamen.push(wichtelName); // Namen an Array anhängen
  ```
</details>
<details>
  <summary>Tip 4: Konsolen Ausgabe</summary>

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
  Initialisiere MAP;
  Initialisiere TEILNEHMERLISTEKOPIE;
  
  FÜR TEILNEHMER in teilnehmerliste  
    Initialisiere INDEX;
    Initialisiere ZÄHLER = 0;
    Initialisiere PARTNER;
    TUE
      INDEX = zufallszahl 0 - TEILNEHMERLISTEKOPIE.anzahl
      PARTNER = TEILNEHMERLISTEKOPIE[index]
      ZÄHLER + 1
    SOLANGE PARTNER == TEILNEHMER && ZÄHLER <= 100
    entferne PARTNER von TEILNEHMERLISTEKOPIE
  ENDE
  ```
</details>
<details>
  <summary>Tip 1: for each</summary>

  ### ForEach
  Vielleicht kennst du schon `for` Schleifen. Wusstest du das es eine vereinfachte Variante fŕ Arrays gibt?
  Wenn du deine Teilnehmer in einem Array gespeichert hast kannst du hiermit ganz einfach durch deine Teilnehmer gehen.

  ```javascript
  const teilnehmer = ['Bernd','Lisa','Klaus','Lara'];

  for (const tn in teilnehmer) {
    console.log(tn);
    /*
      Ausgabe:
        Bernd
        Lisa
        Klaus
        Lara
    */
  }
  ```
</details>

TODO: more tips

### Wann seh ich denn endlich etwas
Wenn du weist dass dein JavaScript-Code funktioniert kannst du dich um die anzeige der paare kümmern.
Versuche deine Lösung dynamisch zu schreiben, damit Sie mit einer beliebigen Anzahl von Teilnehmern funktioniert. Auf diese Weise musst du im nächsten Schritt nicht alles neu schreiben.   

<details>
  <summary>Tip 1: innerHTML</summary>

  ### innerHTML
  HTML elemente haben in JavaScript die Eigenschaft `innerHTML`. der typ dieser Eigenschaft ist String.
  änderst du diesen String, ändert sich auch sofort die Anzeige auf der Website.

  ```javascript
  const liste = document.querySelector(".liste");

  function schreibeInListe(){
    liste.innerHTML += `<div class="paar">...</div>`
  }
  ```
</details>
<details>
  <summary>Tip 2: for each Map</summary>

  ### ForEach mit Map
  Du kennst bestimmt schon den `ForEach` block der dir dabei hilft durch einen Array zu laufen.
  Das geht auch mit einer Map

  ```javascript
  const wichtelPaare = new Map();

  for (const paar in wichtelPaare) {
    let wichtel = paar[0]; // key
    let partner = paar[1]; // value
  }
  ```
</details>
<details>
  <summary>Pro Tip: Templates</summary>

  ### Templates
  Du kannst dir die Arbeit einfacher machen in dem du dir einfach Templates anlegst.
  Wenn du vor und hinter einem String in JavaScript einen "BackTick" benutzt __`__.

  ```javascript

  function schreibeInListe(){
    liste.innerHTML += paarHTML(paar[0], paar[1]);
  }

  function paarHTML(wichtel, partner){
    let template = [
      `<div class="paar">`,
        `<span class="wichtel">${wichtel}</span>`,
        `<span class="wichtel">${partner}</span>`,
      `</div>`
    return template.join("\n");
  }
  ```
</details>

### Einer ist übrig
Wenn deine Seite funktioniert versuche folgendes. Entferne eines der Input-Felder.
Jetzt kannst du nur noch 3 Teilnehmer eingeben. Führe die Zuordnung ein paar mal aus.
Merkst du etwas ? ... Der Algorithmus verstößt gegen eine der Regeln.
Immer wieder mal muss der letzte Teilnehmer sich selbst beschenken.

Versuche herauszufinden wie du es lösen kannst. Man müsste das doch irgendwie abfangen und die Zuordnung einfach nochmal starten können. :thinking:

<details>
  <summary>Tip: Exception</summary>

  Ein möglicher Weg dieses Problem zu lösen ist eine Exception.

  ### Exceptions
  Wie in vielen anderen Programmiersprachen kann man in JavaScript "Fehler werfen".
  Im Grunde bedeutet das, dass eine Funktion "geplant" abbricht und das problem zurückmeldet.
  diese Rückmeldung musst du abfangen, sonst bricht das ganze Programm ab und es passiert nichts mehr. 

  ##### Fehler werfen
  ```javascript
  function wichtelZuordnen(){
    // ... code ...
    if(teilnehmer === partner){
      throw new ZuordnungFehlgeschlagenException();
    }
  }

  function ZuordnungFehlgeschlagenException(){
    const name = "ZuordnungFehlgeschlagenException";
    const beschreibung = "Die Teilnehmer konnten nicht den Regeln entsprechend zugeordnet werden"
  }
  ```
  ##### Fehler abfangen
  ```javascript
  function main() {
    // ... code ...
    let wichtelPaare = null;
    try {
      wichtelPaare = wichtelZuordnen();
    } catch (error) {
      if(error instanceof ZuordnungFehlgeschlagenException){
        console.log("Die Zuordnung hat leider nicht funktioniert");
      }
    }
  }
  ```
  Zusammen mit einer `while` Schleife kannst du eine Exception benutzen um das Zuordnen nochmal zu versuchen.
  Denke aber daran einen Zähler zu benutzen, damit dein Programm es nicht unendlich nochmal versucht.
</details>

## Wir sind mehr als 4
Damit wir nicht immer unsere Seite anpassen müssen wenn sich die Anzahl unserer Teilnehmer ändert versuche das bisher gelernte zu nutzen um beliebig viele Teilnehmer zu ermöglichen.

<details>
  <summary>Tip 1: innerText</summary>

  ### innerText
  Du kannst auch aus "normalen" HTML-Elementen text auslesen. Die funktion dafür heißt `innerText`.

  ```html
  <span class="wichtel">Anna</span>
  ```

  ```javascript
  const wichtel = document.querySelector(".wichtel");
  let name = wichtel.innerText;
  ```
</details>



### Deinen Namen kenn ich nicht
Vielleicht hast du schon festgestellt das es probleme machen kann wenn Man versucht einen leeren String ein zu geben oder ein Name doppelt ist. Versuche zu prüfen ob der eingegebene Name doppelt oder leer ist bevor du ihn verarbeitest.


###### Anmerkungen

Santa Bild von [Radoan Tanvir](https://pixabay.com/de/users/radoan_tanvir-866268/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=5668363) 

[santa]: https://cdn.pixabay.com/photo/2020/10/19/17/03/santa-claus-5668363_960_720.png
