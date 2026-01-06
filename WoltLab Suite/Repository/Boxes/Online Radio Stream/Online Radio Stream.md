# Online Radio Stream 

### Features

-   Das Design kann nach eigenen Wünschen beliebig angepasst werden.
-   Keine Plugins von Seiten des Benutzers erforderlich.
-   Kein Flash erforderlich.
-   Funktioniert auf sämtlichen Endgeräten.
-   Start / Stop durch Anklicken (des Covers oder der Beschreibung)

### Quellcode:

    <script src="https://ajax.aspnetcdn.com/ajax/jQuery/jquery-3.1.0.min.js"></script>
    
    <script>
      jQuery(document).ready(function( $ ) {
        $("audio").on("play", function (me) {
          $("audio").each(function (i,e) {
            if (e !== me.currentTarget) {
              this.pause();
              this.currentTime = 0;
            }
          });
        });
      })
      function play(e) {
        var de = document.getElementById(e);
        var div = document.getElementsByClassName('playlist_container')[0];
        var number = div.getElementsByTagName('input').length;
        for (var i = 0, n = number; i < n; i++){
          div.getElementsByTagName('input')[i].style.background="none";
        }
        if (de.paused) {
          url = de.src.split("?")[0];
          var de1 = url  + "?" + new Date().getTime();
          document.getElementById(e).src = de1;
          div.getElementsByTagName('input')[e-1].style.background="url('images/radio/play.png') no-repeat 2px 2px / 12px";              de.play();
          de.style.display="block";
          de.onended = function (){
            if (document.getElementById(e+1)) {
              play(e+1);
            } else {
              play(1);
            }
          }
          } else {
          de.pause();
          }
        }
    </script>
    
    <!-- Start: Radio Box -->
    <div class="playlist_container" style="width:100%; height: 250px; overflow: scroll;">
      <!-- ::::: Radio Roks ::::: -->
      <div class="song" onclick="play(1)">
        <input type="image" src="images/radio/Radio-Roks.png" width="50" height="50" alt="Radio Roks" style="float: left; margin-right: 10px;">
        <h3>Radio Roks</h3>
        <audio style="display:none" id ="1" src="http://de.streams.radioplayer.by:8000/live" autostart="0" autostart="false" preload ="none" type="audio/mpeg"></audio>
        <p>Kurzbeschreibung zum Sender</p>
      </div>        
      <br>
      <hr style="width: 80%;"><br>
      <!-- ::::: Radio Brest ::::: -->
      <div class="song" onclick="play(2)"> 
        <input type="image" src="images/radio/Radio-Brest.png" width="50" height="50" alt="Stream: Radio Brest" style="float: left; margin-right: 10px;">
        <h3>Radio Brest</h3>
        <audio style="display:none" id ="2" src="https://streaming.liveonline.radio/radio-brest" autostart="0" autostart="false" preload ="none" ></audio>
        <p>Kurzbeschreibung zum Sender</p>
      </div>
      <br><hr style="width: 80%;"><br>        
      <!-- ::::: Radius FM ::::: -->    
      <div class="song" onclick="play(3)">         
        <input type="image" src="images/radio/Radius-FM.png" width="50" height="50" alt="Radius-FM" style="float: left; margin-right: 10px;">        
        <h3>Radius-FM</h3>        
        <audio style="display:none" id ="1" src="https://streaming.liveonline.radio/radius-fm" autostart="0" autostart="false" preload ="none" ></audio>        
        <p>Kurzbeschreibung zum Sender</p>
      </div>
      <br><hr style="width: 80%;"><br>
      <!-- ::::: Humor FM ::::: -->
      <div class="song" onclick="play(4)">
        <input type="image" src="images/radio/Humor-FM.png" width="50" height="50" alt="Humor FM" style="float: left; margin-right: 10px;">        
        <h3>Humor FM</h3>
        <audio style="display:none" id ="1" src="https://streaming.liveonline.radio/humor-fm-2" autostart="0" autostart="false" preload ="none" ></audio>
        <p>Kurzbeschreibung zum Sender</p>
      </div>    
    <!-- Ende: Radio Box -->
    </div>

### Benutzung:

1.  jQuery wird nur benötigt um nicht mehrere Radiosender gleichzeitig abzuspielen.  
    Sollte jQuery jedoch bereits intrigiert sein, so wird dieses natürlich kein zweites mal benötigt.
2.  In der Zeile  style.background="url('images/radio/play.png')  ist das Bild zum Play-Button entsprechend anzupassen.
3.  In den einzelnen div-Tags, sind im Input-Tag die Radio-Logos, sowie im Audio-Tag die Stream-URL's, entsprechend anzupassen.
4.  Insofern weitere Radiosender gewünscht sind, so einfach den kompletten div eines Senders kopieren und im div-Tag das  onclick="play(X)"  um jeweils um eine Nummer zu erhöhen als die letztere. Achtet dabei auf die richtige Reihenfolge!
5.  Das nutzen von mehr als 10 Radiosendern wird nicht empfohlen, da dieses zu Problemen führen kann.
