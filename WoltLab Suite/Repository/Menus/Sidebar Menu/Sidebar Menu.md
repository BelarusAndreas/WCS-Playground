
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
Template
```
<nav class="main-menu">
  <div class="scrollbar" id="style-1">
    <ul>
      <li>
        <a href="index.php">
          <i class="fa fa-home fa-2x"></i>
          <span class="nav-text">Dashboard</span>
        </a>
      </li>
      <li>  
        <a href="index.php/article-list/">
          <i class="fa fa-newspaper-o fa-2x"></i>
          <span class="nav-text">Artikel</span>
        </a>
      </li>
      <li>
        <a href="index.php/forum/">
          <i class="fa fa-comments-o fa-2x"></i>
          <span class="nav-text">Forum</span>
        </a>
      </li>
      <li>
        <a href="index.php/member-list/">
          <i class="fa fa-users fa-2x"></i>
          <span class="nav-text">Mitglieder</span>
        </a>
      </li>
      <li>
        <a href="index.php/filebase">
          <i class="fa fa-database fa-2x"></i>
          <span class="nav-text">Filebase</span>
        </a>
      </li>
      <li>
        <a href="index.php/galery">
          <i class="fa fa-picture-o fa-2x"></i>
          <span class="nav-text">Galerie</span>
        </a>
      </li>
      <li>
        <a href="index.php/marketplace">
          <i class="fa fa-shopping-cart fa-2x"></i>
          <span class="nav-text">Marktplatz</span>
        </a>
      </li>
      <li>
        <a href="index.php/lexicon">
          <i class="fa fa-book fa-2x"></i>
          <span class="nav-text">Lexikon</span>
        </a>
      </li>
      <li>
        <a href="index.php/map">
          <i class="fa fa-map-marker fa-2x"></i>
          <span class="nav-text">Map</span>
        </a>
      </li>
      <li>
        <a href="index.php/calender">
          <i class="fa fa-calendar fa-2x"></i>
          <span class="nav-text">Kalender</span>
        </a>
      </li>
      <li>
        <a href="index.php/blog">
          <i class="fa fa-pencil fa-2x"></i>
          <span class="nav-text">Blog</span>
        </a>
      </li>
      <li>
        <a href="index.php/server">
          <i class="fa fa-server fa-2x"></i>
          <span class="nav-text">Server</span>
        </a>
      </li>
      <li>
        <a href="index.php/upload">
          <i class="fa fa-upload fa-2x"></i>
          <span class="nav-text">Upload</span>
        </a>
      </li>
      <li>
        <a href="index.php/workplace">
          <i class="fa fa-briefcase fa-2x"></i>
          <span class="nav-text">Arbeitsplatz</span>
        </a>
      </li>
      <li>
        <a href="index.php">
          <i class="fa fa-question-circle fa-2x"></i>
          <span class="nav-text">FAQ</span>
        </a>
      </li>
    </ul>
    <hr>
    <ul class="logout">
      <li>
        <a href="index.php/logout/" title="Logout">
          <i class="fa fa-sign-out fa-2x"></i>
        </a>
        <a href="index.php/conversaation-list/" title="Konverstionen">
          <i class="fa fa-comment fa-2x"></i>
        </a>
        <a href="index.php" title="Style">
          <i class="fa fa-paint-brush fa-2x"></i>
        </a>
        <a href="index.php/search/" title="Suche">
          <i class="fa fa-search fa-2x"></i>
        </a>
      </li>
    </ul>
</nav>
```
CSS
```
/* Content-Abstand */
#pageContainer{  
    margin-left: 50px;
}

/* ScrollBar  */
.scrollbar {  
    height: 90%;  
    width: 100%;  
    overflow-y: hidden;  
    overflow-x: hidden;
}
.scrollbar:hover {  
    height: 90%;  
    width: 100%;  
    overflow-y: scroll;  
    overflow-x: hidden;
}
#style-1::-webkit-scrollbar-track {  border-radius: 2px; }
#style-1::-webkit-scrollbar {  width: 5px;  background-color: #F7F7F7; }
#style-1::-webkit-scrollbar-thumb {  border-radius: 10px;  -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,.3);  background-color: #24425f; }
/* Icons */ 
.fa {  
    position: relative;  
    width: 55px;  
    height: 36px;  
    text-align: center;  
    top:12px;  
    font-size:20px;  
    color: #ccc;
}
/* Main Menu */
.main-menu:hover, nav.main-menu.expanded {  
    width:250px;  
    overflow:visible;  
    opacity:1;
}
.main-menu {  
    background:#325C84;  
    position:fixed;  
    z-index: 999;  
    top:0;  
    bottom:0;  
    height:100%;  
    margin-top: 50px;  
    left:0;  
    width:55px;  
    overflow:hidden;  
    -webkit-transition:width .2s linear;  
    transition:width .2s linear;  
    -webkit-transform:translateZ(0) scale(1,1);  
    box-shadow: 1px 0 15px rgba(0, 0, 0, 0.07);  
    opacity:1;
}
.main-menu>ul {  
    margin:7px 0;
}
.main-menu li {  
    position:relative;  
    display:block;  
    width:250px;
}
.main-menu li>a {  
    position:relative;  
    width:255px;  
    height: 45px;  
    display:table;  
    border-collapse:collapse;  
    border-spacing:0;  
    color:#fff;  
    font-size: 13px;  
    text-decoration:none;  
    -webkit-transform:translateZ(0) scale(1,1);  
    -webkit-transition:all .14s linear;  
    transition:all .14s linear;
}
.main-menu .nav-icon {  
    position:relative;  
    display:table-cell;  
    width:55px;  
    height:36px;  
    text-align:center;  
    vertical-align:middle;  
    font-size:18px;
}
.main-menu .nav-text  {  
    position:relative;  
    display:table-cell;  
    vertical-align:middle;  
    width:190px;
}
.main-menu>ul.logout {  
    position:absolute;  
    left:0;  
    bottom:0; 
}
.no-touch .scrollable.hover {  
    overflow-y:hidden;
}
.no-touch .scrollable.hover:hover {  
    overflow-y:auto;  
    overflow:visible; 
}
a:hover,a:focus {  
    text-decoration:none;  
    border-left:0px solid #F7F7F7;
}
nav {  
    -webkit-user-select:none;  
    -moz-user-select:none;  
    -ms-user-select:none;  
    -o-user-select:none;  user-select:none; 
}
nav ul,nav li {  
    outline:0;  
    margin:0;  
    padding:0;
}

.main-menu li:hover>a,nav.main-menu li.active>a,.dropdown-menu>li>a:hover,.dropdown-menu>li>a:focus,.dropdown-menu>.active>a,.dropdown-menu>.active>a:hover,.dropdown-menu>.active>a:focus,.no-touch .dashboard-page nav.dashboard-menu ul li:hover a,.dashboard-page nav.dashboard-menu ul li.active a {  
    color:#fff;  
    background-color:#BFBFBF;  
    text-shadow: 0px 0px 0px;
}
.logout li a{  
    width: 25%;  
    height: 45px;  
    float: left;
}
```
### Benutzung:
1.  Gehe zu  Anpassung   ➞  Templates  und klicke auf  + Template hinzufügen.
2.  Wähle dein Style unter der Templategruppe aus, vergebe einen Namen (als Beispiel: `SidebarMenu`), füge den HTML-Code ein und speicher das Template ab.
3.  Suche das Template  `header`  und klicke auf   ➞  um das Template zu bearbeiten.  
    Hinweis: Sollte das Template  `header` noch nicht vorhanden sein, so kopiere dieses bitte vorab in deine Style-Templategruppe.
4.  Suche im  header-Template nach dem öffnenden Body-Tag
5.  Füge  **danach**  in einer neuen Zeile folgenden Code ein:  `{include file='SidebarMenu'}`  
    Hinweis:  Solltest Du das Template wie unter Punkt 2 genannt einen anderen Namen als `SidebarMenu` gegeben haben so ist dieser mit diesem zu ersetzen!
6.  Füge nun den CSS Code unter  Stil   ➞  Stilunabhängiges CSS und SCSS  -  _**oder**_  - unter  Stil   ➞  Dein_Style   ➞  Erweiterte Einstellungen   ➞  Individuelles CSS und SCSS  ein.
7.  Passe die Links im HTML und den Style im CSS-Code nach Deinen Bedürfnissen an.
8.  Fertig!





