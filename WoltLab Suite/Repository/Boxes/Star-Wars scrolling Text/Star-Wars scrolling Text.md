### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
#scrollingText {
    width: 100%;
    height: 100%;
    font-weight: 700;
    color: #ff6;
    overflow: hidden;
}
p#start {
    position: relative;
    width: 16em;
    font-size: 200%;
    font-weight: 400;
    margin: 20% auto;
    color: #4ee;
    opacity: 0;
    z-index: 1;
    -webkit-animation: intro 2s ease-out;
    -moz-animation: intro 2s ease-out;
    -ms-animation: intro 2s ease-out;
    -o-animation: intro 2s ease-out;
    animation: intro 2s ease-out;
}
#titles {
    position: absolute;
    width: 18em;
    height: 50em;
    bottom: 0;
    left: 50%;
    margin-left: -9em;
    font-size: 350%;
    text-align: justify;
    overflow: hidden;
    -webkit-transform-origin: 50% 100%;
    -moz-transform-origin: 50% 100%;
    -ms-transform-origin: 50% 100%;
    -o-transform-origin: 50% 100%;
    transform-origin: 50% 100%;
    -webkit-transform: perspective(300px) rotateX(25deg);
    -moz-transform: perspective(300px) rotateX(25deg);
    -ms-transform: perspective(300px) rotateX(25deg);
    -o-transform: perspective(300px) rotateX(25deg);
    transform: perspective(300px) rotateX(25deg);
}
#titles:after {
    position: absolute;
    content: ' ';
    left: 0;
    right: 0;
    top: 0;
    bottom: 60%;
    background-image: -webkit-linear-gradient(top, rgba(0,0,0,1) 0%, transparent 100%);
    background-image: -moz-linear-gradient(top, rgba(0,0,0,1) 0%, transparent 100%);
    background-image: -ms-linear-gradient(top, rgba(0,0,0,1) 0%, transparent 100%);
    background-image: -o-linear-gradient(top, rgba(0,0,0,1) 0%, transparent 100%);
    background-image: linear-gradient(top, rgba(0,0,0,1) 0%, transparent 100%);
    pointer-events: none;
}
#titles p {
    text-align: justify;
    margin: 0.8em 0;
}
#titles .center {
    text-align: center;
}

#titlecontent {
    position: absolute;
    top: 100%;
    -webkit-animation: scroll 100s linear 4s infinite;
    -moz-animation: scroll 100s linear 4s infinite;
    -ms-animation: scroll 100s linear 4s infinite;
    -o-animation: scroll 100s linear 4s infinite;
    animation: scroll 100s linear 4s infinite;
}
@-webkit-keyframes intro {
    0% { opacity: 1; }
    90% { opacity: 1; }
    100% { opacity: 0; }
}
@-moz-keyframes intro {
    0% { opacity: 1; }
    90% { opacity: 1; }
    100% { opacity: 0; }
}
@-ms-keyframes intro {
    0% { opacity: 1; }
    90% { opacity: 1; }
    100% { opacity: 0; }
}
@-o-keyframes intro {
    0% { opacity: 1; }
    90% { opacity: 1; }
    100% { opacity: 0; }
}
@keyframes intro {
    0% { opacity: 1; }
    90% { opacity: 1; }
    100% { opacity: 0; }
}
@-webkit-keyframes scroll {
    0% { top: 100%; }
    100% { top: -170%; }
}
@-moz-keyframes scroll {
    0% { top: 100%; }
    100% { top: -170%; }
}
@-ms-keyframes scroll {
    0% { top: 100%; }
    100% { top: -170%; }
}
@-o-keyframes scroll {
    0% { top: 100%; }
    100% { top: -170%; }
}
@keyframes scroll {
    0% { top: 100%; }
    100% { top: -170%; }
}
</style>
<div id="scrollingText">
  <div id="titles">
    <div id="titlecontent">

    <h1 class="center">EPISODE I</h1><br />
    <h2 class="center">Eine neue Hoffnung</h2>

    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut arcu mi, interdum eu feugiat vitae, tempus a justo. Morbi gravida nisi massa, nec dapibus urna interdum at. Phasellus fringilla ut lectus dapibus tincidunt. Nunc quis urna et dui ornare ultrices non sit amet lectus. Nulla mollis eleifend lectus in tincidunt.</p>

    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut arcu mi, interdum eu feugiat vitae, tempus a justo. Morbi gravida nisi massa, nec dapibus urna interdum at. Phasellus fringilla ut lectus dapibus tincidunt. Nunc quis urna et dui ornare ultrices non sit amet lectus. Nulla mollis eleifend lectus in tincidunt.</p>

    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut arcu mi, interdum eu feugiat vitae, tempus a justo. Morbi gravida nisi massa, nec dapibus urna interdum at. Phasellus fringilla ut lectus dapibus tincidunt. Nunc quis urna et dui ornare ultrices non sit amet lectus. Nulla mollis eleifend lectus in tincidunt.</p>

    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut arcu mi, interdum eu feugiat vitae, tempus a justo. Morbi gravida nisi massa, nec dapibus urna interdum at. Phasellus fringilla ut lectus dapibus tincidunt. Nunc quis urna et dui ornare ultrices non sit amet lectus. Nulla mollis eleifend lectus in tincidunt.</p>

    </div>
  </div>
</div>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
