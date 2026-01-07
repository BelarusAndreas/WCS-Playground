### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<!-- Der Adventskranz ist für das Jahr 2025. Für kommende Jahre muss das Script an die jeweiligen Adventstage angepasst werden! 
Passe dazu den JavaScript unter "Monat == 11 && Tag == 30" entsprechend an. -->

<script type="text/javascript">
Heute = new Date();
Tag = Heute.getDate();
Monat = Heute.getMonth()+1;
if (Monat == 11 && Tag == 30) {
document.write("<img src=\"images/adventskranz/first.png\">");
}
if (Monat == 12 && Tag == 7) {
document.write("<img src=\"images/adventskranz/second.png\">");
}
if (Monat == 12 && Tag == 14) {
document.write("<img src=\"images/adventskranz/third.png\">");
}
if (Monat == 12 && Tag == 21) {
document.write("<img src=\"images/adventskranz/forth.png\">");
}
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

