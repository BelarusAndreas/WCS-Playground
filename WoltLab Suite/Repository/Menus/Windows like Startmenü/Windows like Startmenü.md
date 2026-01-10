
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
Template
```
<div id="woltlabDesktop">
  
  <!-- Start: Woltlab Panel-->
  <div class="woltlabPanel">
    <div class="woltlabPanelStart">
        <a href="javascript:void(0);" id="openStartMenu">
        <i class="fa fa-th-large" aria-hidden="true"></i>
      </a>
    </div>
  </div>
  <!-- End: Woltlab Panel-->
  
  <!-- Start: Woltlab StartMenu-->
  <div id="woltlabStartMenu">
    <div class="wrapper">
      <div class="woltlabStartMenuHeader">
        <i class="fa fa-user-circle-o" aria-hidden="true"></i> 
        <span>User</span>
      </div>
    
      <div class="woltlabStartMenuContent">
        
        <!-- Woltlab StartMenu Left-->
        <div class="woltlabStartMenuLeft">
          <h5>Apps</h5>
          <li>
            <a href="#"><span>Dashboard</span></a>
          </li>
        </div>
        
        <!-- Start: Woltlab StartMenu Right-->
        <div class="woltlabStartMenuRight">
          <h5>Favoriten</h5>         
          <div class="metroTilesWrapper">

            <div class="metroTiles">
            <!-- Start: Woltlab Metro Tiles -->
              <a href="#" class="metroTile green">
                <i class="fa fa-th-large fa-3x" aria-hidden="true"></i>
                <p>Metro</p>
              </a>
              <a href="#" class="metroTile red">
                <i class="fa fa-th-large fa-3x" aria-hidden="true"></i>
                <p>Metro</p>
              </a>
              <a href="#" class="metroTile blue">
                <i class="fa fa-th-large fa-3x" aria-hidden="true"></i>
                <p>Metro</p>
              </a>
              <a href="#" class="metroTile grey">
                <i class="fa fa-th-large fa-3x" aria-hidden="true"></i>
                <p>Metro</p>
              </a>
              <a href="#" class="metroTile yellow">
                <i class="fa fa-th-large fa-3x" aria-hidden="true"></i>
                <p>Metro</p>
              </a>
              <!-- End: Woltlab Metro Tiles -->
            </div>
          </div>
          <!-- End: Woltlab StartMenu Right --> 
        </div>    
      </div>
      
      <div class="woltlabStartMenuFooter">
        <i class="fa fa-search" aria-hidden="true"></i>
      </div>
    
    </div>
  </div>
  <!-- End: Woltlab StartMenu-->
</div>  

<script>
$(function(){
  $('#openStartMenu').click(function(){
    $('#woltlabStartMenu').toggle();
  });
});
</script>  
```
CSS
```
.woltlabPanel{
    background-color: rgba(1, 1, 1, .8);
    border-color: rgba(1, 1, 1, .8);
    height: 36px;
    bottom: 0;
    left: 0;
    right: 0;
    position: fixed;
}
.woltlabPanelStart{
    padding: 3px;
    height: 36px;
    width: 36px;
    font-size: 1.4em;
    text-align: center;
}
.woltlabPanelStart:hover{
    height: 36px;
    width: 36px;
    border-bottom: 3px solid #76b9ed;
    background-color: rgba(255, 255, 255, .15);
}
.woltlabPanel a{
    color: #fff;
}
.wrapper {
    height: 100vh;
    display: flex;
    flex-direction: column;
}
#woltlabStartMenu {
    display: none;
    width: auto;
    max-width: 425px;
    padding: 2px;
    top: 0px;
    background-color: rgba(1, 1, 1, .8);
    border-color: rgba(1, 1, 1, .8);
}
.woltlabStartMenuContent{
    flex: 1;
    display: grid;
    grid-template-columns: 150px 300px;
    grid-gap: 20px;
}
.woltlabStartMenuHeader{
    height: 30px;
    padding: 5px 10px;
}
.woltlabStartMenuFooter{
    height: 36px;
    padding: 5px;
    margin-bottom: 36px;
    border-top: 1px solid #000;
}
.woltlabStartMenuLeft{
    padding: 5px 10px;
}
.woltlabStartMenuLeft li{
    list-style: none;
    width: 100%;
    color: #fff;
    text-decoration: none;
    padding: 3px 0px;
}
.woltlabStartMenuLeft li:hover{
    background: #0f1214;
}
.woltlabStartMenuLeft a{
    color: #fff;
}
.woltlabStartMenuLeft a:hover{
    text-decoration: none;
}
.woltlabStartMenuRight{
    padding: 5px 10px;
}
.metroTilesWrapper{
    display: grid;
}
.metroTiles{
    display: flex;
    flex-direction: row;
    grid-gap: 5px;
    flex-wrap: wrap;
}
.metroTile{
    width: 75px;
    height: 75px;
    color: #fff;
    text-align: center;
    padding: 5px;
}
.metroTile:hover{
    color: #fff;
    text-decoration: none;
}
/* Metro Tile Colors */
.green{background-color: #029100; }
.green:hover{background-color: #03cf00; }
.red{background-color: #b30000; }
.red:hover{background-color: #ff0000; }
.blue{background-color: #01228d; }
.blue:hover{background-color: #0231c9; }
.yellow{background-color: #b3a400; }
.yellow:hover{background-color: #ffea00; }
.grey{background-color: #707070; }
.grey:hover{background-color: #999999; }
```
### Benutzung:
1.  Gehe zu ACP  ➞  Anpassung  ➞  Templates  ➞  Filter: `DEIN STIL`
2.  Erstelle ein neues Template mit dem Namen  `Startmenu`
3.  Füge hier den obigen HTML Quellcode und danach den JS Quellcode ein und passe diesen an deinen Bedürfnissen an und speichere ab.
4.  Gehe zu ACP  ➞  Anpassung  ➞  Templates  ➞  Filter: `DEIN STIL`  ➞  Wähle das Template:  `footer`  
     **Hinweis:**  Sollte das Template `footer` noch nicht vorhanden sein, so kopiere dieses aus den Standard-Template in deine Templategruppe deines Stils.
5.  Suche nach  `</body>`  und füge  **davor** ` {include file="Startmenu"}`  ein und speichere ab.
6.  Gehe zu ACP  ➞  Anpassung  ➞  Stile  ➞ Filter: `DEIN STIL`  ➞  Tab: `Erweiterte Einstellungen`
7.  Füge hier den obigen CSS Quellcode ein und passe diesen an deinen Bedürfnissen an und speichere ab.
8.  Fertig!

### ToDo's
Integration der Suchfunktion
Benutzerbedingte Anzeige(n) (u.a. das Feld "User")
Responsive Anpassungen
Badges in den Metro Tiles


