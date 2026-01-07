

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.poo {
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%); 
  justify-content: center;
  margin-top: 45px;
}
.you-found-us {
    height: 25px;
    margin-bottom: 25px;
}
.then-donate-us {
    height: 25px;
    position: relative;
    bottom: 0;
}
.donate-button {
    width: 100%;
    text-align: center;
}
.spot {
  margin: auto;
  background-color: #93540b;
  height: 20px;
  width: 60px;
  border-radius: 10px 10px 7px 7px;
  box-shadow: inset 0 -5px 7px rgba(0, 0, 0, 0.3);
}
.top {
  height: 15px;
  width: 20px;
  border-radius: 10px 0 5px 5px;
}
.middle {
  width: 45px;
}
.fly {
  margin-left: 35%;
  position: absolute;
  top: 50%;
  left: 50%;
  width: 7px;
  height: 5px;
  background-color: #000;
  border-radius: 5px;
  animation: fly 3s linear infinite;
  &:before {
      position: absolute;
      top: -3px;
      left: 2px;
      content: '';
      height: 2px;
      width: 5px;
      background-color: #edece3;
      border-radius: 100% 50% 50% 0; 
      border: 1px solid black;
      animation: flywing 0.3s linear infinite;
  }
}
@keyframes flywing {
  0% {
    height: 2px;
    top: -3px;
  }
  100% {
    height: 0px;
    top: -1px;
  }
}
@keyframes fly {
  0% {
    left: 80px;
    top: 0px;
    transform: scaleX(1);
  }
  25% {
    left: 30px;
    top: -10px;
    transform: scaleX(1);
  }
  50% {
    left: -20px;
    top: 0px;
    transform: scaleX(1);
  }
  51% {
    left: -20px;
    top: 0px;
    transform: scaleX(-1);
  }
  75% {
    left: 30px;
    top: 10px;
    transform: scaleX(-1);
  }
  100% {
    left: 80px;
    top: 0px;
    transform: scaleX(-1);
  }
}
</style>

<p class="you-found-us">Du findest uns ...</p>
<div class="poo">
    <div class="spot top"></div>
    <div class="spot middle"></div>
    <div class="spot bottom1"></div>
    <div class="fly"></div>
</div>
<p class="then-donate-us">Dann spende und wir machen es besser :)</p>
<br>
<button class="button donate-button"><a href="#">Jetzt spenden</a></button>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
