

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] .egg{
    width: 200px;
    height: 280px;
    margin: auto;
    background: #FFFEFC;
    border-radius: 50%/60% 60% 40% 40%;
    box-shadow: 0 0 20px gray;
}
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] form, 
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] fieldset, 
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] input, 
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] label, 
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] #result {
    color: #000;
    margin: auto;
}
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] form, 
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] fieldset {
    border: none;
}
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] form{
     display: flex;
     padding:20px;
     text-align: center;
}
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] legend{
     display:none;
}
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] input[type=button]{
     width: 100px;
     height: 100px;
     line-height: 40px;
     border: 3px solid #F28100;
     border-radius: 50%;
     color: #000;
     text-align: center;
     text-decoration: none;
     background: #FFB508;
     box-shadow: 0 0 3px #000;
     font-size: 20px;
     font-weight: bold;
     outline: none;
}
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] button:hover, 
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] input[type=button]:hover {
     background: #F28100 !important;
}
:focus {outline:none;}
::-moz-focus-inner {border:0;}
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] #result {
     font-size:20px;
     font-weight: bold;
     line-height: 1.2;
}
</style>

<div class="egg">
<form method="post" id="radio-demo">
  <fieldset id="ready">
    <legend>Egg timer</legend><br>
    <input type="radio" name="time" value="3" />
    <label for="radio"><strong>Weich</strong></label>
    <br><br>
    <input type="radio" name="time" value="6" />
    <label for="radio"> <strong>Mittel</strong></label>
    <br><br>
    <input type="radio" name="time" value="9" />
    <label for="radio"> <strong>Hart</strong></label>
    <br><br>
    <input type="button" value="Start" onclick="setTimer()"/>
  </fieldset>
  <fieldset id="counting" style="display:none">
     <br><br><br>
     <div id="result"></div>
     <br><br><br>
     <input type="button" value="Stop" onclick="cancelTimer()"/>
  </fieldset>
</form>
</fiv>
    
<script>
  var cancel; 
  var audio = new   Audio('URL-ZUR-AUDIODATEI.mp3');
function setTimer() {
    cancel = false;
    document.getElementById("ready").style.display = "none";
    document.getElementById("counting").style.display = "block";
    var radio = document.getElementsByName("time");
    for (var i = 0, length = radio.length; i < length; i++) {
      if (radio[i].checked) {
        var totalMinutes = Number(radio[i].value);
        break;
      }
    }
    var totalTime = totalMinutes * 60;
    function countdown()  {
      var minutes = Math.floor(totalTime / 60);
      var seconds = totalTime - minutes * 60;
      totalTime--;
      var counter = document.getElementById("result");
      counter.innerHTML = String(minutes) + ":" + (seconds < 10 ? "0" : "") + String(seconds);
      if (cancel) {
        return;
      }
      if ( totalTime >= 0 ) {
        setTimeout(countdown, 1000);
      } else {
           audio.loop = true;
           audio.play();
           counter.innerHTML = "Fertig!";
      }
    }
    countdown();
  }
  function cancelTimer() {
    cancel = true;
    audio.loop = false;
    document.getElementById("counting").style.display = "none";
    document.getElementById("ready").style.display = "block";
  }
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
