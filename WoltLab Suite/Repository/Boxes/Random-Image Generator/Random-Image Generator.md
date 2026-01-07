

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.image-generator {
  background: #ccc;
  width: 100%;
  margin: auto;
  padding: 40px 20px;
}
.form {
  width: 100%;
  margin-bottom: 20px;
}
.form-label {
  text-shadow: 1px 1px #fff;
  display: block;
  padding: 10px 10px 10px 0;
}
.form-input {
  width: 100%;
  background: #fff;
  border: 3px solid transparent;
  border-radius: 3px;
  height: 45px;
  line-height: 45px;
  padding: 0 40px 0 10px;
  margin-bottom: 20px;
  transition: 0.3s ease all;
}
.form-submit {
  font-weight: bold;
  border: none;
  border-radius: 3px;
  margin-top: 25px;
}
.form-submit:hover {
  box-shadow: 3px 0px 30px rgba(163, 163, 163, 1);
}
.img-result {
    max-width: 100%;
    max-height: 100%;
    object-fit: cover; 
}
</style>

<div class="image-generator">
  <form action="" class="form" id="form">
    <label for="width" class="form-label">Breite:</label>
    <input type="number" class="form-input" id="width" name="width" />
    <label for="height" class="form-label">Höhe:</label>
    <input type="number" class="form-input" id="height" name="height" />
    <button type="submit" class="form-submit button">Bild Generieren</button>
  </form>
  <img alt="" id="img" class="img-result"/>
</div>

<script>
const getImage = () => {
  const width = document.getElementById("width").value;
  const height = document.getElementById("height").value;
  const url = `https://picsum.photos/${width}/${height}`;
  const image = document.getElementById("img");
  image.src = url;
};
const form = document.getElementById("form");
form.addEventListener("submit", (e) => {
  e.preventDefault();
  getImage();
});
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
