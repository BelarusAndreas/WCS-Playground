### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.main{
  margin: 20px;
}
.content{
  text-align: center;
  height: 120px;
}
button{
  background-color: #b51836;
  border: 0px;
  border-radius: 15px;
  width: 400px;
  height: 100px;
  color: white;
  font-size: 3em;
  font-family: 'Offside'
}
button:hover{
  background-color: #40B440;
  -webkit-box-shadow:  5px 5px 10px 1px rgba(0, 0, 0, .5);
  box-shadow:  5px 5px 10px 1px rgba(0, 0, 0, .5);
}
</style>

<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>

<div class="main">
  <div class="header">
    <h1>Speed Test</h1>
  </div>
  <div class="content">
    <button id="starttest">Start</button>
  </div>
  <div id="results">
  </div>  
</div>

<script>
var imageAddr = "http://wallpaperswide.com/download/shadow_of_the_tomb_raider_2018_puzzle_video_game-wallpaper-7680x4800.jpg" + "?n=" + Math.random();
var startTime, endTime;
var downloadSize = 5616998; //5.36Mb
var download = new Image();
var roundedDecimals = 2;
var bytesInAKilobyte = 1024;
function showResults() {
  var duration = (endTime - startTime) / 1000;
  var bitsLoaded = downloadSize * 8;
  var speedBps = ( bitsLoaded / duration ).toFixed(roundedDecimals);
  var displaySpeed = speed(speedBps);
  var results = "<h2>Deine Geschwindigkeit beträgt: <h2><h1>" + displaySpeed.value + " " + displaySpeed.units + "</h1>"
    $('#results').fadeOut('fast',function(){
      $('#results').html(results);
      $('#results').fadeIn('fast', function(){
        $('#starttest').text('Thank You!');
      });
    });
}
function speed( bitsPerSecond ){
  var KBps = (bitsPerSecond / bytesInAKilobyte).toFixed(roundedDecimals);
  if ( KBps <= 1 ) return { value: bitsPerSecond, units: "Bps" };
  var MBps = (KBps / bytesInAKilobyte).toFixed(roundedDecimals);
  if ( MBps <= 1 ) return { value: KBps, units: "KBps" };
  else return { value: MBps, units: "MBps" };
}
$('#starttest').on('click', function(){
  $('#starttest').text('Bitte warten ...');
  $('#starttest').attr('disabled', 'disabled');
  download.onload = function () {
    endTime = (new Date()).getTime();
    showResults();
  }
  startTime = (new Date()).getTime();
  download.src = imageAddr;
})
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

