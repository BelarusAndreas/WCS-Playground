
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.wrapper {
    margin: 0 auto;
}
.block {
    float: left;
    position: relative;
    margin-top: 20px;
    background: #000;
    color: #fff;
    width: 18.85%;
    margin-right: 10px;
    min-width: 250px;
    height: 260px;
    border: solid 1px #000;
    text-align: center;
    overflow: hidden;
    -webkit-backface-visibility: hidden;
}
.heading {
    height: 30px;
    position: relative;
    font-size: 1.4em;
    width: 100%;
    background: rgba(255, 255, 255, .13);
    padding: 25px 0;
    border-bottom: solid 1px;
}
.block h1 { 
    margin-top: -10px;
}
.block-content {
    position: relative;
    padding: 15px;
}
.green, .green a {
    color: #5eda37;
    box-shadow: 4px 4px 5px #5eda37;
}
.orange, .orange a {
    color: #f66538;
    box-shadow: 4px 4px 5px #f66538;
}
.purple, .purple a {
    color: #f16bf3;
    box-shadow: 4px 4px 5px #f16bf3;
}
.blue, .blue a {
    color: #7ca6de;
    box-shadow: 4px 4px 5px #7ca6de;
}
</style>

<div class="wrapper">
  <div class="blocks">
  
    <div class="block green">
      <div class="heading">
        <h1>Navigation</h1>
      </div>
      <div class="block-content">
        <p>Home</p>
        <p>Forum</p>
        <p>Kontakt</p>
      </div>
    </div>

    <div class="block blue">
      <div class="heading">
        <h1>Partner</h1>
      </div>
      <div class="block-content">
        <p>Marta Musterman</p>
        <p>Michael Musterman</p>
      </div>
    </div>  
  
    <div class="block purple">
      <div class="heading">
        <h1>Rechtliches</h1>
      </div>
      <div class="block-content">
        <p>Nutzungsbedingungen</p>
        <p>Datenschutzerklärung</p>
        <p>Lizenz</p>
      </div>
    </div>
  
    <div class="block orange">
      <div class="heading">
        <h1>Impressum</h1>
      </div>
      <div class="block-content">
        <p>Max Musterman</p>
        <p>Musterstrasse 123</p>
        <p>12345 Musterstadt</p>
      </div>
    </div>
  
  </div>
</div>
```

### Benutzung:
1.  Gehe zu ACP   ➞  Anpassung   ➞  Templates   ➞  Filter: `DEIN STIL`   ➞  Suche:  `pageFooter`
     Hinweis:  *Sollte das Template noch nicht vorhanden sein, so ist dies aus der Standard-Templategruppe zu kopieren!*
2.  Suche dort nach  `<footer id="pageFooter" class="pageFooter">`  und füge  **davor**  den o.g. Quellcode ein und passe diesen an deinen Bedürfnissen an und speichere ab.
3. Fertig!
