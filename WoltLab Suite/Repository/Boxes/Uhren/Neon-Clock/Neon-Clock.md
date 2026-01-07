
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.clock {    transform: translateX(-50%) translateY(-50%);    color: #17D4FE;    font-size: 60px;    letter-spacing: 7px;
}
</style>

<div id="neonclock" class="neonclock" onload="showTime()"></div>

<script>  function showTime(){    var date = new Date();    var h = date.getHours();    var m = date.getMinutes();    var s = date.getSeconds();      if(h == 0){        h = 24;    }      h = (h < 10) ? "0" + h : h;    m = (m < 10) ? "0" + m : m;    s = (s < 10) ? "0" + s : s;        var time = h + ":" + m + ":" + s; document.getElementById("neonclock").innerText = time;   document.getElementById("neonclock").textContent = time;      setTimeout(showTime, 1000);   }
showTime();
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
