

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.placeholder-generator {
    background: #ccc;
    text-shadow: 1px 1px #fff;
}
.placeholder-generator h3 {
    font-size: 1.2em;
}
.input {
    height: 30px;
    box-sizing: border-box;
}
#inputWidth, #inputHeight {
    width: 80px;
}
#inputDataUrl {
    width: 100%;
    max-width: 600px;
}
#imagePreview {
    width: 100%;
}
</style>
<div class="placeholder-generator">
  <h3>Größe</h3>
  <p>Angaben sind in Pixeln (px) zu machen.</p>
  <input type="number" class="input" id="inputWidth" value="400"> x <input type="number" class="input" id="inputHeight" value="300"> <button id="buttonGenerate" type="button">Generieren</button>
  <h3>Data URL</h3>
  <p>Kopiere den Code und füge ihn im img-Tag ein.</p>
  <input type="text" class="input" id="inputDataUrl" placeholder="Generiere zuerst ein Placeholder." readonly>
  <h3>Vorschau</h3>
  <p>Rechtsklich und "speichern unter" wählen um das Bild herunterzuladen.</p>
  <img alt="Preview Image" id="imagePreview" style="display: none">
</div>

<script>
function createPlaceholderCanvas(width, height) {
    const element = document.createElement("canvas");
    const context = element.getContext("2d");
    element.width = width;
    element.height = height;
    context.fillStyle = "#aaaaaa";
    context.fillRect(0, 0, element.width, element.height);
    context.font = "bold 25px sans-serif";
    context.fillStyle = "#333333";
    context.textAlign = "center";
    context.textBaseline = "middle";
    context.fillText(`${width}x${height}`, element.width / 2, element.height / 2);
    return element;
}
const inputWidth = document.getElementById("inputWidth");
const inputHeight = document.getElementById("inputHeight");
const inputDataUrl = document.getElementById("inputDataUrl");
const imagePreview = document.getElementById("imagePreview");

document.getElementById("buttonGenerate").addEventListener("click", () => {
    const MIN_SIDE_LENGTH = 200;
    if (
        isNaN(inputWidth.value)
        || isNaN(inputHeight.value)
        || inputWidth.value < MIN_SIDE_LENGTH
        || inputHeight.value < MIN_SIDE_LENGTH
    ) {
        alert(`Bitte gebe eine Mindestlänge von ${MIN_SIDE_LENGTH}px an.`);
        return;
    }
    const canvasElement = createPlaceholderCanvas(inputWidth.value, inputHeight.value);
    const dataUrl = canvasElement.toDataURL();
    inputDataUrl.value = dataUrl;
    imagePreview.src = dataUrl;
    imagePreview.style.display = "block";
    imagePreview.style.maxWidth = `${inputWidth.value}px`;
});
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
