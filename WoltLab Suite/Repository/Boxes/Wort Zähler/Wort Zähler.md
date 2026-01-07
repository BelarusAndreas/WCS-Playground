

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.ui-input-container {
  background-color: #ccc;
  padding: 10px;
  width: 100%;
  margin: 0 auto;
}
.ui-input-container h2 {
  font-family: sans-serif;
  margin-bottom: 20px;
  font-weight: 700;
  text-transform: capitalize;
}
.ui-form-input-container {
  position: relative;
  font-size: 1rem;
  margin-bottom: 15px;
  display: block;
}
.ui-form-input {
  padding: 13px 15px;
  border: 2px solid #245269;
  outline: 0;
  width: 100%;
}
.form-input-label {
  position: absolute;
  top: -7px;
  left: 10px;
  color: #1a73e8;
  font-size: 0.85rem;
  padding-right: 0.33rem;
  padding-left: 0.33rem;
  background: #fff;
  transition: all 0.15s cubic-bezier(0.4, 0, 0.2, 1);
  font-family: sans-serif;
  text-transform: capitalize;
}
.ui-form-btn {
  padding: 13px 15px;
  border-radius: 8px;
  background: #1a73e8;
  outline: 0;
  width: 100%;
  border: none;
  cursor: pointer;
  font-size: 1rem;
  color: white;
  font-weight: 500;
}
.error .ui-form-input,
.error .form-input-label {
  border-color: #d50000;
  color: #d50000;
}
textarea {
  min-height: 6em;
  max-height: 50vh;
  width: 100%;
}
</style>

<div class="ui-input-container">
  <label class="ui-form-input-container">
    <textarea class="ui-form-input" id="word-count-input" placeholder="Hier deinen Text eingeben."></textarea>
    <span class="form-input-label">Nachricht</span>
  </label>
  <p aria-live="polite">Dein Text enthält <strong><span id="word-count">0</span></strong> Wörter und <strong><span id="character-count">0</span></strong> Zeichen.</p>
</div>

<script>
var countTarget = document.querySelector("#word-count-input");
var wordCount = document.querySelector("#word-count");
var characterCount = document.querySelector("#character-count");
var count = function () {
  var characters = countTarget.value;
  var characterLength = characters.length;
  var words = characters.split(/[\n\r\s]+/g).filter(function (word) {
    return word.length > 0;
  });
  wordCount.innerHTML = words.length;
  characterCount.innerHTML = characterLength;
};
count();
window.addEventListener(
  "input",
  function (event) {
    if (event.target.matches("#word-count-input")) {
      count();
    }
  },
  false
);
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
