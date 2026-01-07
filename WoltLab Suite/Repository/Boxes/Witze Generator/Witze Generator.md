

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar
 - Bereits 50 Witze mit inbegriffen

### Quellcode
```
<style>
.phrase-generator {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: auto;  
}
.generate {
  margin: 0 auto;
  text-align: center;
}
.phrase {
  color: #000;
  font-size: 1.2rem;
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
  '"Eine Blondine missachtet das rote Licht. Der Verkehrspolizei stoppt sie und fragt: Haben Sie nicht gesehen, wie ich Ihnen gewinkt habe? Ich habe es gesehen, ich bin aber verheiratet!"',
  '"Der neue Nachbar kauft eine neue Wohnung und fragt: Ist die Wohnung leise? Sehr leise. Der vorherige Inhaber wurde erschossen und keiner hat es gehört."',
  '"Der Sohn kommt nach der Schule nach Hause und sagt: Papa! Ich habe das nicht verstanden: Es ist die erste Klasse, aber die Bänke sind aus Holz!"',
  '"Volksweisheit: Gut, die Hälfte der Verkehrspolizei nimmt Schwarzgeld, die böse Hälfte nimmt auch den Führerschein mit."',
  '"Zwei Verkehrspolizei stehen an einer Radarfalle. Da fährt jemand zu schnell! Wie schnell? Etwa 50 Euro!"',
  '"Doktor. Mein Mann ist sehr krank. Was kann ich tun? Zuerst muss man eine Diagnose ermitteln. Ziehen Sie sich aus und zeigen sie mir, wo er Schmerzen hat."',
  '"Russland und Deutschland spielen Fußball, 0:3, Deutschland gewinnt. Ein alter Mann sagt:  Los! Los! Wir haben doch 1945 gewonnen! In der Nähe sitzt ein Georgier und sagt: Opa! Damals hatten die Russen einen anderen Trainer."',
  '"Iwan! wir haben nichts zum Essen zu Hause! Lass mich in Ruhe. Iwan, war haben keine Socken ohne Löcher mehr! Lass mich! Ich konnte fürs Internet noch nicht bezahlen und du störst mich mit unwichtigen Dummheiten!"',
  '"Ein Mann kauft ein Gemälde bei einem Maler und fragt: Warum ist auf dem Gemälde alles so verschwommen und unverständlich? Weil ich es so sehe. Na cool! Warum trägst du denn keine Brille?"',
  '"Die Ehefrau kommt nach Hause und fragt: Bist du allein? Vielleicht ja? Warum so unsicher? Ich weiß nicht, ob man Hausmädchen dazu zählen kann oder nicht?"',
  '"Zwei Autofahrer: Gestern habe ich mir einen neuen Antiradar gekauft. Und? Ich habe aber nicht gesehen, dass er nach Vorgaben der Verkehrspolizei erstellt wurde. Na und? Jetzt meldet er jedes Mal, wenn noch 300 Meter bis zur Verkehrspolizei bleiben: Hol dein Geld raus! Hol dein Geld ..."',
  '"Zwei Kollegen unterhalten sich: Weißt du, unser Buchhalter ist ein Betrüger. Aber ein fairer Mensch. Wie kann es sein? Er betrügt alle ohne Ausnahme."',
  '"Hallo, ist dies das Restaurant? Ja. Wir würden gern einen Tisch für 7 Uhr bestellen. Ok, und was ist mit den Stühlen?"',
  '"Kellner! Ich habe eine Fliege in der Suppe! Das macht nichts. Die Spinne auf dem Brot wird sie bestimmt fangen."',
  '"Besucher: Was für ein Restaurant ist das? Kein Fleisch! Kein Hummer! Keine Oliven! Bringen Sie mir meinen Mantel. Der Kellner: Entschuldigen Sie, es gibt aber Ihren Mantel auch nicht mehr."',
  '"Im Zug. In jedes Abteil schaut eine Schaffnerin mit einem netten Lächeln und fragt: Gibt es hier Ausländer? Nein. Sie findet keine Ausländer im Zug und sagt: Wasja! Die Klimaanlage kann ausgeschaltet werden. Es fahren nur Landsleute mit."',
  '"Schaffner! Was soll das! Was für einen Zug ist das hier? Ich bin gerade eingestiegen, als mein Koffer schon gestohlen wurde.Der Schaffner: Kein Wunder. Es ist ein Schnellzug."',
  '"Der Sohn schaut zu, wie sein Vater die Decke streicht. Mutter sagt: Schau zu und lerne! Wenn du größer wirst, wirst du dem Vater helfen können. Warum? Wird mein Vater bis dahin nicht fertig damit?"',
  '"Lehrerin zu Erwin: Warum sind in deinem Test die gleichen Fehler wie bei deiner Schulbanknachbarin Sabine? Wir haben doch die gleiche Lehrerin."',
  '"Mathematikunterricht. Die Lehrerin fragt Erwin. Stelle dir mal vor, ich gebe dir 200$. Du gibst Mascha 50$, Lena 50$, Natascha 50$. Was hast du dann? Eine Orgie."',
  '"Erin du bist schon 6 Jahre alt. Und ich muss dir erzählen, woher die Kinder kommen. Na so was. Mit 3 habe ich gelernt, dass es keinen Weihnachtsmann gibt. Und wenn sich herausstellt, dass Leute keinen Sex haben, woran soll ich dann noch glauben?!?"',
  '"Erwin, gib mir ein Beispiel für einen Satz ohne Verb. Meine Tante: Nutte. Was für Wörter sind das? Gehe sofort zum Direktor! In der Pause fragen alle, was mit Erwin, der gerade einen Apfel ist, passiert ist: Was ist los? Was hat dir Direktor gesagt? Erwin sagt ruhig: Der Direktor gab mir einen Apfel und fragte nach der Adresse meiner Tante."',
  '"Ich gebe dir 10$, wenn du zum Bahnhof fährst und meine Schwiegermutter abholst. Und was ist, wenn sie nicht ankommt? Dann bezahle ich das Doppelte."',
  '"Die Schwiegermutter kommt zu ihrem Schwiegersohn: Lieber Schwiegersohn! Hier sind 100.000 $. Mach, was du willst, ich will aber hier begraben werden. Am nächsten Morgen kommt der Schwiegersohn zu seiner Schwiegermutter. Liebe Schwiegermutter. Mach was du willst, aber das Begräbnis findet heute um 12 Uhr statt."',
  '"Was ist gleichzeitig eine gute und eine schlechte Nachricht? Es ist, wenn du siehst, wie deine Schwiegermutter in deinem Auto in die Schlucht fällt."',
  '"Zwei Alkoholiker treffen einander: Peter, trinken wir? Nein, jetzt will ich nicht. 10 Sekunden später: Und jetzt?"',
  '"Der Betrunkene steigt in den Bus ein und setzt sich neben eine alte Dame. Die Dame: Wissen Sie, junger Mann, Sie kommen aber so in die Hölle! Der Betrunkene steht auf und sagt dem Fahrer: Halt! Halt! Ich bin in den falschen Bus eingestiegen."',
  '"Eine Frage ans Radio: Kann man in einem Land Sozialismus einführen? Im Prinzip ja, man kann in einem Land Sozialismus einführen, dabei wird man aber gezwungen, in einem anderem Land zu wohnen."',
  '"Wo ist der Unterschied zwischen Videoclips von Britney Spears und Pornofilmen? Die Antwort: Die Musik in den Pornofilmen ist besser."',
  '"Warum reden die Frauen oft über die Liebe und die Männer über Sex? Die Antwort: Frauen sagen nicht immer das, was sie denken."',
  '"Was soll eine Frau machen, um 10 Jahre jünger auszusehen. Die Antwort: Sie muss 10 Jahre später geboren werden."',
  '"Kann ein Film ein Happy End haben, falls die Hauptfigur stirbt? Die Antwort: Ja, wenn die Hauptfigur die Schwiegermutter ist."',
  '"Welche Fremdsprache ist am schwierigsten zu lernen: Chinesisch oder Hebräisch? Die Antwort: Ukrainisch, da die Hälfte der Ukrainer es selbst immer noch nicht gelernt hat."',
  '"Genosse Tschuktsche: Bei euch in Tschukotka, ist das Klima so langweilig, kalt. Vielleicht gibt es auch keine Abwechslung im Leben. Nein, natürlich gibt es genug Abwechslung! Ok, was machst du im Sommer? Im Sommer gehe ich Angeln und schlafe mit meiner Frau. Und im Winter? Im Winter gehe ich nicht angeln."',
  '"In der Nacht klopft jemand an der Tür. Rabinowitsch: Wer ist da?. Geheimdienst. Machen Sie auf! Wir müssen reden. Rabinowitsch: Und wie viele seid ihr?. Zu zweit. Dann redet miteinander!"',
  '"Haben Sie die Möglichkeit, Geld zu sparen? Die Möglichkeit habe ich, nur das Geld dafür habe ich nicht."',
  '"Russen und Estländer stecken im Fahrstuhl fest und rufen um Hilfe: Hilfe! Hilfe! Die Russen sagen: Lassen Sie uns zusammen rufen. Die Estländer schauen einander an und rufen dann: Zusammen! Zuuusaaammen!"',
  '"Wie kann man den Amerikaner dazu bringen, vom Eiffelturm zu springen? Man kann ihm sagen, dass seine Firma Bankrott ist. Wie kann man den Franzosen dazu bringen, vom Eiffelturm zu springen? Man kann ihm sagen, dass seine Frau ihn für ihre Liebhaber verlassen hat. Wie kann man den Russen dazu bringen, vom Eiffelturm zu springen? Man sollte ein Schild aufhängen: Springen vom Turm ist strengstens verboten!"',
  '"Eine Engländerin, eine Französin und eine Russin vor dem Schönheitswettbewerb. Die Frage: Stellen Sie sich vor, dass sie auf einer unbewohnten Insel mit 20 Männern sind. Was würden Sie tun? Die Engländerin: Beten und Gott um Hilfe bitten. Die Französin: Ich werde den Stärksten finden und er wird mich beschützen. Die Russin: Die Frage habe ich verstanden, aber wo ist das Problem?"',
  '"Der Amerikaner mag sein Land und hasst alle, die seine Meinung nicht vertreten. Der Russe hasst sein Land und hasst alle, die mit ihm einer Meinung sind."',
  '"Gorbatschjow kommt nach Hause und sieht, dass die ganzen Möbel aus der Wohnung getragen worden sind, Tür und Fenster sind zerbrochen, weder Licht noch Gas, irgendwelche Leute ziehen das Parkett ab. Gorbatschjow: Was ist hier los? Perestrojka - Umbau!"',
  '"Perestroika begann im April 1986 und wurde im April 2007 beendet. So hat Russland einen Weltrekord erreicht: Ein Aprilscherz, der 21 Jahre ohne Pause auf einem Gebiet von 17000000 km2 stattgefunden hat. Wer kann das noch?"',
  '"Papa, sag mal. Beginnen alle Märchen mit: Es war einmal...? Nein, mein Sohn. Die besten Märchen beginnen mit: Wenn Sie mich wählen..."',
  '"Zwei Obdachlose sitzen auf der Müllkippe. Der erste: Hast du gehört? Es herrscht eine Krise in der Stadt. Der zweite: Was heißt das? Na z.B. kennst du Oligarchen? Nein. Bald wirst du sie kennenlernen"',
  '"Direktor an seine Mitarbeiter: Sie alle beschweren sich wegen der Krise, wegen der Verschlechterung des Lebens. Ihr Gehalt ist übrigens 75% höher. Entschuldigen Sie, höher als was? Als ihr Gehalt im nächsten Jahr."',
  '"Leutnant, warum reden wir immer wieder über Frauen, Frauen, Frauen. Lassen Sie uns über Musik oder Musikinstrumente reden. Ja, ja, über Musik. Ich habe neulich mit einer Frau auf dem Klavier Sex gehabt. Sehr glattes Musikinstrument"',
  '"Ein Deutscher fragt einen Russen. Was machst du für deine Gesundheit. Der Russe: Für die Verdauung Wodka, für zu niedrigen Blutdruck Rotwein und für zu hohen Blutdruck Cognac. Der Deutsche: Und was ist mit Wasser? Der Russe: So eine Krankheit kenne ich nicht."',
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
