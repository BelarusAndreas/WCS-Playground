### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.boxContent {    text-align: center;
}
.clockTime {    font-size: 28px;    font-weight: 600;
}
</style>    <div>  <div class="clockTime"></div>  <div class="clockDate"></div>
  <script>  (function (script) {    const displayTime = script.parentNode.querySelector('.clockTime');    const displayDate = script.parentNode.querySelector('.clockDate');    const dateFormat = new Intl.DateTimeFormat(        document.documentElement.lang,        { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' }    );    const timeFormat = new Intl.DateTimeFormat(        document.documentElement.lang,        { hour: 'numeric', minute: 'numeric', second: 'numeric' }    );        function update() {        const now = new Date();        displayTime.innerHTML = `        ${timeFormat.format(now)}        `;        displayDate.innerHTML = `        ${dateFormat.format(now)}        `;    }        update();    setInterval(() => { requestAnimationFrame(update); }, 500);    })(document.currentScript);  </script>
</div>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

