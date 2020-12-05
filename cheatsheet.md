# Cheatsheet für HTML, CSS und JavaScript

**Dokumentation:**

* Tutorials und Dokumentation zu HTML/CSS/JS auf Deutsch: [https://wiki.selfhtml.org/wiki](https://wiki.selfhtml.org/wiki)
    * Alle wichtigen HTML-Elemente: [https://wiki.selfhtml.org/wiki/HTML#Elemente](https://wiki.selfhtml.org/wiki/HTML#Elemente)
* Kurz und kompakt alle HTML-Befehle und CSS-Eigenschaften (auf Englisch): [https://www.w3schools.com/](https://www.w3schools.com/)
    * CSS-Referenz: [https://www.w3schools.com/cssref](https://www.w3schools.com/cssref)
    * HTML-Referenz: [https://www.w3schools.com/tags](https://www.w3schools.com/tags)    
* Einfache JavaScript dokumentation mit Beispielen
    * [W3Schools.com JavaScript](https://www.w3schools.com/js/default.asp)  
* Detailierte JavaScript dokumentation wenn man es genau wissen will 
    * [MDN JavaScript Dokumentation](https://developer.mozilla.org/de/docs/Web/JavaScript)  

**[HTML](#html)**

* [HTML-Grundgerüst](#html-grundgerst)
* [Texte](#texte)
* [Bilder](#bilder)
* [Links](#links)
* [Container](#container)

**[CSS](#css)**

* [CSS-Datei im HTML einbinden](#css-datei-im-html-einbinden)
* [Schriftformatierung](#schriftformatierung)
* [Außenabstände](#auenabstnde)
* [Slektoren](#selektoren)
* [Links](Links)
* [div-container formatieren](#div-container-formatieren)
* [Innenabstände](#innenabstnde)

**[JavaScript](#javascript)**

## HTML

### HTML-Grundgerüst

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

### Texte

```html
<h1>Überschriften (von h1 bis h6)</h1>
<h2>Unterüberschrift</h2>
<p>Absätze (engl. paragrahps)</p>

```

### Bilder

```html
<img src="hacker-school.jpg" alt="Hacker School Logo" width="100px" />
```

### Links

```html
Viel Spaß mit dem <a href="advents-calender.html">Online-Adventskalender</a> von der Hacker School.
```

### Container

```html
 <div class="grid">
     <div>1</div>
     <div>2</div>
     <div>3</div>
 </div>
 ```

## CSS

### CSS-Datei im HTML einbinden

```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```

### Schriftformatierung

|      |  Eigenschaft    |  Werte    |
| ---- | ---- | ---- |
|  Schriftgröße     | `font-size`       |  `0.75em`, `1em`, `3em`, ...  |
|  Schriftart       | `font-family`     |  `sans-serif`, `serif`     |
|  Fett             | `font-weight`     |  `bold`                    |
|  Kursiv           | `font-style`      |  `italic`                  |
|  Farbe            | `color`           |  `pink`, `red`, `orange`, `yellow`, `gold`, `brown`, `olive`, `green`, `cyan`, `blue`, `violet`, `magenta`, `purple`, `white`, `black` |
|  Textausrichtung  | `text-align`      |  `left`, `right`, `center` |

### Außenabstände

|      |  Eigenschaft    |  Werte    |
| ---- | ---- | ---- |
|  oben     | `margin-top`       |  `0.75em`, `1em`, `3em`, ...    |
|  unten     | `margin-bottom`       |  `0.75em`, `1em`, `3em`, ...    |
|  links     | `margin-left`       |  `0.75em`, `1em`, `3em`, ...    |
|  rechts     | `margin-right`       |  `0.75em`, `1em`, `3em`, ...    |

### Selektoren

|  Selektor    |  Beispiel   |  Beschreibung    | 
| ---- | ---- | ---- |
|  Typselektor     | `p`, `h1`, ...       |  Gilt für alle HTML-Elemente mit diesem Tag |
|  id-Selektor     | `#zitat`       |  Gilt für genau ein HTML-Element, das diese id besitzt (HTML-Attribut: `id="zitat"`)  |
|  Klassenselektor     | `.fliesstext`  |  Gilt für alle HTML-Elemente, diesen Klassennamen haben (HTML-Attribut: `class="fliesstext"`) |

### Links

|      |  Eigenschaft    |  Werte    |
| ---- | ---- | ---- |
|  unterstreichen     | `text-decoration`       |  `none`, `underline`    |

Für Links kannst du auch noch die Formatierung ändern, sobald du mit der Maus darüber fährst.
Dies machst du mit `hover`. Für Klassen verwendest du `a.CLASSNAME:hover`
und für Id-Selektoren z. B. `#zitat:hover`.

```css
a:hover {
    color: blue;
}
```

### div-container formatieren

|      |  Eigenschaft    |  Werte    |
| ---- | ---- | ---- |
|  Hintergrundfarbe     | `background-color`       |  `red`, `green`, `blue`, ...    |
|  Breite     | `width`       |  `5em`, ...    |
|  Höhe     | `height`       |  `5em`, ...    |

### Innenabstände

Innenabstände kannst du hauptsächlich bei den Boxen (`<div>`) verwenden.

|      |  Eigenschaft    |  Werte    |
| ---- | ---- | ---- |
|  oben     | `padding-top`       |  `0.75em`, `1em`, `3em`, ...    |
|  unten     | `padding-bottom`       |  `0.75em`, `1em`, `3em`, ...    |
|  links     | `padding-left`       |  `0.75em`, `1em`, `3em`, ...    |
|  rechts     | `padding-right`       |  `0.75em`, `1em`, `3em`, ...    |


## JavaScript

### JavaScript-Datei im HTML einbinden
```html
<head>    
	<script src="script.js" defer>
</head>
```
Das Schlüsselwort defer is hier wichtig. Es sorgt dafür, dass dieses Script erst geladen wird wenn das HTML fertig ist. 

### Variablen

```javascript
const festeVariable // definiert eine variable die nicht überschrieben werden darf, arrays in so einer variable können sich aber noch ändern
let variable // Variable, ist auf den block {} begrenzt in dem Sie definiert wird
```

### Array
```javascript
let liste = []; // Array initialisieren
liste.push("Anna"); // Namen an Array anhängen
liste.push("Ernie");
// liste : ["Anna","Ernie"]
liste.splice(liste.length-1, 1); // letztes Element löschen
// liste : ["Anna"]
```

### Konsolenausgabe
```javascript
console.log("Hallo Welt");
```

### EventHandler
```javascript
htmlElement.addEventListener("click", tueEtwas); // Wenn ein element geklickt wird
htmlElement.addEventListener("mouseover", tueEtwas); // Wenn die Maus über ein element fährt
htmlElement.addEventListener("mouseout", tueEtwas); // Wenn die Maus ein Element verlässt
htmlElement.addEventListener("keypress", tueEtwas); // Wenn die eine taste auf der Tastatur gedrückt wird

funktion tueEtwas(event) {
}
```

### HTML Elemente finden
```javascript
// Gibt das erste element zurück das die button class hat
document.querySelector(".button");

// Gibt einen Array mit allen elementen zurück die die wichtel class haben
document.querySelectorAll(".wichtel");
```

### IF Bedingungen
```javascript
if(wichtel === "klaus"){
  // Wird ausgeführt wenn die Variable wichtel den String 'klaus' enthällt
}

if(wichtel === "klaus" && zaehler < 100){
  // Wird ausgeführt wenn die Variable wichtel den String 'klaus' enthällt und der zähler kleiner als 100 ist
}

if(wichtel === "klaus" || zaehler < 100){
  // Wird ausgeführt wenn die Variable wichtel den String 'klaus' enthällt oder der zähler kleiner als 100 ist
}
```

### For each Schleife

```javascript
const teilnehmer = ['Bernd','Lisa','Klaus','Lara'];

for (const tn in teilnehmer) {
  // wird für jeden teilnehmer ausgeführt
  // tn enthällt den namen des aktuellen teilnehmers
}
```
