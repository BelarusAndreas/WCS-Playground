### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.rss-box {
  display: flex;
  flex-direction: column;
}
.rss {
  background: orange;
  padding: 5px 15px;
  border-radius: 5px;
  margin: 5px;
  width: 200px;
}
.rss:hover {
  background: #E49B0F;
  cursor: pointer;
}
.rss a {
  text-decoration: none;
  color: white;
}
.fa-rss { 
  color: white;
}
</style>

<!-- Beachte bitte, dass das "#" (Raute-Zeichen) mit der URL des RSS-Feeds deiner Seite zu ersetzen ist! -->

<div class="rss-box">
 <span class="rss">
   <i class="fa fa-rss" aria-hidden="true"></i>
   <a href="#">Artikel</a>
 </span>
 <span class="rss">
   <i class="fa fa-rss" aria-hidden="true"></i>
   <a href="#">Blog</a>
 </span>
 <span class="rss">
   <i class="fa fa-rss" aria-hidden="true"></i>
   <a href="#">Forum</a>
 </span>
 <span class="rss">
   <i class="fa fa-rss" aria-hidden="true"></i>
   <a href="#">Filebase</a>
 </span>
</div>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

