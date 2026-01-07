
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<head>
  <script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
  <script src="https://cdn.rawgit.com/senchalabs/cssbeautify/master/cssbeautify.js"></script>
<style>
.minifierContent {
    background: #ccc;
    width: 100%;
    grid-template-columns: 1fr 1fr 1fr; 
    grid-template-rows: 1fr; 
    grid-template-areas: 
    ". . ."; 
    justify-items: center;    
}
.cssmin-btn {
    display: grid;
    grid-template-columns: auto auto;    
    gap: 5px 10px;
    padding: 0 10px 0 10px;
    margin: 10px 0 10px 0;
    }

.cssmin-in {
    height: 150px;
}
.cssmin-out {
    height: 150px;
}
</style>
</head>

<div class="minifierContent">
    <textarea placeholder=".meineEingabe { color: black; }" class="cssmin-in"></textarea>
    <div class="cssmin-btn">
      <button class="minify" type="submit">Minifier</button>
      <button class="clear-code" type="submit">Löschen</button>
    </div>
    <textarea placeholder="Ausgabe" class="cssmin-out"></textarea>
</div>

<script>
$(function() {
  $('.minify').click(function() {
    var input = $('.cssmin-in').val();
    var output = input
      .replace(/\/\*.*\*\/|\/\*[\s\S]*?\*\/|\n|\t|\v|\s{2,}/g, '')
      .replace(/\s*\{\s*/g, '{')
      .replace(/\s*\}\s*/g, '}')
      .replace(/\s*\:\s*/g, ':')
      .replace(/\s*\;\s*/g, ';')
      .replace(/\s*\,\s*/g, ',')
      .replace(/\s*\~\s*/g, '~')
      .replace(/\s*\>\s*/g, '>')
      .replace(/\s*\+\s*/g, '+')
      .replace(/\s*\!\s*/g, ' !')
      .replace(/\s*\;\}\s*/g, '}');
    $('.cssmin-out').val(output);
  });
  $('.clear-code').click(function() {
    $('.cssmin-in').val('');
    $('.cssmin-out').val('');
  });
});
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
