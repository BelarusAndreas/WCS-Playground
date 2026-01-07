### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<div id="clock"></div>

<script>
const timeElement = document.getElementById("clock");
function updateTime() {
    const now = new Date();
    const hours = now.getHours();    
    const minutes = now.getMinutes();    
    const seconds = now.getSeconds();    
    const clockStr = `${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;    
    timeElement.innerText = clockStr;
}
updateTime();
setInterval(updateTime, 1000);
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
