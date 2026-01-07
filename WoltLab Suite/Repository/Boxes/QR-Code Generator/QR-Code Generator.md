

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.qrcodeContent {
    background: #ccc;    
}
.wrapper {
  height: 265px;
  max-width: 100%;
  padding: 20px 25px 0;
  transition: height 0.2s ease;
}
.wrapper.active {
  height: 530px;
}
.wrapper .qrcodeform {
  margin: 20px 0 25px;
}
.qrcodeform :where(input, button) {
  width: 100%;
  height: 55px;
  border: none;
  outline: none;
  border-radius: 5px;
  transition: 0.1s ease;
}
.qrcodeform input {
  font-size: 18px;
  padding: 0 17px;
  border: 1px solid #999;
}
.qrcodeform input:focus {
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.13);
}
.qrcodeform input::placeholder {
  color: #999;
}
.qrcodeform button {
  color: #fff;
  cursor: pointer;
  margin-top: 20px;
  font-size: 17px;
  background: #3498db;
}
.qrcodesubmit {
  color: #fff;
  cursor: pointer;
  margin-top: 20px;
  font-size: 17px;
  background: #3498db;
}
.qr-code {
  opacity: 0;
  display: flex;
  padding: 33px 0;
  border-radius: 5px;
  align-items: center;
  pointer-events: none;
  justify-content: center;
  border: 1px solid #ccc;
}
.wrapper.active .qr-code {
  opacity: 1;
  pointer-events: auto;
  transition: opacity 0.5s 0.05s ease;
  background: #fff;
}
.qr-code img {
  width: 170px;
}
@media (max-width: 430px) {
  .form :where(input, button) {
    height: 52px;
  }
  .qr-code img {
    width: 160px;
  }
}
</style>

<div class="wrapper qrcodeContent">
  <div class="qrcodeform">
    <input name="text" type="text" spellcheck="false" placeholder="Text oder URL eingeben ">
    <input class="qrcodesubmit" type="submit" value="QR-Code generieren">
  </div>
  <div class="qr-code">
    <img src="" alt="qr-code">
  </div>
</div>

<script>
const wrapper = document.querySelector(".wrapper"),
  qrInput = wrapper.querySelector(".qrcodeform input"),
  generateBtn = wrapper.querySelector(".qrcodesubmit"),
  qrImg = wrapper.querySelector(".qr-code img");
let preValue;

generateBtn.addEventListener("click", () => {
  let qrValue = qrInput.value.trim();
  if (!qrValue || preValue === qrValue) return;
  preValue = qrValue;
  generateBtn.innerText = "Generiere QR Code...";
  qrImg.src = `https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=${qrValue}`;
  qrImg.addEventListener("load", () => {
    wrapper.classList.add("active");
    generateBtn.innerText = "QR-Code generieren";
  });
});

qrInput.addEventListener("keyup", () => {
  if (!qrInput.value.trim()) {
    wrapper.classList.remove("active");
    preValue = "";
  }
});
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
