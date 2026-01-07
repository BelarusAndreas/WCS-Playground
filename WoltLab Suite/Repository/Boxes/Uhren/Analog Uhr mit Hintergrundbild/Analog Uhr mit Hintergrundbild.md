### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
$size: 200px;
@keyframes rotateArms {
    from {transform: rotate(0);}
    to {transform: rotate(360deg);}
}
@-webkit-keyframes rotateArms {
    from {transform: rotate(0);}
    to {transform: rotate(360deg);}
}
@-moz-keyframes rotateArms {
    from {transform: rotate(0);}
    to {transform: rotate(360deg);}
}
.clock {
  width:$size;
  height:$size;
  box-shadow: 0px 0px 0px 7px #000;
  border-radius:$size;
  position: relative;
  background: url(https://cdn.pixabay.com/photo/2017/12/24/00/13/abstract-background-3036235_1280.jpg);
  background-size: 100% 100%;
}
.center, .minute-lines > div {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  -webkit-transform: translate(-50%, -50%);
  -moz-transform: translate(-50%, -50%);
}
.knob {
  width: $size/15;
  height: $size/15;
  background: #111;
  border-radius: $size/15;
  z-index:4;
}
.arm {
  position:absolute;
  top:50%;
  left:50%;
  transform-origin: top left 0;
  -webkit-transform-origin: top left 0;
  -moz-transform-origin: top left 0;
  z-index:2;
  width:0;
  animation: rotateArms linear 60s infinite;
  -webkit-animation: rotateArms linear 60s infinite;
  -moz-animation: rotateArms linear 60s infinite;
}
.minute.arm {
  height:$size/2.6;
  box-shadow:0 0 0 $size/128 #fff;
  animation-duration: 60s * 60;
  -webkit-animation-duration: 60s * 60;
  -moz-animation-duration: 60s * 60;
}
.hour.arm {
  height:$size/3.6;
  box-shadow: 0 0 0 $size/128 #fff;
  animation-duration: 60s * 60 * 12;
  -webkit-animation-duration: 60s * 60 * 12;
  -moz-animation-duration: 60s * 60 * 12;
}
.second.arm {
  height:$size/2.2;
  box-shadow: 0 0 0 $size/150 #ff0000;
}
.box {
  position:absolute;
  top:0;
  left:0;
  width:100%;
  height:100%;
}
@for $i from 0 through 29 {
  .minute-lines > .min-#{$i} {
    transform: rotate($i * 6deg);
    -moz-transform: rotate($i * 6deg);
    -webkit-transform: rotate($i * 6deg);
  }
}
.minute-lines {
  width:100%;
  height:100%;
}
.minute-lines > div::before, .minute-lines > div::after {
  content:"";
  position:absolute;
  width:0px;
  height: $size/40;
  top: $size/2.25;
  box-shadow: 0px 0px 0px 0.5px #fff;
}
.minute-lines > div::after {
  bottom: $size/2.25;
  top:auto;
}
div.long::before, div.long::after {
  height: $size/22;
  top: $size/2.3675;
}
div.long::after {
  bottom: $size/2.3675;
  top:auto;
}
div.dark::before, div.dark::after {
  box-shadow: 0px 0px 0px 1px #000;
}
</style>

<div class="clock center">
  <div class="knob center"></div>
  <div class="box seconds">
    <div class="arm second"></div>
  </div>
  <div class="box minutes">
    <div class="arm minute"></div>
  </div>
  <div class="box hours">
    <div class="arm hour"></div>
  </div>
  <div class="minute-lines">
    <div class="min-0 long dark"></div>
    <div class="min-1"></div>
    <div class="min-2"></div>
    <div class="min-3"></div>
    <div class="min-4"></div>
    <div class="min-5 dark"></div>
    <div class="min-6"></div>
    <div class="min-7"></div>
    <div class="min-8"></div>
    <div class="min-9"></div>
    <div class="min-10 dark"></div>
    <div class="min-11"></div>
    <div class="min-12"></div>
    <div class="min-13"></div>
    <div class="min-14"></div>
    <div class="min-15 long dark"></div>
    <div class="min-16"></div>
    <div class="min-17"></div>
    <div class="min-18"></div>
    <div class="min-19"></div>
    <div class="min-20 dark"></div>
    <div class="min-21"></div>
    <div class="min-22"></div>
    <div class="min-23"></div>
    <div class="min-24"></div>
    <div class="min-25 dark"></div>
    <div class="min-26"></div>
    <div class="min-27"></div>
    <div class="min-28"></div>
    <div class="min-29"></div>
  </div>
</div>

<script>
var date = new Date();
var seconds = date.getSeconds() * 6;
var minutes = date.getMinutes() * 6 + seconds/60;
var hours = (180 + date.getHours()%12 * 30 + minutes / 15);
document.querySelector(".box.seconds").style.transform = "rotate(" + (180 + seconds) + "deg)"; 
document.querySelector(".box.minutes").style.transform = "rotate(" + (180 + minutes) + "deg)"; document.querySelector(".box.hours").style.transform = "rotate(" + hours + "deg)"; 
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

