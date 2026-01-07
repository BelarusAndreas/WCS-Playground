
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
  height: 100vh;  
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
  '"Ich hab‘ vorhin ein Schnitzel gegessen mit Gurkensalat. Und der Gurkensalat war musikalischer als Du."',
  '"Es gibt Stimmen, da kommt was rüber. Und es gibt Stimmen, da kommt nix rüber. Bei Dir kommt noch nicht mal nix rüber."',
  '"Also bist Du weiter - weiter weg vom Recall als jeder vorher."',
  '"Du hast keinen Star-Appeal. Du hast nix. Am liebsten würde ich dir ein Euro geben. Das ist alles Mitleid."',
  '"Du triffst weder die Töne noch hast du ein Rhythmusgefühl. Das war so ziemlich Top Five der Schlechtesten. Vielleicht kannst du versuchen, mit der Stimme den Leuten die Beine zu enthaaren."',
  '"Deine Freunde sagen ja, dass sie möchten, dass du das gewinnst. An deiner Stelle würde ich mir deine Freunde noch mal genau angucken."',
  '"Das wird nie was. Diese Tanzerei war ein nettes Dessert, hat mir gut geschmeckt. Der Gesang war wie so eine Fischvergiftung."',
  '"Normalerweise sagt man zu einem Kandidaten: ‚Komm, gib nicht auf!‘ Aber bei Dir würde ich da echt eine Ausnahme machen. Also ich würde an Deiner Stelle echt aufgeben."',
  '"Wollt Ihr wissen, was der Unterschied zwischen Eurer Stimme und einem Eimer Scheiße ist? Der Eimer!"',
  '"Du hast es versucht. Nein. Nein. Nein. - „Was hast Du bei drei Mal ‚Nein‘ nicht verstanden?"',
  '"Ich könnte dich in meinem Garten vergraben, als Kompost für die Blumen."',
  '"Da ist die Frage: Wo hört der Gesang auf und wo fängt die Straftat an?"',
  '"Wenn ich mir morgens einen Pickel ausdrücke, dann hat das mehr Power als deine Stimme."',
  '"Deshalb haben irgendwelche Leute Drogen erfunden - um Menschen wie dich auszuhalten."',
  '"Kann ich das irgendwie noch verhindern, dass du Musiklehrer wirst?"',
  '"Das ist Darmverschluss - und das ist scheiße."',
  '"Bei mir kommen solche Geräusche aus anderen Öffnungen."',
  '"Selbst mein Wellensittich würde nicht so hoch kommen, wenn ich auf ihn drauf trete. Du hast mich überrascht!"',
  '"Du bist ein Mensch wie Gott ihn geschaffen und McDonalds ihn geformt hat."',
  '"Ne Steigerung wär es, wenn dein Popel tanzen könnte."',
  '"Ich kann nicht mal sagen dass das scheiße war, das war schlechter. Wenn Du mir einen Affen mitgibst für ein halbes Jahr, dann singt der besser."',
  '"Wenn du jetzt 3000 Prozent besser singst, könntest du eventuell Scheiße erreichen."',
  '"Du hast keinen Starappeal. Du hast nix. Am liebsten würde ich dir einen Euro geben. Das ist alles Mitleid."',
  '"Du kneifst die Augen zusammen wie ich beim Kacken."',
  '"Bei mir ist das Problem: Soll ich dir helfen oder dich notschlachten?"',
  '"Du triffst weder die Töne, noch hast du ein Rhythmusgefühl. Das war so ziemlich Top 5 der Schlechtesten. Vielleicht kannst du versuchen mit der Stimme den Leuten die Beine zu enthaaren."',
  '"Ich würde auch fünf Kilogramm Hackfleisch in die Charts kriegen."',
  '"Ich bin ja die Klobürste von DSDS – an mir bleibt immer die Scheiße hängen."',
  '"Du klingst, wie wenn ein Schaf an den Elektrozaun pinkelt."',
  '"Klopups-Imitator - da hast du genau die richtige Stimme für. Weißt du, wenn du auf dem Klo sitzt und neben dir sitzt ein anderer, und du singst und der furzt, dann denkt ihr beide, ihr singt im Duett."',
  '"Deine Stimme klingt ätzend! Ätzend für einen Kloreiniger ist geil, ätzend für eine Stimme ist scheiße."',
  '"Du bist wie eine Wolke. Wenn du dich verziehst, könnte es noch ein schöner Tag werden."',
  '"Bei normalen CDs ist ja immer so ein Booklet dabei. Bei dir müsste das eine Kotztüte sein."',
  '"Du hast eine vorbildliche Einstellung. Wenn nur diese Scheiß-Stimme nicht wäre."',
  '"Wir suchen hier Vulkanausbrüche und keine Furzfontänen."',
  '"Ich glaube, dass du zu den Leuten gehörst, die keine Ahnung von Musik haben und denken, die Zauberflöte ist von Beate Uhse."',
  '"Man spürt, dass du die Musik liebst, aber diese Liebe ist einseitig."',
  '"Wir sind Talentsucher und keine Müllsortierer."',
  '"Dein Outfit ist aber mehr out als fit."',
  '"Für mich bist du im Finale - im finalen Endstadium."',
  '"Das Einzige, was du hier zu suchen hast, ist der Ausgang."',
  '"Wenn du deine Stimmbänder in Säure schmeißt, dann haben wir ein gelöstes Problem."',
  '"Du musst nicht traurig sein. Guck mal, Schweine können z.B. nicht Stabhochspringen und sind deshalb auch nicht traurig."',
  '"Wenn DAS die Nummer ist, bei der du aus dir rausgehst, dann bleib mal besser in dir drin."',
  '"Das klingt, als wenn sie dir den Arsch zugenäht haben und die Scheiße oben raus kommt."',
  '"Also wenn Du bei mir im Keller singen würdest, würden die Kartoffeln freiwillig geschält nach oben kommen."',
  '"Du triffst noch nicht mal dann einen Ton, wenn er genau vor dir steht."',
  '"Wenn schlechte Stimmen fliegen könnten, wärst du ein Satellit."',
  '"Du gehörst zu der Abteilung musikalischer Bildschirmschoner. Da passiert nix.',
  '"Lieber Cholera am Pillermann, als dein Gesang!"',
  '"Du hast einfach nichts drauf, außer vielleicht Zahnbelag."',
  '"Wenn du deine Stimme zwischen zwei Mülltonnen stellst, können wir da ein schönes Familienfoto von machen."',
  '"Du bist ein hübsches Mädchen, du kannst doch auch einfach etwas anderes machen."',
  '"Wir suchen hier nach Pralinen und dann stehen da immer irgendwelche Lutscher!"',
  '"Das ist fast aktive Sterbehilfe, wenn du singst!"',
  '"Weißt du, was Durchfall ist? So ähnlich war dein Auftritt: es war zwar flüssig aber am Ende bleibt es trotzdem Scheiße."',
  'Die hohen Töne klingen lebensgefährlich für mich."',
  '"Ich habe heute Morgen in der Zeitung gelesen, dass 80 Prozent der Deutschen nicht singen können. Davon warst du 79 Prozent."',
  '"Wenn ich dich zum Singen in den Park stelle, dann bringen die Vögel die Kirschen vom letzten Jahr zurück!"',
  '"Den ganzen Vormittag hatte ich das Gefühl, am Abgrund zu stehen. Mit dir sind wir einen Schritt weiter."',
  '"Du piepst rum wie ein schwangerer Wellensittich."',
  '"Ich stelle mir das so vor: Wenn ich im Auto sitze und ich höre das im Radio, dann würde ich anhalten und gucken, ob ich eine Katze überfahren habe."',
  '"Du hast schwach angefangen und stark nachgelassen."',
  '"Ich kann dir nur einen super guten Tipp geben: lass das Singen für alle Zeiten. Verschon die Menschheit!"',
  '"Wenn das Wetter so wäre wie deine Stimme, würde es Scheiße regnen!"',
  '"Jeder Specht im Wald hat mehr Taktgefühl als du."',
  '"Wenn du deine Stimmbänder in die Mülltonne schmeißt, ist das artgerechte Haltung."',
  '"Solange wir in Deutschland Stimmen haben wie deine, müssen wir uns nicht wundern, dass die Geburtenrate sinkt."',
  '"Wenn im Schweinestall die Sau rumgrunzt, findet der Eber das ja auch geil, aber ICH deshalb noch lange nicht."',
  '"Im Recall würdest du nicht länger überleben als ein Tampon im Piranha-Becken!"',
  '"Eins hast du, nämlich deinen eigenen Stil. Aber den finde ich absolut scheiße."',
  '"Nicht jeder Mensch mit Stimme kann Sänger werden. Jeder Mann hat einen Steifen, aber nicht jeder spielt im Porno mit."',
  '"Du musst dich auch mal angucken, im Spiegel zu Hause. Das sieht irgendwie so aus, als wäre ein seltsames Tier in deinem Gesicht gestorben.',
  '"Persönlichkeit wie eine Bockwurst. Jeder isst das, aber: Fällt nicht besonders auf."',
  '"Der Nachteil bei dir ist, dass du keinen Vorteil hast."',
  '"Wenn du auf der Straße stehst und singst, dann berechnet mein Navigationsgerät automatisch eine Umleitung."',
  '"Das Ding heißt hier nicht: Deutschland sucht Naturkatastrophen."',
  '"Wenn du in die Berge gehst und rufst: Hallo Echo - dann kommt nicht mal ein Echo, weil Echos haben auch Geschmack."',
  '"Sonst sagt man den Kandidaten immer: Gibt nicht auf! Aber bei dir würde ich da eine Ausnahme machen."',
  '"Wenn die Kelly Clarkson morgens aufs Klo geht und in die Schüssel pinkelt, klingt das immer noch besser als dein Gesang."',
  '"Wenn ich meinem Hund eine Currywurst in den Hintern schiebe, dann macht der auch solche Geräusche."',
  '"Einen Vorteil hat dein Gesangsstil: Wenn du in der Kneipe auftrittst, und die Leute müssen kotzen, die kotzen noch nicht mal in deine Richtung."',
  '"Weißt du was uns trennt? So schätzungsweise 130 Millionen verkaufte Platten."',
  '"Die Stimme, die du hast, reicht vielleicht zum Eier-Abschrecken."',
  '"Slatko, John, Jürgen & Co sind keine Stars, sondern Eintagsfliegen, die alle auf die Klatsche warten."',
  '"Als Fußballer magst du was taugen, aber wenn du singst, flüchtet die Eckfahne."',
  '"Dein Talent liegt bei null und da habe ich noch aufgerundet."',
  '"Das klang nicht wie gebrochenes Spanisch, sondern wie erbrochenes Spanisch."',
  '"Du bist ein Gesangs-Tsunami der ersten Klasse."',
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
