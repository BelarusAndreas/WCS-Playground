

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
textarea {
    display: block;
    width: 100%;
    height: 250px;
}
.minified {
    background: #fff;
    color: #000;
    padding: 10px;
    width: 100%;
    height: 250px;
    word-break: break-all;
    word-wrap: break-word;
    margin: 10px 0 0 0;
}
.minifie-options {
    background: #ccc;
}
#html-submit {
    margin: 0 auto;
    display: block;
    text-align: center;
    background: #245269;
    color: #fff;
}
#html-submit:hover {
    background: #78909C;
}
#html-submit span {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: rotate(0deg) translate(-50%,-50%);
    display: none;
    height: 25px;
    width: 25px;
    border-radius: 50%;
    border: 4px solid rgb(62, 154, 235);
    z-index: 5;
    border-top-color: rgb(196, 203, 209);
    border-bottom-color: rgb(54, 119, 209);
    animation: rotate 1s linear infinite;
}
@keyframes rotate {
    0%{ transform:translate(-50%,-50%) rotate(0deg); }
    100%{ transform:translate(-50%,-50%) rotate(350deg); }
}
</style>

<div>
  <textarea name="html" rows=20 placeholder="Füge hier deinen JS ein."></textarea>
  <div class="minifie-options">
    <div onclick="minify(this.parentNode.querySelector('textarea').value)" id="html-submit" class="button"><span></span>Minimieren</div>
    <h3><span id="original"></span>Ergebnis:<span id="final"></span></h3>
    <div class="minified"></div>
  </div>
</div>

<script>
let button=""
function minify(div) {
    button=document.querySelector("#html-submit");
    // button.firstChild.style.display="block";
    // button.setAttribute('disabled',true);
    // button.textContent="Minifying";
    let originalSize= `${((div.toString().length)/1024).toFixed(3)}KB`;
    patterns = ["\n"," =","= "," ;", "; ", " {", "{ ", " }", "} ", " :", ": ",", "," ,","[ "," ["," ]","] "];
    replacePatterns = ["","=","=",";", ";", "{", "{", "}", "}", ":", ":",",",",","[","[","]","]"];
    this.patterns.forEach((value, i) => {
        while (div.includes(value)) {
            div = div.replace(value, this.replacePatterns[i]);
        }
    });
    let finalSize= `${((div.toString().length)/1024).toFixed(3)}KB`;
    document.querySelector(".minified").textContent = div;
    document.querySelector("#original").innerHTML = originalSize;
    document.querySelector("#final").innerHTML = finalSize;
    // button.removeAttribute("disabled");  
}
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
