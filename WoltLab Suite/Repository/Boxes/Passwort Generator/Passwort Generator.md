

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.pass-container {
    background: #ccc;
    padding: 10px;
    width: 100%;
}

.result-container {
    background-color: #fff;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    position: relative;
    font-size: 18px;
    letter-spacing: 1px;
    padding: 12px 10px;
    height: 50px;
    width: 100%;
}

.result-container #result {
    word-wrap: break-word;
    max-width: calc(100% - 40px);
}

.result-container .btn {
    position: absolute;
    top: 5px;
    right: 5px;
    width: 40px;
    height: 40px;
    font-size: 20px;
}

.btn {
    border: none;
    background-color: #325C84;
    color: #fff;
    font-size: 16px;
    padding: 8px 12px;
    cursor: pointer;
}

.btn-large {
    display: block;
    width: 100%;
}

.setting {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 15px 0;
}    
</style>

<div class="pass-container">
      <p>Dein generiertes Passwort:</p>
      <div class="result-container">
        <span id="result"></span>
        <button class="btn jsTooltip" id="clipboard" title="Passwort kopieren">
          <i class="fa fa-clipboard" style="color: #fff;"></i>
        </button>
      </div>
      <div class="settings">
        <div class="setting">
          <label>Länge des Passwortes (4-20 Zeichen)</label>
          <input type="number" id="length" min="4" max="20" value="20" />
        </div>
        <div class="setting">
          <label>Mit großen Zeichen</label>
          <input type="checkbox" id="uppercase" checked />
        </div>
        <div class="setting">
          <label>Mit kleinen Zeichen</label>
          <input type="checkbox" id="lowercase" checked />
        </div>
        <div class="setting">
          <label>Mit Zahlen</label>
          <input type="checkbox" id="numbers" checked />
        </div>
        <div class="setting">
          <label>Mit Symbolen</label>
          <input type="checkbox" id="symbols" checked />
        </div>
      </div>
      <button class="btn btn-large" id="generate">Passwort generieren</button>
    </div>

<script>
'use strict';
const resultEl = document.getElementById('result'),
  lengthEl = document.getElementById('length'),
  uppercaseEl = document.getElementById('uppercase'),
  lowercaseEl = document.getElementById('lowercase'),
  numbersEl = document.getElementById('numbers'),
  symbolsEl = document.getElementById('symbols'),
  generateEl = document.getElementById('generate'),
  clipboardEl = document.getElementById('clipboard');

const randomFunc = {
  lower: getRandomLower,
  upper: getRandomUpper,
  number: getRandomNumber,
  symbol: getRandomSymbol,
};

clipboardEl.addEventListener('click', () => {
  const textarea = document.createElement('textarea'),
    password = resultEl.innerText;

  if (!password) return;

  textarea.value = password;
  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand('copy');
  textarea.remove();
  alert('Passwort wurde kopiert!');
});

generateEl.addEventListener('click', () => {
  const length = +lengthEl.value,
    hasLower = lowercaseEl.checked,
    hasUpper = uppercaseEl.checked,
    hasNumber = numbersEl.checked,
    hasSymbol = symbolsEl.checked;

  resultEl.innerText = generatePassword(
    hasLower,
    hasUpper,
    hasNumber,
    hasSymbol,
    length
  );
});

function generatePassword(lower, upper, number, symbol, length) {
  let generatedPassword = '';
  const typesCount = lower + upper + number + symbol,
    typesArr = [{ lower }, { upper }, { number }, { symbol }].filter(
      (item) => Object.values(item)[0]
    );
  if (typesCount === 0) {
    return '';
  }

  for (let i = 0; i < length; i += typesCount) {
    typesArr.forEach((type) => {
      const funcName = Object.keys(type)[0];
      generatedPassword += randomFunc[funcName]();
    });
  }

  const finalPassword = generatedPassword.slice(0, length);

  return finalPassword;
}

function getRandomLower() {
  return String.fromCharCode(Math.floor(Math.random() * 26) + 97);
}

function getRandomUpper() {
  return String.fromCharCode(Math.floor(Math.random() * 26) + 65);
}

function getRandomNumber() {
  return String.fromCharCode(Math.floor(Math.random() * 10) + 48);
}

function getRandomSymbol() {
  const symbols = '!@#$%*&(){}[]=<>/,.';
  return symbols[Math.floor(Math.random() * symbols.length)];
}
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
