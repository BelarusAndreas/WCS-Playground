
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.loremContent {
    background: #ccc;
    padding: 20px;
}
.text {
    height: 250px;
}
</style>

<div class="loremContent">
  <form class="generator">
    <label for="number">Anzahl der Paragraphen:</label>
    <input type="number" min="1" id="number" value="1" />
    <input type="button" value="Generieren" />
  </form>
  <br>
  <hr>
  <br>
  <p>Ergebnis:</p>
  <br>
  <textarea class="text"></textarea>
</div>

<script>
const generate = document.querySelector('input[type = "button"]');
const text = document.querySelector(".text");
const lorem =
  "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vero officia alias placeat quibusdam? Tempora ipsa non odit quo quod veritatis unde velit adipisci consequuntur, iste officiis nulla eum rem natus. Eveniet corrupti nam animi. Ut magni distinctio, ipsam sit totam voluptate corporis, dolores dolor hic quia modi neque corrupti numquam provident quo culpa illum itaque. Dicta, repellat aperiam optio minima harum illum officiis sint laudantium recusandae ipsa tempora inventore hic a dignissimos sed quod provident voluptatem molestiae dolorum eius amet, reprehenderit eligendi? Reprehenderit voluptates praesentium autem excepturi eligendi. Laboriosam earum aliquam ducimus facere? Quos praesentium sequi porro nemo molestias cum!";
function randomNum(min, max) {
  return Math.floor(Math.random() * (max - min + 1) + min);
}
function generateLorem() {
  const number = Number(document.querySelector('input[type = "number"]').value);
  const loremArg = lorem.split(" ");
  const emptyArg = Array(number).fill("");
  const randomLoremArg = emptyArg.map(() =>
    loremArg.slice(0, randomNum(20, 100)).join(" ")
  );
  text.innerHTML = randomLoremArg.map((lorem) => `${lorem}`).join("");
}
generate.addEventListener("click", generateLorem);
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
