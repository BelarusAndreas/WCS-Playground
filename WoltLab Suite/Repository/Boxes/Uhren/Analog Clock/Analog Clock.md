### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.clock {  position: relative;  width: 300px;  height: 300px;  background: #fff;  border: 15px solid #000;  border-radius: 50%;
}
.clock::after {  position: absolute;  top: calc(50% - 11px);  left: calc(50% - 11px);  display: block;  width: 14px;  height: 14px;  background: #fff;  border: 4px solid #ff0000;  border-radius: 50%;  content: '';
}
.needle {  position: absolute;  transform-origin: 50% bottom;
}
.hours {  top: 55px;  left: calc(50% - 5px);  height: 80px;  width: 10px;  background: black;  border-radius: 10px;
}
.minutes {  top: 35px;  left: calc(50% - 3px);  height: 100px;  width: 6px;  background: #000;  border-radius: 5px;
}
.seconds {  top: 15px;  left: calc(50% - 2px);  height: 150px;  width: 4px;  background: #ff0000;  border-radius: 5px;  transform-origin: 50% 120px;
}
.seconds::after {  position: absolute;  bottom: 0;  left: -2px;  display: block;  width: 8px;  height: 8px;  background: #ff0000;  border-radius: 50%;  content: '';
}
</style>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.1.1/jquery.min.js" integrity="sha512-U6K1YLIFUWcvuw5ucmMtT9HH4t0uz3M366qrF5y4vnyH6dgDzndlcGvH/Lz5k8NFh80SN95aJ5rqGZEdaQZ7ZQ==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>

<div class="clock">  <div class="needle hours"></div>  <div class="needle minutes"></div>  <div class="needle seconds"></div>
</div>

<script>
var Clock = function() {  var ui = {    hours: {      element: $('.hours'),      divider: 12    },    minutes: {      element: $('.minutes'),      divider: 60    },    seconds: {      element: $('.seconds'),      divider: 60    }  };    var d, hours, minutes, seconds, needles;  var rotateNeedle = function(needle, time) { ui[needle].element.css('transform', 'rotateZ(' + time * 360 / ui[needle].divider + 'deg)');  };  var setClock = function() {    d = new Date();    hours = d.getHours() > 12 ? d.getHours() - 12 : d.getHours();    minutes = d.getMinutes();    seconds = d.getSeconds();    needles = {      'hours': hours + minutes / ui.minutes.divider,      'minutes': minutes + seconds / ui.seconds.divider,      'seconds': seconds    };    for (var needle in needles) {      rotateNeedle(needle, needles[needle]);    }  };  var checkTime = function() {    setInterval(function() {      setClock();    }, 1000);  };  return {    init: function() {      setClock();      checkTime();    }  }
}()
Clock.init();
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

