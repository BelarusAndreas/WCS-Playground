
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>    
.tabButton {
    background: #325c84;
    color: #fff;
    padding: 3px 5px;    
}    
.tabTitle {
    font-size: 1.2em;
    border-top: 1px solid #000;
    margin-top: 5px;
}
</style>    
<div>  
  <button class="tabButton" onclick="openTab('First')">First</button>  
  <button class="tabButton" onclick="openTab('Second')">Second</button>  
  <button class="tabButton" onclick="openTab('Third')">Third</button>
</div>

<div id="First" class="tab tabContent">  
  <h1 class="tabTitle">First Tab</h1>  
  <p>Lorem ipsum dolor sit amet, consectetur adipisici elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua.</p>
</div>

<div id="Second" class="tab tabContent" style="display:none">  
  <h1 class="tabTitle">Second Tab</h1>  
  <p>Lorem ipsum dolor sit amet, consectetur adipisici elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua.</p> </div>

<div id="Third" class="tab tabContent" style="display:none">  
  <h1 class="tabTitle">Third Tab</h1>  
  <p>Lorem ipsum dolor sit amet, consectetur adipisici elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua.</p>
</div>

<script>
  function openTab(tabName) {  
  var i;  var x = document.getElementsByClassName("tab");  
  for (i = 0; i < x.length; i++) {    
    x[i].style.display = "none";    
  }  
  document.getElementById(tabName).style.display = "block";  
  }
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
4.  Fertig.
