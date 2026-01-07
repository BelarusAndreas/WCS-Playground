### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<canvas id="canvas" width="500" height ="500"></canvas>

<script>
var canvas = document.getElementById('canvas');
var ctx = canvas.getContext('2d');
ctx.strokeStyle = "#28D1FA";
ctx.lineWidth = 17;
ctx.lineCap = "round";
ctx.shadowBlur = 15;
ctx.shadowColor = "#28D1FA";
function degToRad(degree) {  var factor = Math.PI / 180;  return degree * factor;
}
function renderTime() {  var now = new Date();  var today = now.toDateString();  var time = now.toLocaleTimeString();  var h = now.getHours();  var m = now.getMinutes();  var s = now.getSeconds();  var ms = now.getMilliseconds();  var newS = s + (ms / 1000);  // Farbanpassungen  // Hintergrundfarbe  ctx.fillStyle = "#161D29";  ctx.fillRect(0, 0, 500, 500);  // Stunden  ctx.beginPath();  ctx.arc(250, 250, 200, degToRad(270), degToRad((h * 15) - 90));  ctx.stroke();  // Minuten  ctx.beginPath();  ctx.arc(250, 250, 170, degToRad(270), degToRad((m * 6) - 90));  ctx.stroke();  // Sekunden  ctx.beginPath();  ctx.arc(250, 250, 140, degToRad(270), degToRad((newS * 6) - 90));  ctx.stroke();  // Zeit  ctx.font = "bold 50px Sans Serif UI";  ctx.fillStyle = "#28D8FA";  ctx.fillText(time, 160, 270);
}
setInterval(renderTime, 40);
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

