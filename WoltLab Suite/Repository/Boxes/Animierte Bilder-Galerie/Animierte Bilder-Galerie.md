
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.wrapper{
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
}
.items{
    display: flex;
    gap: 0.4rem;
    perspective: calc(var(--index) * 35);
}
.item{
    width: calc(var(--index) * 3);
    height: calc(var(--index) * 12);
    background-color: #222;
    background-size: cover;
    background-position: center;
    cursor: pointer;
    filter: grayscale(1) brightness(.5);
    transition: transform 1.25s var(--transition), filter 3s var(--transition), width 1.25s var(--transition);
    will-change: transform, filter, rotateY, width;
}
.item::before, .item::after{
    content: '';
    position: absolute;
    height: 100%;
    width: 20px;
    right: calc(var(--index) * -1);
}
.item::after{
    left: calc(var(--index) * -1);
}
.items .item:hover{
    filter: inherit;
    transform: translateZ(calc(var(--index) * 10));
}
.items .item:hover + *{
    filter: inherit;
    transform: translateZ(calc(var(--index) * 8.5)) rotateY(35deg);
    z-index: -1;
}
.items .item:hover + * + *{
    filter: inherit;
    transform: translateZ(calc(var(--index) * 5.6)) rotateY(40deg);
    z-index: -2;
}
.items .item:hover + * + * + *{
    filter: inherit;
    transform: translateZ(calc(var(--index) * 2.5)) rotateY(30deg);
    z-index: -3;
}
.items .item:hover + * + * + * + *{
    filter: inherit;
    transform: translateZ(calc(var(--index) * .6)) rotateY(15deg);
    z-index: -4;
}
.items .item:has( + :hover){
    filter: inherit;
    transform: translateZ(calc(var(--index) * 8.5)) rotateY(-35deg);
}
.items .item:has( + * + :hover){
    filter: inherit;
    transform: translateZ(calc(var(--index) * 5.6)) rotateY(-40deg);
}
.items .item:has( + * + * + :hover){
    filter: inherit;
    transform: translateZ(calc(var(--index) * 2.5)) rotateY(-30deg);
}

.items .item:has( + * + * + * + :hover){
    filter: inherit;
    transform: translateZ(calc(var(--index) * .6)) rotateY(-15deg);
}
.items .item:active, .items .item:focus {
    width: 28vw;
    filter: inherit;
    z-index: 100;
    transform: translateZ(calc(var(--index) * 10));
    margin: 0 .45vw;
}
</style>

<!-- "DEINE_URL_ZUM_BILD" ist mit der URL des gewünschten Bilds zu ersetzen -->
<div class="wrapper">
  <div class="items">
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
    <div class="item" tabindex="0" style="background-image: url(DEINE_URL_ZUM_BILD)"></div>
  </div>
</div>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
