

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.phrase-generator {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: auto;  
  min-height: 100px; 
}
.generate {
  margin: 0 auto;
  text-align: center;
}
.phrase {
  color: #000;
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 2rem;
  text-align: center;  
}
</style>

<div class="phrase-generator">
  <div class="phrase"></div>
  <div class="generate">
    <button class="button" id="generateButton">Generieren</button>
  </div>
</div>

<script>
const phrases = [
  'Pusteblume',
  '(O)-(O)',
  'Schmetterling',
  'Sauerkraut',
  'PissNelke',
  'Atomix',
  'BoeserOnkel',
  'Hexenkind',
  'Satansbraten',
  'DaBeatGoes',
  'W4rri0r',
  'DerWiXXeR',
  'Alphorn',
  'Marsianer',
  'H4cKeR',
  'Apollo13',
  'Gnom',
  'Fee',
  'T3rmin4t0r',
  'RoBoTiX',
  'Da-One',
  'Ich-bins',
  'Ich-wars-nicht',
  'R4nGeR',
  'Unschuldiger',
  'Helfer',
  'NoName',
  'Everless',
  'KinG',
  'Vollstrecker',
  'ArmyMan',
  'Godless',
  'CatWoman',
  'SuperPupa',
  'Chupa-Chups',
  'Kruzifix',
  'Musikantenstadl',
  'Seifenlauge',
  'Affenkind',
  'BieneMaja',
  'Asterix',
  'Obelix',
  'Skelleton',
  'Superman',
  'Mr.X',
  'Rate-mal',
  'Ich-sag-nichts',
  'RoBot',
  'Rotbart',
  'Robärt',
  'Rose',
  'Palmenwedler',
  'Deine-Seele',
  'P.Langstrumpf',
  'Sägeblatt',
  'Saugling',
  'DerAlte',
];

const phraseElement = document.querySelector('.phrase');
const generateButton = document.querySelector('#generateButton');

generateButton.addEventListener('click', () => {
  const randomIndex = Math.floor(Math.random() * phrases.length);
  const randomPhrase = phrases[randomIndex];
  phraseElement.textContent = randomPhrase;
  phraseElement.style.color = getRandomColor();
});

function getRandomColor() {
  const colors = ['red', 'orange', 'yellow', 'green', 'blue', 'purple']; /* Farbangabe (Name oder Hex-Code) der Sprüche */
  const randomIndex = Math.floor(Math.random() * colors.length);
  const randomColor = colors[randomIndex];
  return randomColor;
}
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
