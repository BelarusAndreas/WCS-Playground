
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
@font-face {  font-family: 'Digital-7';  src: url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/184191/Digital-7.eot?#iefix') format('embedded-opentype'),  url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/184191/Digital-7.woff') format('woff'), url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/184191/Digital-7.ttf')  format('truetype'), url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/184191/Digital-7.svg#Digital-7') format('svg');    font-weight: normal;    font-style: normal;
}
figure {    width: 210px;    height: 210px;    position: absolute;    top: 50%;    left: 50%;    margin-top: -105px;    margin-left: -105px;    transform-style: preserve-3d;    -webkit-transform-style: preserve-3d;    -webkit-transform: rotateX(-35deg) rotateY(45deg);    transform: rotateX(-35deg) rotateY(45deg);    transition: 2s;
}
.face {    width: 100%;    height: 100%;    position: absolute;    -webkit-transform-origin: center;    transform-origin: center;    background: #000;    text-align: center;
}
p {    font-size: 180px;    font-family: 'Digital-7';    margin-top: 20px;    color: #2982FF;    text-shadow: 0px 0px 5px #000;    -webkit-animation: color 10s infinite;    animation: color 10s infinite;    line-height: 180px;
}
.front {    -webkit-transform: translate3d(0, 0, 105px);    transform: translate3d(0, 0, 105px);    background: #111;
}
.left {    -webkit-transform: rotateY(-90deg) translate3d(0, 0, 105px);    transform: rotateY(-90deg) translate3d(0, 0, 105px);    background:#151515;
}
.top {    -webkit-transform: rotateX(90deg) translate3d(0, 0, 105px);    transform: rotateX(90deg) translate3d(0, 0, 105px);    background:#222;
}
@keyframes color{  0%{color:#2982ff;text-shadow:0px 0px 5px #000;}  50%{color:#cc4343;text-shadow:0px 0px 5px #ff0000;}
}
@-webkit-keyframes color{  0%{color:#2982ff;text-shadow:0px 0px 5px #000;}  50%{color:#cc4343;text-shadow:0px 0px 5px #ff0000;}
}
</style>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.3/jquery.min.js" integrity="sha512-egJ/Y+22P9NQ9aIyVCh0VCOsfydyn8eNmqBy+y2CnJG+fpRIxXMS6jbWP8tVKp0jp+NO5n8WtMUAnNnGoJKi4w==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>

<figure>  <div class="face top">    <p id="s"></p>  </div>  <div class="face front">    <p id="m"></p>  </div>  <div class="face left">    <p id="h"></p>  </div>
</figure>

<script>
function date_time(id) {    date = new Date;    h = date.getHours();    if(h<10) {       h = "0"+h;    }    m = date.getMinutes();    if(m<10) {       m = "0"+m;    }    s = date.getSeconds();    if(s<10) {       s = "0"+s;    }    document.getElementById("s").innerHTML = ''+s;    document.getElementById("m").innerHTML = ''+m;    document.getElementById("h").innerHTML = ''+h;    setTimeout('date_time("'+"s"+'");','1000');    return true;
}
window.onload = date_time('s');
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
