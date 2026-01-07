
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.color-picker {
    background: #ccc;
    width: 100%;
    margin: 0 auto;
    text-align: center;
}
sl-card {
   margin: 0 auto; 
}
sl-card::part(base) {
  --padding: var(--spacing);
  border: none;
}
#result {
  display: grid;
  grid-template-columns: repeat(11, var(--swatch-size));
  gap: 4px;
  margin-bottom: var(--spacing);
}
.swatch {
  display: inline-block;
  width: var(--swatch-size);
  height: var(--swatch-size);
}
.inputs {
  display: flex;
  gap: var(--spacing);
}
sl-color-picker {
  margin-bottom: var(--spacing);  
}
sl-color-picker::part(base) {
  box-shadow: none; 
}
.right {
  flex: 1 1 auto; 
}
small:not(:first-child):before {
  content: '·';
}
@media screen and (max-width: 900px) {
  #result {
    grid-template-columns: repeat(6, 1fr);
  } 
  .inputs {
    flex-direction: column;
    margin: auto;
  }  
  small {
    display: block;
    margin-top: var(--spacing);
  }  
  small:before {
    display: none; 
  }
}    
</style>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@shoelace-style/shoelace@2.0.0-beta.48/dist/themes/light.css">
<script type="module" src="https://cdn.jsdelivr.net/npm/@shoelace-style/shoelace@2.0.0-beta.48/dist/shoelace.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/chroma-js/2.1.2/chroma.min.js"></script>

<div class="color-picker">
  <sl-card>
    <div id="result"></div>
    <div class="inputs">
      <div class="left">
        <sl-color-picker inline value="#4a90e2"></sl-color-picker>
      </div>
    </div> 
  </sl-card>
</div>

<script>
const colorPicker = document.querySelector('sl-color-picker');
const nameInput = document.querySelector('sl-input[name="name"]');
const outputTextarea = document.querySelector('sl-textarea[name="tokens"]');
const result = document.querySelector('#result');
function update() {  
  if (!chroma.valid(colorPicker.value)) {
    return;
  } 
  const colorScale = [50, 100, 200, 300, 400, 500, 600, 700, 800, 900, 950]
  const hex = chroma(colorPicker.value).hex();
  const scale = chroma.scale([
    chroma(hex).luminance(.95), // 50
    chroma(hex).luminance(.84), // 100
    chroma(hex).luminance(.73), // 200
    chroma(hex).luminance(.62), // 300
    chroma(hex).luminance(.49), // 400
    chroma(hex).luminance(.35), // 500
    chroma(hex).luminance(.23), // 600
    chroma(hex).luminance(.15), // 700
    chroma(hex).luminance(.10), // 800
    chroma(hex).luminance(.05), // 900
    chroma(hex).luminance(.02)  // 950
  ]).colors(colorScale.length);
  const name = nameInput.value.trim().toLowerCase() || 'custom';
  let swatches = '';
  let tokens = ''; 
  scale.map((color, index) => {
    const rgb = chroma(color).rgb();
    swatches += `<div class="swatch" style="background-color: ${color};"></div>`;
    tokens += `--sl-color-${name}-${colorScale[index]}: rgb(${rgb.join(' ')});\n`;
  });  
  result.innerHTML = swatches;
  outputTextarea.value = `/* Copy & paste into your theme */\n\n${tokens}`;
}
colorPicker.swatches = null;
colorPicker.addEventListener('sl-change', update);
nameInput.addEventListener('sl-input', update);
window.addEventListener('DOMContentLoaded', update);
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
4.  Fertig.
