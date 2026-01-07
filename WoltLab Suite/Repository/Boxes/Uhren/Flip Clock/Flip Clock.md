
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.clock{  font-size: 32pt;  color: #aaa;  position: absolute;  text-align: center;  top: 50%;  left:50%;  margin: -128px 0 0 -310px;
}
.clock p {  padding: 20px 10px;  background: #000;
}
.clock p span{  background: #444444;  background: -webkit-gradient(linear, 0 0, 0 100%, from(#444444), to(#111111));  background: -webkit-linear-gradient(#444444 0%, #111111 100%);  background: -moz-linear-gradient(#444444 0%, #111111 100%);  background: -o-linear-gradient(#444444 0%, #111111 100%);  background: linear-gradient(#444444 0%, #111111 100%);  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#444444', endColorstr='#111111',GradientType=0 );  text-shadow: 1px 2px 5px #000, 0px -1px 0px #FFF;  padding: 10px 15px;  margin: 0 0 0 5px;
}
</style>

<div class="clock">  <p>    <span id="h0">0</span>    <span id="h1">0</span>:    <span id="m0">0</span>    <span id="m1">0</span>  </p>
</div>

<script>
setTime();
this.setInterval(function(){  setTime();
},1000);
function setTime(){  var date = new Date();  var h = ''+date.getHours();  var m = ''+date.getMinutes();    if(h.length === 1){    document.getElementById('h0').innerHTML = '0';    document.getElementById('h1').innerHTML = h;  } else {    document.getElementById('h0').innerHTML = h.charAt(0);    document.getElementById('h1').innerHTML = h.charAt(1);  }  if(m.length === 1){    document.getElementById('m0').innerHTML = '0';    document.getElementById('m1').innerHTML = m;  } else {    document.getElementById('m0').innerHTML = m.charAt(0);    document.getElementById('m1').innerHTML = m.charAt(1);  }
}
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
