

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.slide-nav-left {
    position: absolute;
    top: 55%;
    left: 0%;
    transform: translate(0%,-50%);    
    background: #000;
    opacity: 0.5;
}
.slide-nav-right {
    position: absolute;
    top: 55%;
    right: 0%;
    transform: translate(0%,-50%);
    background: #000;
    opacity: 0.5;
}
</style>

<div class="slider">
  <img class="slide" src="DEINE_URL_ZUM_BILD" style="width:100%">
  <img class="slide" src="DEINE_URL_ZUM_BILD" style="width:100%">
  <img class="slide" src="DEINE_URL_ZUM_BILD" style="width:100%">
  <img class="slide" src="DEINE_URL_ZUM_BILD" style="width:100%">
  <img class="slide" src="DEINE_URL_ZUM_BILD" style="width:100%">

  <button class="slide-nav-left" onclick="plusDivs(-1)">&#10094;</button>
  <button class="slide-nav-right" onclick="plusDivs(1)">&#10095;</button>
</div>

<script>
var slideIndex = 1;
  showDivs(slideIndex);
function plusDivs(n) {
  showDivs(slideIndex += n);
}
function showDivs(n) {
  var i;
  var x = document.getElementsByClassName("slide");
  if (n > x.length) {slideIndex = 1}
  if (n < 1) {slideIndex = x.length}
  for (i = 0; i < x.length; i++) {
    x[i].style.display = "none";  
  }
  x[slideIndex-1].style.display = "block";  
}
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
