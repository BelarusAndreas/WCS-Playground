

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.petrol-calculator h4, .summeryText    {
  font-size: 1.2em;
  color: #fff;
  text-shadow: 1px 1px #000;
}
.summery {
  color: #B51836;
  font-size: 1.3em;
  font-weight: 700;
}
.petrol-calculator input {
  width: 6em;
  text-align: center;
  border: 0px;
  margin: 2px;
}
#calculate-btn {
  width: 100%;
  text-align: center;
}
</style>

<div class="petrol-calculator">
<h4>Nach Verbrauch</h4>
<table>
  <tr>
    <td>Effizienz </td>
    <td><input id='efficiency' type="number" value="7.5" min="0" /></td>
    <td>(L / 100 km)</td>
  </tr> 
  <tr>
    <td>Preis pro Liter:</td>
    <td><input id='petrol' type="number" value="1.85" min="0" /></td>
    <td>€</td>
  </tr>
  <tr>
    <td>Entfernung:</td>
    <td><input id='distance' type="number" value="100" min="0" /></td> 
    <td>km</td>
  </tr>
  <tr>
    <td><span class="summeryText">Summe:</span></td>
    <td><span class="summery" id='result'></span></td>
    <td><span class="summeryText">€</span></td>
  </tr>
</table>
<br/>
<h4>Nach Liter</h4>
<table>
  <tr>
    <td><label for="cost">Preis pro Liter:</label></td>
    <td><input type="number" id="cost" step="0.01" min="0.01" value="1.85"></td>
    <td>€</td>
  </tr>
  <tr>
    <td><label for="liters">Getankt:</label></td>
    <td><input type="number" id="liters" step="0.01" min="0" value="25"></td>
    <td>Liter</td>
  </tr>
  <tr>
    <td><span class="summeryText">Summe:</span></td>
    <td><span class="summery" id="total-cost">$0.00</span></td>
    <td><span class="summeryText">€</span></td>
  </tr>
</table>
<button class="button" id="calculate-btn">Kalkulieren</button>
</div>
    
<script>
/* Nach Verbrauch */
const efficiencyEl = document.getElementById("efficiency");
const petrolEl = document.getElementById("petrol");
const distanceEl = document.getElementById("distance");
const resultEl = document.getElementById("result");
efficiencyEl.addEventListener('change', recalculateCost);
petrolEl.addEventListener('change', recalculateCost);
distanceEl.addEventListener('change', recalculateCost);
recalculateCost();
function recalculateCost() {
  const efficiency = parseFloat(efficiencyEl.value);
  const price = parseFloat(petrolEl.value);
  const distance = parseFloat(distanceEl.value);  
  const cost = efficiency * price * distance / 100.0;  
  resultEl.innerText = `${Math.round(cost * 100.0, 2) / 100.0}`;
}
/* Nach Liter */
const costInput = document.getElementById("cost");
const litersInput = document.getElementById("liters");
const calculateBtn = document.getElementById("calculate-btn");
const totalCost = document.getElementById("total-cost");
calculateBtn.addEventListener("click", function() {
  const cost = parseFloat(costInput.value);
  const liters = parseFloat(litersInput.value);
  const total = cost * liters;
  totalCost.textContent = `${total.toFixed(2)}`;
});
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
