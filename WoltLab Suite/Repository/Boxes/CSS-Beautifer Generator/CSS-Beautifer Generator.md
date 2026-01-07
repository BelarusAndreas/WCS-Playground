

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<head>
  <script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
  <script src="https://cdn.rawgit.com/senchalabs/cssbeautify/master/cssbeautify.js"></script>
<style>
.beautifyContent {
    background: #ccc;
    width: 100%;
    grid-template-columns: 1fr 1fr 1fr; 
    grid-template-rows: 1fr; 
    grid-template-areas: 
    ". . ."; 
    justify-items: center;    
}
.cssbeaut-btn {
    display: grid;
    grid-template-columns: auto auto;    
    gap: 5px 10px;
    padding: 0 10px 0 10px;
    margin: 10px 0 10px 0;
}
.cssbeaut {
    height: 150px;
}
.cssbeaut-out {
    height: 150px;
}
</style>
</head>

<div class="beautifyContent">
    <textarea placeholder="Eingabe" class="cssbeaut"></textarea>
    <div class="cssbeaut-btn">
      <button class="beautify" type="submit">Beautifier</button>
      <button class="beaut-clear-code" type="submit">Löschen</button>
    </div>
    <textarea placeholder="Ausgabe" class="cssbeaut-out"></textarea>
</div>

<script>
$(function() {
  $('.beautify').click(function() {
    var beaut_input = $('.cssbeaut-in').val();
    var beaut_output = cssbeautify(beaut_input, {
      indent: '    ',
      openbrace: 'end-of-line',
      autosemicolon: true
    });
    $('.cssbeaut-out').val(beaut_output);
  });
  $('.beaut-clear-code').click(function() {
    $('.cssbeaut-in').val('');
    $('.cssbeaut-out').val('');
  });
});
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
