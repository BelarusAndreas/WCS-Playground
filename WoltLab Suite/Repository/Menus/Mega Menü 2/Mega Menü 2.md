
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.container {
    margin: 10px auto;
    display: table;
    max-width: 1140px;
    width: 100%;
}
.container:after, .container:before {
    content: "" clear : both;
}
nav.menu {
    background: #b51836;
    position: relative;
    min-height: 45px;
    height: 100%;
}
.menu > ul > li {
    list-style: none;
    display: inline-block;
    color: #fff;
    line-height: 45px;
}
.menu > ul li a, .xs-menu li a {
    text-decoration: none;
    color: #fff;
     display:block;
     padding: 0px 24px;
}
.menu > ul li a:hover {
    background:#444;
    color: #fff;
    transition-duration: 0.3s;
    -moz-transition-duration: 0.3s;
    -webkit-transition-duration: 0.3s;
}
.active{
    background:#444 !important;
}
.displaynone{
    display: none;
}
.xs-menu-cont{
    display:none;
}
.xs-menu-cont > a {
    background: none repeat scroll 0 0 #ff7f50;
    border-radius: 3px;
    padding: 3px 6px;
    display: block;
}
.xs-menu-cont > a:hover{
    cursor: pointer;
}
.xs-menu li {
    color: #000;
    padding: 14px 30px;
    background: #ccc;
}
.xs-menu  a{
    text-decoration:none;
}
.mega-menu {
    background: none repeat scroll 0 0 #ccc;
    left: 0;
    margin-top: 3px;
    position: absolute;
    width: 100%;
    padding:15px;
    display:none;
    transition-duration: 0.9s;
}
#menutoggle i {
    color: #000;
    font-size: 33px;
    margin: 0;
    padding: 0;
}
.mm-6column:after, 
.mm-6column:before, 
.mm-3column:after, 
.mm-3column:before{
    content:"";
    display:table;
    clear:both;
}
.mm-6column, 
.mm-3column {
    float: left;
    position: relative;
}
.mm-6column {
    width: 50%;
}
.mm-3column {
    width: 25%;
}
.responsive-img {
    display: block;
    max-width: 100%;
}
.left-images{
    margin-right:25px;
}
 .left-images, .left-categories-list {
    float: left;
}
.categories-list span {
    color: #000;
}
.categories-list li {
    display: block;
    line-height: normal;
    color: #000;
    margin: 0;
    padding: 5px 0;
}
.categories-list li :hover{
    background: inherit !important;
}
.left-images > p {
    background: none repeat scroll 0 0 #b51836;
    display: block;
    font-size: 18px;
    line-height: normal;
    margin: 0;
    padding: 5px 14px;
}
.categories-list span {
    font-size: 18px;
    padding-bottom: 5px;
    text-transform: uppercase;
}
.mm-view-more {
    background: none repeat scroll 0 0 #b51836;
    color: #fff;
    display: inline !important;
    line-height: normal;
    padding: 5px 8px !important;
    margin-top:10px;
}
.display-on {
    display:block;
    transition-duration: 0.9s;
}
.drop-down > a:after{
    content:"\f103";
    color:#000;
    font-family: FontAwesome;
    font-style: normal;
    margin-left: 5px;
}
 @media (max-width: 600px) {
  .menu {
     display:none;
   }
  .xs-menu li a {
     padding:0px;
 }
 .xs-menu-cont{
     display:block ;
    }
 }
.animated {
    -webkit-animation-duration: 1s;
    animation-duration: 1s;
    -webkit-animation-fill-mode: both;
    animation-fill-mode: both;
}
@-webkit-keyframes fadeIn {
  0% { opacity: 0; }
  100% { opacity: 1; }
}
@keyframes fadeIn {
  0% { opacity: 0; }
  100% { opacity: 1; }
}
.fadeIn {
    -webkit-animation-name: fadeIn;
    animation-name: fadeIn;
}
</style>

<div class="container">
  <div class="xs-menu-cont">
    <a id="menutoggle">
      <i class="fa fa-align-justify"></i>
    </a>
    <nav class="xs-menu displaynone">
      <ul>
        <li class="active">
          <a href="#">Home</a>
        </li>
        <li>
          <a href="#">Mega-Menü</a>
        </li>
      </ul>
    </nav>
  </div>
  <nav class="menu">
    <ul>
      <li class="active">
        <a href="#">Home</a>
      </li>
      <li class="drop-down">
        <a href="#">Mega-Menü</a>
        <div class="mega-menu fadeIn animated">
          <div class="mm-6column">
            <span class="left-images">
              <img src="https://placehold.co/200x100/png">
              <p>Titel</p>
            </span>
          </div>
          <div class="mm-3column">
            <span class="categories-list">
              <ul>
                <span>Titel</span>
                <li>Link 1</li>
                <li>Link 2</li>
                <li>Link 3</li>
                <li>Link 4</li>
                <li>Link 5</li>
                <a class="mm-view-more" href="#">Mehr</a>
      </li>
    </ul>
    </span>
</div>
<div class="mm-3column">
  <span class="categories-list">
    <ul>
      <span>Titel</span>
      <li>Link 1</li>
      <li>Link 2</li>
      <li>Link 3</li>
      <li>Link 4</li>
      <li>Link 5</li>
      <a class="mm-view-more" href="#">Mehr</a>
        </li>
    </ul>
  </span>
</div>
</div>
</li>
</ul>
</nav>
</div>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen / Seiten
2.  Klicke auf  + Box / Seite hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
