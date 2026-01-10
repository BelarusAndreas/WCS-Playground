
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.context {
    font-size: 1.1em;
    position: absolute;
    width: 200px;
    height: auto;
    padding: 5px 0px;
    border-radius: 5px;
    top: 10;
    left: 10;
    background-color: #fff;
    box-shadow: 0 12px 15px 0 rgba(0, 0, 0, 0.24);
    color: #333;
}
.context_item {
    height: 32px;
    line-height: 32px;
    cursor: pointer;
    text-overflow: ellipsis;
    overflow: hidden;
    white-space: nowrap;
}
.context_item:hover {
    background-color: #ddd;
}
.inner_item {
    margin: 0px 10px;
}
.context_hr {
    height: 1px;
    border-top: 1px solid #bbb;
    margin: 3px 10px;
}
</style>

<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>

<div class="context" hidden>
  <div class="context_item"> 
    <div class="inner_item">
      <i class="fa-solid fa-house"></i> Home
    </div> 
  </div>
  <div class="context_item"> 
    <div class="inner_item">
      <i class="fa-solid fa-newspaper"></i> Artikel
    </div> 
  </div>
  <div class="context_item"> 
    <div class="inner_item">
      <i class="fa-solid fa-comments"></i> Forum
    </div> 
  </div>
  <div class="context_hr"></div>
  <div class="context_item"> 
    <div class="inner_item">
      <i class="fa-solid fa-circle-user"></i> Profil
    </div> 
  </div>
  <div class="context_hr"></div>
  <div class="context_item"> 
    <div class="inner_item">
      <i class="fa-solid fa-right-from-bracket"></i> Logout
    </div> 
  </div>
</div>

<script>
$(document).on("contextmenu", function(event) {
  event.preventDefault();
  $(".context")
    .show()
    .css({
      top: event.pageY,
      left: event.pageX
    });
});
$(document).click(function() {
  if ($(".context").is(":hover") == false) {
    $(".context").fadeOut("fast");
  };
});
</script>
```

### Benutzung:
1.  Gehe zu ACP   ➞  Anpassung   ➞  Templates   ➞  Filter: `DEIN STIL`   ➞  Suche:  `header`
     Hinweis:  *Sollte das Template noch nicht vorhanden sein, so ist dies aus der Standard-Templategruppe zu kopieren!*
2.  Suche dort nach  `<body>`  und füge  **danach**  den o.g. HTML-Quellcode ein und passe diesen an deinen Bedürfnissen an und speichere ab.
3. Fertig!
