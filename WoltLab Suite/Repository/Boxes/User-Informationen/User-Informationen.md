### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.text-green {
  color: #fff;
  background: green;
  padding: 10px;
  width: 250px;
  text-align: center;
  border-radius: 5px;
}
.text-red {
  color: #fff;
  background: red;
  padding: 10px;
  width: 250px;
  text-align: center;
  border-radius: 5px;
}
.result-table {
  background: #fff;
  border: 1px solid #ccc;
  border-radius: 5px;
}
.info-cell {
  background: #eee;
  padding: 5px;
  color: #000;
}
</style>

<div>
  <p id="result"></p>
  <p id="visitor-info"></p>
</div>

<script>     
document.addEventListener('DOMContentLoaded', function () {
            const botUserAgents = [
                'Googlebot',
                'Bingbot',
                'Yahoo Slurp',
                'YandexBot',
                'DuckDuckBot',
                'Baiduspider',
                'Sogou',
                'Exabot',
                'AhrefsBot',
                'MJ12bot',
                'SemrushBot'
];
function isBot() {
  const userAgent = navigator.userAgent;
  for (const bot of botUserAgents) {
    if (userAgent.includes(bot)) {
      return true;
    }
  }
  return false;
}
function displayResult() {
  const resultElement = document.getElementById('result');
  const visitorInfoElement = document.getElementById('visitor-info');
  if (isBot()) {                   
    resultElement.textContent = 'Sie sind ein Bot!';
    resultElement.classList.add('text-red');
    } else {               
    resultElement.textContent = 'Sie sind ein realer Benutzer';
    resultElement.classList.add('text-green');
    fetch('https://ipinfo.io/json')
    .then(response => response.json())
    .then(data => {
      const info = `
      <table class="result-table">
        <tr>
          <td class="info-cell"><i class="fa fa-exclamation-circle" aria-hidden="true"></i> IP Addresse:</td>
          <td>${data.ip}</td>
        </tr>
        <tr>
          <td class="info-cell"><i class="fa fa-flag" aria-hidden="true"></i> Land:</td>
          <td>${data.country}</td>
        </tr>
        <tr>
          <td class="info-cell"><i class="fa fa-map" aria-hidden="true"></i> Region:</td>
          <td>${data.region}</td>
        </tr>
        <tr>
          <td class="info-cell"><i class="fa fa-building" aria-hidden="true"></i> Stadt:</td>
          <td>${data.city}</td>
        </tr>
        <tr>
          <td class="info-cell"><i class="fa fa-location-arrow" aria-hidden="true"></i> Koordinaten:</td>
          <td>${data.loc}</td>
        </tr>
        <tr>
          <td class="info-cell"><i class="fa fa-tasks" aria-hidden="true"></i> ISP:</td>
          <td>${data.org}</td>
        </tr>
        <tr>
          <td class="info-cell"><i class="fa fa-desktop" aria-hidden="true"></i> Gerät:</td>
          <td>${navigator.platform}</td>
        </tr>
        <tr>
          <td class="info-cell"><i class="fa fa-microchip" aria-hidden="true"></i> System:</td>
          <td>${navigator.userAgent}</td>
        </tr>
        <tr>
          <td class="info-cell"><i class="fa fa-chrome" aria-hidden="true"></i> Browser:</td>
          <td>${getBrowserInfo()}</td>
        </tr>
      </table>
        `;
        visitorInfoElement.innerHTML = info;
      })
      .catch(error => {
        console.error('Fehler:', error);
      visitorInfoElement.textContent = 'Fehler bei holen der Benutzerinformationen.';
    });
  }
}
function getBrowserInfo() {
  const userAgent = navigator.userAgent;
  const browserInfo = userAgent.match(/(chrome|safari|firefox|msie|trident|edge(?=\/))\/?\s*(\d+)/i) || [];
  return browserInfo[1];
}
displayResult();
});
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

