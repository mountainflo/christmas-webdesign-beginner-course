![santa]
# Secret Santa (Wichtel Paar Generator)
Wenn du dich schon ein bisschen mit html und css auskennst kannst du diese schwerere Aufgabe versuchen.

Wichteln, wer kennt es nicht, zu Weihnachten schreibt man die Namen der Familie und Freunde auf 
kleine Zettel, mischt Sie in einer Schüssel und jeder zieht einen Namen. Der gezogene wird dann heimlich beschenkt.

In den heutigen Zeiten wird es aber immer schwerer sich zu treffen um Namen aus der Schüssel zu ziehen.
Zum Glück kannst du programmieren. Jetzt kannst du eine Seite schreiben die Wichtelpartner zuordnet.
Das funktioniert auch in Skype und Teams.

Mehr infos zum Wichteln: [Geschenke.de - Wichteln](https://www.geschenke.de/magazin-wichteln/)

### Die Regeln
1. Jeder der mitspielt wird beschenkt
2. Jeder beschenkt jemand anderen
3. Niemand darf sich selbst beschenken

## Ziel des Projektes
In diesem Projekt benutzen wir JavaScript um Namen die auf einer HTML Seite eingegeben wurden auszulesen.
Diese Namen ordnen wir dann zufällig einander zu, so das jeder einem anderen aus der Gruppe etwas schenkt.
Zu Beginn testen wir auf der Konsole, bauen unsere Seite aber nach und nach aus.

Wenn du alle Aufgaben gemeistert hast sollte deine Seite
* Die Paare auf der Seite ausgeben
* Beliebig viele Teilnehmer unterstützen
* Keine leeren Namen akzeptieren
* Die Partner nur anzeigen wenn man darüber fährt

Du wirst hier viel JavaScript brauchen also halte besser eine JavaScript Dokumentation bereit:  
Einfach : [W3Schools.com JavaScript](https://www.w3schools.com/js/default.asp)  
Detailiert : [MDN JavaScript Dokumentation](https://developer.mozilla.org/de/docs/Web/JavaScript)  


## Zuordnen von 4 Teilnehmern

Als ersten Schritt wollen wir 4 Namen sammeln und jedem einen partner aus der Gruppe zulosen.

#### Beispiel :  
```
Eingabe: Anna, Bert, Ernie, Lisa  
Ausgabe: {"Anna" => "Bert", "Bert" => "Anna", "Ernie" => "Lisa", "Lisa" => "Ernie"}
```

### Anfang
Um zu beginnen, erstellt ein neues repl auf [repl.it](https://repl.it). Die Sprache sollte `HTML, CSS, JS` sein.
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
  Der erste Parameter gibt die Aktion an z.b. "click" für einen Mausklick.  
  Der zweite Parameter gibt die funktion an, die dann aufgerufen wird.  
  Parameter brauch ihr nicht angeben, JavaScript übergibt der Funktion immer das event objekt.
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
  
  ### Value und Array
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
Dafür brauchst du einen Algorithmus der die Regeln befolgt die oben beschrieben sind. Wenn du keine Idee hast wie das funktionieren kann, kannst du dir meinen anschauen:
<details>
  <summary>Algorithmus</summary>
  
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
  <summary>Tip 1: Array kopieren</summary>

  Wenn du in Javascript einen Array einer Funktion übergeben wollt wird nicht der inhalt des Arrays übergeben sondern nur ein Verweis auf das original. Wenn du also in der Funktion den Teilnehmer-Array verändern willst, musst du ihn kopieren. 

  ### Array.from und splice
  `Array.from` erstellt eine genaue Kopie von dem übergebenen Array. Mit `splice(pos, anzahl)` kanst du an der übergebenen Position die übergebene Anzahl an Elementen löschen.
  Denkt daran das der index eines arrays bei 0 anfängt.
  
  ```javascript
  const teilnehmer = ['Bernd','Lisa'];
  
  function tueetwas(teilnehmer){
    let teilnehmerKopie = Array.from(teilnehmer);
    teilnehmerKopie.splice(0, 1);
    // teilnehmerKopie : ['Lisa']
  }
  
  // teilnehmerKopie : ['Bernd','Lisa']
  ```
</details>
<details>
  <summary>Tip 2: for each</summary>

  ### ForEach
  Vielleicht kennst du schon `for` Schleifen. Wusstest du das es eine vereinfachte Variante für Arrays gibt?
  Wenn du deine Teilnehmer in einem Array gespeichert hast kannst du hiermit ganz einfach durch deine Teilnehmer gehen.

  ```javascript
  const teilnehmer = ['Bernd','Lisa','Klaus','Lara'];

  for (const tn of teilnehmer) {
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
<details>
  <summary>Tip 3: Zufallszahlen</summary>

  ### Math.random()
  Um zufällige Paare zu generieren brauchst du Zufallszahlen. diese kannst du mit der Funktion `Math.random()` generieren. Sie generiert Zahlen von 0 bis 1.
  Um eine Zahl in deinem gewünschten Breich zu bekommen musst du das Ergebnis mit der höchsten Zahl multiplizieren die du erhalten möchtest. 
  Um kommazahlen zu vermeiden kannst du die Funktion `Math.floor()` benutzen, diese rundet die Zahl.

  ```javascript
  // Zufallszahl von 0 bis 10
  let zahl = Math.floor(Math.random() * 10);
  
  // Zufallszahl von 0 bis 8
  let zahl = Math.floor(Math.random() * 8);
  ```
</details>
<details>
  <summary>Tip 4: Paare merken</summary>

  ### Map()
  Arrays können pro Index nur einen Wert speichern. Um uns paare zu merken müssen wir aber nicht viel tricksen. Eine `Map` speichert immer einen Wert zu einem Schlüssel.
  Das ist perfekt für diese Aufgabe. Neue paare fügst du mit der funktion `push()` hinzu.

  ```javascript
    let paare = new Map();
    paare.set("Anna","Bert");
    paare.set("Bert","Anna");
    console.log(paare);
    // Ausgabe: {"Anna" => "Bert", "Bert" => "Anna"}
  ```
</details>


### Wann seh ich denn endlich etwas
Wenn du weist dass dein JavaScript-Code funktioniert kannst du dich um die Anzeige der Paare kümmern.
Versuche deine Lösung dynamisch zu schreiben, damit Sie mit einer beliebigen Anzahl von Teilnehmern funktioniert. Auf diese Weise musst du im nachher nicht alles neu schreiben.   

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

  for (const paar of wichtelPaare) {
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
  <summary>Tip 1: textContent</summary>

  ### textContent
  Du kannst auch aus "normalen" HTML-Elementen text auslesen. Die funktion dafür heißt `textContent`.

  ```html
  <span class="wichtel">Anna</span>
  ```

  ```javascript
  const wichtel = document.querySelector(".wichtel");
  let name = wichtel.textContent;
  ```
</details>

<details>
  <summary>Tip 2: target & classList</summary>

  Falls du nicht nur Teilnehmer hinzufügen sondern auch entfernen möchtest. Kannst du das target und classList attribut verwenden um den EventListener einfacher zu machen.

  ### target & classList
  Jeder EventListener 

  ```html
  <div class="list">
    <div class="wichtel">
      <span class="name">Bert</span>
      <span class="remove-icon">Löschen</span>
    </div>
  </div>
  ```

  ```javascript
  const list = document.querySelector(".list");
  list.addEventListener("click", wichtelLöschen);
  
  function wichtelLöschen(event) {
    let element = event.target;
    if(element.classList[0] === "remove-icon") {
      element.parentElement.remove();
    }
  }
  ```

  In diesem Beispiel gibt es gleich mehrere Dinge die dir helfen. 
</details>



### Deinen Namen kenn ich nicht
Vielleicht hast du schon festgestellt das es Probleme machen kann wenn man versucht einen leeren String ein zu geben. Versuche zu prüfen ob der eingegebene Name leer ist bevor du ihn verarbeitest. Bonus: schaffst du es auch zu prüfen ob der Name schon in der Gruppe vorhanden ist ?

## Partner bleiben geheim
Wie ihr bestimmt schon gemerkt habt, kann man nach dem Klick auf den Button immer direkt alle Partner sehen. Nutzt was ihr bisher gelernt habt um die namen erst an zu zeigen wenn man über ein icon in der Zeile fährt. dafür könnt ihr die Event-Listener `mouseover` und `mouseout` nutzen.


###### Anmerkungen

Santa Bild von [Radoan Tanvir](https://pixabay.com/de/users/radoan_tanvir-866268/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=5668363) 

[santa]: https://cdn.pixabay.com/photo/2020/10/19/17/03/santa-claus-5668363_960_720.png
