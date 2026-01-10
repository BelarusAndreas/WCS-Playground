
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.menu-container {
    width:100%;
    margin: 0 auto;
    padding: 20px 0;
}
.menu {
    width: 850px;
    font-family: Verdana, Geneva, sans-serif;
    font-weight: 400;
    font-size: 15px;
    line-height: 15px;
    position: relative;
    padding: 0 0 0 4px;
    margin: 0;
    background-color: #b51836;
}
.menu a, .menu a:link, .menu a:visited, .menu a:focus, span {
    color: #fff;
    text-decoration: none;
}
.menu a:hover {
    color: #227087;
    text-decoration: none;
}
.menu > li {
    display: inline-block;
    text-align: center;
    margin-left: -4px;
    border-left: 1px solid #b51836;
}
.menu > li > a {
    padding:20px 18px;
    display: block;
}
.menu > li:hover > a {
    color: #227087;
}
.menu > li > .megadrop {
    background: #ccc;
    opacity: 0;
    visibility: hidden;
    position: absolute;
    list-style: none;
    top:53px;
    left: 0px;
    width: 99.5%;
    min-height: 100px;
    text-align: left;
    margin-top:30px;
    padding: 0;
    z-index: 99;
  color: #000;
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
    overflow: hidden;
    border-left: 2px solid #b51836;
    border-right: 2px solid #b51836;
    border-bottom: 2px solid #b51836;
}
.menu > li:hover .megadrop {
    opacity: 1;
    visibility: visible;
    margin-top: 0px;
}
.menu ul li:hover:after {
    color: #000;
}
.menu .col {
    width: 14.1%;
    float: left;
    color: #000;
    margin: 0 0 0 2.2%;
}
.menu .col ul {
    padding: 0;
    margin: 0;
}
.menu .col ul li {
    padding: 0;
    list-style: none;
    font-size: 11px;
}
.menu .col h3 {
    font-size: 16px;
    padding: 10px 0;
    font-weight: bold;
    margin: 5px 0 5px 0;
    color: #000;
}
.menu .col ul li a {
    display: block;
    padding: 0 0 15px 0;
    color: #000;
}
.menu .col ul li a:hover {
    color: #000;
    text-decoration: underline;
}
.menu > li > ul li ul, .menu li >ul li, .menu > li > .megadrop, .menu > li > ul, .menu > li {
    transition: all 0.2s ease-in-out;
    -moz-transition: all 0.2s ease-in-out;
    -webkit-transition: all 0.2s ease-in-out;
    -ms-transition: all 0.2s ease-in-out;
    -o-transition: all 0.2s ease-in-outs;
}
</style>

<div>
  <ul class="menu">
    <li class="dropdown">
      <a href="#">Mega Menü</a>
      <div class="megadrop">
        <div class="col">
          <h3>Titel</h3>
          <ul>
            <li>
              <a href="#">Link 1</a>
            </li>
            <li>
              <a href="#">Link 2</a>
            </li>
            <li>
              <a href="#">Link 3</a>
            </li>
          </ul>
        </div>
        <div class="col">
          <h3>Titel</h3>
          <ul>
            <li>
              <a href="#">Link 1</a>
            </li>
            <li>
              <a href="#">Link 2</a>
            </li>
            <li>
              <a href="#">Link 3</a>
            </li>
          </ul>
        </div>
        <div class="col">
          <h3>Titel</h3>
          <ul>
            <li>
              <a href="#">Link 1</a>
            </li>
            <li>
              <a href="#">Link 2</a>
            </li>
            <li>
              <a href="#">Link 3</a>
            </li>
          </ul>
        </div>
        <div class="col">
          <h3>Titel</h3>
          <ul>
            <li>
              <a href="#">Link 1</a>
            </li>
            <li>
              <a href="#">Link 2</a>
            </li>
            <li>
              <a href="#">Link 3</a>
            </li>
          </ul>
        </div>
      </div>
    </li>
    </li>
  </ul>
</div>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen / Seiten
2.  Klicke auf  + Box / Seite hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
