
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.splitview {
    position: relative;
    width: 100%;
    min-height: 45vw;
    overflow: hidden;
}
.panel {
    position: absolute;
    width: 100vw;
    min-height: 45vw;
    overflow: hidden;
}
.panel .content {
    position: absolute;
    width: 100vw;
    min-height: 45vw;
    color: #FFF;
}
.panel .description {
    width: 25%;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    text-align: center;
}
.panel img {
    width: 35%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.bottom {
    background-color: rgb(44, 44, 44);
    z-index: 1;
}
.bottom .description {
    right: 5%;
}
.top {
    background-color: #161E2B;
    z-index: 2;
    width: 50vw;
}
.top .description {
    left: 5%;
}
.handle {
    height: 100%;
    position: absolute;
    display: block;
    background-color: #B51836;
    width: 5px;
    top: 0;
    left: 50%;
    z-index: 3;
}
.skewed .handle {
    top: 50%;
    transform: rotate(30deg) translateY(-50%);
    height: 200%;
    -webkit-transform-origin: top;
    -moz-transform-origin: top;
    transform-origin: top;
}
.skewed .top {
    transform: skew(-30deg);
    margin-left: -1000px;
    width: calc(50vw + 1000px);
}
.skewed .top .content {
    transform: skew(30deg);
    margin-left: 1000px;
}
</style>

<div class="splitview skewed">
  <div class="panel bottom">
    <div class="content">
      <div class="description">
        <h1>Titel</h1>
        <p>Beschreibung</p>
      </div>
      <img src="https://cdn.pixabay.com/photo/2016/12/30/07/59/kitchen-1940174_1280.jpg" alt="Before">
    </div>
  </div>
  <div class="panel top">
    <div class="content">
      <div class="description">
        <h1>Titel</h1>
        <p>Beschreibung</p>
      </div>
      <img src="https://cdn.pixabay.com/photo/2017/06/13/22/42/kitchen-2400367_1280.jpg" alt="After">
    </div>
  </div>
  <div class="handle"></div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    var parent = document.querySelector('.splitview'),
        topPanel = parent.querySelector('.top'),
        handle = parent.querySelector('.handle'),
        skewHack = 0,
        delta = 0;
    if (parent.className.indexOf('skewed') != -1) {
        skewHack = 1000;
    }
    parent.addEventListener('mousemove', function(event) {
        delta = (event.clientX - window.innerWidth / 2) * 0.5;
        handle.style.left = event.clientX + delta + 'px';
        topPanel.style.width = event.clientX + skewHack + delta + 'px';
    });
});
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen / Seiten
2.  Klicke auf  + Box / Seite hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
