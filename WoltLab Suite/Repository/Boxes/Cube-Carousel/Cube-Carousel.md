### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
:root {
  --color-primary: dimgray;
  --rotation-speed: 1s;
}
.container {
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  perspective: 800px;
  perspective-origin: 50%;
}
.image-cube {
  width: 300px;
  height: 300px;
  transform-style: preserve-3d;
  position: relative;
  transition: var(--rotation-speed);
}
.image-cube div {
  height: 300px;
  width: 300px;
  position: absolute;
  background-size: cover;
  background-position: 50% 50%;
  border: 3px solid white;
  -webkit-box-reflect: below -3px linear-gradient(to bottom, rgba(0,0,0,0) 80%, rgba(0,0,0,0.15));
}
/* Bilder */
.front {
  background-image: url('URL_ZUM_BILD_1');       /* URL zum Bild 1 anpassen */
  transform: translateZ(150px);
}
.right {
  background-image: url('URL_ZUM_BILD_2');       /* URL zum Bild 2 anpassen */
  transform: rotateY(-270deg) translateX(150px);
  transform-origin: 100% 0;
}
.back {
  background-image: url('URL_ZUM_BILD_3');       /* URL zum Bild 3 anpassen */
  transform: translateZ(-150px) rotateY(180deg);
}
.left {
  background-image: url('URL_ZUM_BILD_4');       /* URL zum Bild 4 anpassen */
  transform: rotateY(270deg) translateX(-150px);
  transform-origin: 0 50%;
}
</style>

<div class="container">
  <div class="image-cube">
    <div class="front"></div>
    <div class="right"></div>
    <div class="back"></div>
    <div class="left"></div>
  </div>
</div>
    
<script>
let con = document.querySelector('.container'),
    cube = document.querySelector(".image-cube"),
    switch_delay = 3000 //milli-seconds
let pos = 0;
function autoClick() {
  pos -= 90;
  cube.style.transform = `rotateY(${pos}deg)`;
}
autoClick()
let autoRun = setInterval(autoClick, switch_delay)
con.addEventListener('mouseenter', function(){
  clearInterval(autoRun)
})
con.addEventListener('mouseleave', function(){
  autoRun = setInterval(autoClick, switch_delay)
})
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

