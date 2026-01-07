

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
#sayit {
  font-size: 1.2em;
  margin: 0 auto;
  width: 100%;
  color: #3d3d3d;
}
#speak {
  width: 100%;
  margin-top: 10px;
}
</style>

<input id="sayit" type="text" />
<button id="speak">Sprich</button>

<script>
function sayIt(query, language) {
  var q = new SpeechSynthesisUtterance(query);
  q.lang = language;
  q.rate = 1.2;
  speechSynthesis.speak(q);
}
function attach(elementId, event, functionName) {
  var element = document.getElementById(elementId);
  if (element.addEventListener) {
    element.addEventListener(event, functionName, false);
  } else if (element.attachEvent) {
    element.attachEvent('on' + event, functionName);
  } else {
    element['on' + event] = functionName;
  }
}
/* Sprache der Sprachausgabe*/
function interpret() {  sayIt(document.getElementById('sayit').value, 'de-DE');
}
/* Sprachausgabe nach dem laden der Seite */
sayIt('Hallo! Ich kann sprechen', 'de-DE');
attach('activate', 'click', interpret);
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
