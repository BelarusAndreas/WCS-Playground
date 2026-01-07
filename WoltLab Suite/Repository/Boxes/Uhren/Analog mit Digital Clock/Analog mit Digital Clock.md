### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.clock {    width: 500px;    height: 500px;    border-radius: 500px;    position: relative;    margin: 10px auto;    background-image: url(https://i.imgur.com/bXOJmcx.png), url(http://textures101.com/textures/Plastic/Other_Plastic/2012/2/26/tn1_BlackPlasticTexturebyShadowRunner27_zzguh.jpg);
}
.hours {    width: 5px;    height: 110px;    position: absolute;    background: #fff;    border-radius: 500px;    left: calc(50% - 2.5px);    top: 140px;    z-index: 6;    transform-origin: bottom center;    box-shadow: 0 0 4px; rgba(0,0,0,0.4);
}
.minutes {    width: 5px;    height: 210px;    position: absolute;    background: #fff;    border-radius: 500px;    z-index: 6;    left: calc(50% - 2.5px);    top: 40px;    transform-origin: bottom center;    box-shadow: 0 0 4px; rgba(0,0,0,0.4);
}
.seconds {    width: 3px;    height: 220px;    position: absolute;    background: red;    box-shadow: 0 0 4px; rgba(0,0,0,0.4);    border-radius: 500px;    left: calc(50% - 1.5px);    top: 30px;    z-index: 15;    transform-origin: bottom center;
}
.circle {    width: 18px;    height: 18px;    background: red;    z-index: 25;    border-radius: 20px;    position: absolute;    left: calc(50% - 9px);    top: calc(50% - 9px);
}
p {  text-align: center;  font-size: 16px;  color: #000;  position: absolute;  left: 17%;  top: calc( 50% - 14px );  margin:0;  background: #fff;  padding: 5px 10px;  width: 90px;  font-weight: 600;  border-radius: 100px;  box-shadow: inset 2px 2px 5px rgba(0,0,0, 0.6);
}
.author {  text-align: center;  color: #fff;  text-transform: uppercase;  position: absolute;  top: 150px;  width: 100%;  font-weight: 600;  font-size: 12px;  letter-spacing: 4px;  opacity: 0.2;
}
</style>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.min.js" integrity="sha512-bnIvzh6FU75ZKxp0GXLH9bewza/OIw6dLVh9ICg0gogclmYGguQJWl8U30WpbsGTqbIiAwxTsbe76DErLq5EDQ==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>

<div class="clock">  <div class="hours"></div>  <div class="minutes"></div>  <div class="seconds"></div>  <div class="circle"></div>  <p id="timer"></p>  <span class="author">DEIN_SEITENNAME</span>
</div>

<script>
var timer = document.getElementById('timer');
var loop;
function time(){    var now = new Date();    var h = now.getHours();    var m = now.getMinutes();    var s = now.getSeconds();    var h1 = (now.getHours() / 12) * 360;    var m1 = now.getMinutes() * 6;    var s1 = now.getSeconds() * 6;        timer.innerHTML = h+' : '+m+'</span> : <span>'+s+'</span>'; $('.hours').css('transform','rotate('+ h1 +'deg)');   $('.minutes').css('transform','rotate('+ m1 +'deg)');   $('.seconds').css('transform','rotate('+ s1 +'deg)');
}
loop = setInterval(time, 1000);
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

