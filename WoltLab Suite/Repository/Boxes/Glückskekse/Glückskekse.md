### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.glueckskeks { 
    margin-top: 20px; 
    text-align: center; 
}
span.quote {
    font-style: italic; 
}
#new-quote-btn {
    text-align: center;
    margin: 0 auto;
}
</style>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.3/jquery.min.js" integrity="sha512-egJ/Y+22P9NQ9aIyVCh0VCOsfydyn8eNmqBy+y2CnJG+fpRIxXMS6jbWP8tVKp0jp+NO5n8WtMUAnNnGoJKi4w==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>

<div class="row">
  <span class="glueckskeks"></span>
</div>

<div class="glueckskeks">
  <button class="button" onclick="neuerGlueckskeks()">
    Neuer Glückskeks
  </button>
</div>

<script>
$(document).ready(function(){
  neuerGlueckskeks();
});

var neuerGlueckskeks = function(){
  var index = Math.floor(Math.random() * glueckskeksQuotes.length);
  
  $('span.glueckskeks').html('"' + glueckskeksQuotes[index] + '"');
};

var glueckskeksQuotes = [
  "Gib jedem Tag die Chance, der schönste deines Lebens zu werden.",
  "Was uns den Weg verlegt, bringt uns voran.",
  "Auch eine Reise von 1000 Meilen fängt mit dem ersten Schritt an.",
  "Wer sich darauf versteht, das Leben zu genießen, braucht keine Reichtümer.",
  "Entfernung ist nichts. Sich nah zu sein, ist eine Sache des Herzens.",
  "Glück ist, Zeit mit einem Menschen zu verbringen, der aus einem ganz normalen Tag, etwas Besonderes macht.",
  "Warte nicht immer bis andere sich entschieden haben, sondern treffe deine eigenen Entscheidungen.",
  "Wenn du an dich glaubst und hart arbeitest, wirst du alles erreichen, was du willst.",
  "Ein Tag ohne dich, ist wie ein Glückskeks ohne Spruch.",
  "Zusammen ist man weniger allein"
]
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen / Seiten
2.  Klicke auf  + Box / Seite hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

