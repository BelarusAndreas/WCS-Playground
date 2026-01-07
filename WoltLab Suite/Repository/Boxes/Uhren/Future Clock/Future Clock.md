### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style id="clock-animations"></style>
<style>
.clockContainer {
    position: relative;
    margin-left: -65px;
    margin-top: -100px;
    height: 300px !important;
}
.clock {
  width: 400px;
  height: 400px;
  background: #0D181A;
  border-radius: 50%;
  position: relative;
  transform: scale(0.5);
}
.seconds-wrapper, .hours-wrapper {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}
#seconds {
  width: 100%;
  height: 100%;
  position: relative;
}
#hours {
  width: 100%;
  height: 100%;
  position: relative;
}
.second {
  width: 6px;
  height: 1px;
  background: #02C9AE;
  position: absolute;
  left: 40%;
  transform: translateX(-50%);
  opacity: 0.4;
}
.hour {
  width: 15px;
  height: 1px;
  background: #02C9AE;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
}
.hand {
  position: absolute;
  left: 50%;
  top: 50%;
  transform-origin: 50% 0;
  background: #02C9AE;
  z-index: 10;
}
.second-hand {
  width: 1px;
  height: 120px;
  background: #0B4A4B;
  transition: 0.5s;
  animation: rotate-second 60s linear infinite;
}
.minute-hand {
  width: 1px;
  height: 120px;
  background: #0B4A4B;
  transition: .5s;
  animation: rotate-minute 3600s linear infinite;
}
.hour-hand {
  width: 1px;
  height: 80px;
  background: #0B4A4B;
  transition: .5s;
  animation: rotate-hour 43200s linear infinite;
}
.minute-hand-cap, .hour-hand-cap {
  width: 3px;
  height: 30px;
  background: #02C9AE;
  position: absolute;
  top: 76%;
  left: -1px;
}
.hour-hand-cap {
  top: 64%;
}
.center-point {
  position: absolute;
  width: 15px;
  height: 15px;
  background: #02C9AE;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 50%;
  z-index: 99;
}
.center-point-border {
  position: absolute;
  width: 35px;
  height: 35px;
  background: none;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 50%;
  border: 1px solid #02C9AE;
}
.calendar-wrapper {
  position: absolute;
  width: 80px;
  height: 80px;
  top: 60%;
  left: 50%;
  transform: translateX(-50%);
}
.calendar {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  position: relative;
  opacity: 0.6;
}
.calendar-year {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  font-family: 'Montserrat';
  font-size: 14px;
  font-weight: 600;
  letter-spacing: 0.05em;
  color: #02C9AE;
  background: #0D181A;
  padding: 0 2px;
}
.calendar-day {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  font-family: 'Montserrat';
  font-size: 28px;
  font-weight: 500;
  letter-spacing: 0.1em;
  color: #02C9AE;
}
.calendar-weekday {
  position: absolute;
  left: 50%;
  top: 80%;
  transform: translateX(-50%);
  font-family: 'Montserrat';
  font-size: 14px;
  font-weight: 600;
  letter-spacing: 0.01em;
  color: #02C9AE;
  background: #0D181A;
  padding: 0 4px;
  text-transform: uppercase;
}
.cal-division {
  width: 3px;
  height: 1px;
  background: #02C9AE;
  position: absolute;
  left: 40%;
  transform: translateX(-50%);
  opacity: 0.5;
}
.bg-gradient {
  position: absolute;
  width: 325px;
  height: 325px;
  background: linear-gradient(to bottom, #0499a9 0%,#0d181a 100%);
  top:50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 50%;
  opacity: 0.1;
}
.center-gradient {
  position: absolute;
  width: 120px;
  height: 120px;
 background: linear-gradient(to bottom, #0499a9 0%,#0d181a 55%);
  top:50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 50%;
  opacity: 0.07;
}
.seconds-animation-wrapper {
  position: absolute;
  width: 380px;
  height: 380px;
  top:50%;
  left: 50%;
  transform: translate(-50%, -50%); 
}
.seconds-animation {
  box-sizing: border-box;
  width: 100%;
  height: 100%;
  background: none;
  border-radius: 50%;
  background:  conic-gradient(#0d181a, #06eceb, #047da6);
  opacity: 0.3;
  transition: 0.5s;
  animation: sec-animation 60s linear infinite;
}
.seconds-animation:after {
  content: '';
  display: block;
  position: absolute;
  width: 325px;
  height: 325px;
  border-radius: 50%;
  background: #0d181a;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>

<div class="clockContainer">
    <div id ="clock" class="clock">
      <div class="seconds-animation-wrapper">
        <div class="seconds-animation"></div>
      </div>
       <div class="calendar-wrapper">
        <div id="calendar" class="calendar">
          <div id="cal-year" class="calendar-year">2020</div>
          <div id="cal-day" class="calendar-day">31</div>
          <div id="cal-weekday" class="calendar-weekday">Fri</div>
        </div>
      </div>
      <div class="center-gradient"></div>
      <div class="bg-gradient"></div>
      <div class="seconds-wrapper">
        <div id="seconds">
         </div>
      </div>
       <div class="hours-wrapper">
         <div id="hours">
         </div>
      </div>
      <div id="sec" class="hand second-hand"></div>
      <div id="min" class="hand minute-hand">
        <div class="minute-hand-cap"></div>
      </div>
      <div id="hr" class="hand hour-hand">
        <div class="hour-hand-cap"></div>
      </div>
      <div class="center-point"></div>
      <div class="center-point-border"></div>
    </div>
  </div>

<script>
function setSecondsDivision() {
    for (let i = 0; i < 60; i++) {
     let seconds = document.getElementById('seconds');
     seconds.insertAdjacentHTML( 'afterbegin', '<div class="second second_' + i +'"></div>' );
   }
  var seconds = document.getElementsByClassName('second');
  var angle = 0;
  var step = (2*Math.PI)/seconds.length;
  var width = 400;
  var height = 400;
  var degValue = 0;
  for (let i = 0; i < 60; i++) {
    var x = width/2 + 175*Math.cos(angle);
    var y = height/2 + 175*Math.sin(angle);
    seconds[i].style.left = x - 3 + 'px';
    seconds[i].style.top = y + 'px';
    seconds[i].style.transform = "rotate("+ degValue +"deg)";
    angle += step;
    degValue += 6;
  }
}
setSecondsDivision();
function setHoursDivision() {
  for (let i = 0; i < 12; i++) {
   let hours = document.getElementById('hours');
   hours.insertAdjacentHTML( 'afterbegin', '<div class="hour hour_' + i +'"></div>' );
 }
  var hours = document.getElementsByClassName('hour');
  var angle = 0;
  var step = (2*Math.PI)/hours.length;
  var width = 400;
  var height = 400;
  var degValue = 0;
  console.log(hours);
  for (let i = 0; i < 12; i++) {
    var x = width/2 + 150*Math.cos(angle);
    var y = height/2 + 150*Math.sin(angle);
    hours[i].style.left = x - 8 + 'px';
    hours[i].style.top = y + 'px';
    hours[i].style.transform = "rotate("+ degValue +"deg)";
    angle += step;
    degValue += 30;
  }
}
setHoursDivision();
(function(){
  var date = new Date(); 
  var hourDeg   = date.getHours() / 12 * 360 + date.getMinutes() / 60 * 30 + 180;
  var minuteDeg = date.getMinutes() / 60 * 360 + date.getSeconds() / 60 * 6 + 180;
  var secondDeg = date.getSeconds() / 60 * 360 + 180;
  var secondAnimationDeg = date.getSeconds() / 60 * 360;
  var stylesDeg = [
                    "@keyframes rotate-hour{from{transform:rotate(" + hourDeg + "deg);}to{transform:rotate(" + (hourDeg + 360) + "deg);}}",
                    "@keyframes rotate-minute{from{transform:rotate(" + minuteDeg + "deg);}to{transform:rotate(" + (minuteDeg + 360) + "deg);}}",
                    "@keyframes rotate-second{from{transform:rotate(" + secondDeg + "deg);}to{transform:rotate(" + (secondDeg + 360) + "deg);}}",
                    "@keyframes sec-animation{from{transform:rotate(" + secondAnimationDeg + "deg);}to{transform:rotate(" + (secondAnimationDeg + 360) + "deg);}}"
                ].join("");
            document.getElementById("clock-animations").innerHTML = stylesDeg;
})();
(function() { 
  var date = new Date();
  var weekDays = ['So', 'Mo', 'Di', 'Mi', 'Do', 'Fr', 'Sa'];
  var dayIndex = date.getDay();
  document.getElementById('cal-weekday').innerHTML = weekDays[dayIndex];
  document.getElementById('cal-year').innerHTML = date.getFullYear();
  document.getElementById('cal-day').innerHTML = date.getDate();
  
})();
function setCalendarDivision() {
   for (let i = 0; i < 40; i++) {
     let calendar = document.getElementById('calendar');
     calendar.insertAdjacentHTML( 'afterbegin', '<div class="cal-division cal-' + i +'"></div>' );
   }
  var calDivision = document.getElementsByClassName('cal-division');
  var angle = 0;
  var step = (2*Math.PI)/calDivision.length;
  var width = 80;
  var height = 80;
  var degValue = 0;
  for (let i = 0; i < 40; i++) {
    var x = width/2 + 35*Math.cos(angle);
    var y = height/2 + 35*Math.sin(angle);
    calDivision[i].style.left = x - 2 + 'px';
    calDivision[i].style.top = y + 'px';
    calDivision[i].style.transform = "rotate("+ degValue +"deg)";
    angle += step;
    degValue += 9;
  }
 
}
setCalendarDivision();
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

