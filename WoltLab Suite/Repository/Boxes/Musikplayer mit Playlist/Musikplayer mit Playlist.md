
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
/* Ersetze XXX mit der Box-ID deiner angelegten Box */
[data-box-identifier="com.woltlab.wcf.genericBoxXXX"] .boxContent {    
padding: 10px
}
.img {
width: 100% ;
flex-shrink: 0;
display: block ;
object-fit: cover ;
}
.list {
margin: 0 ;
padding: 0 ;
list-style-type: none ;
}
.flex {
display: flex ;
align-items: center ;
justify-content: space-between ;
}
.uppercase{
text-transform: uppercase ;
}
.player {
width: 17.15em ;
display: flex ;
overflow: hidden ;
font-size: 1.22em ;
color: white;
flex-direction: column ;
background-color: transparent !important;
height: var(--parent-height) ;
}
.player__header {
z-index: 1 ;
gap: 0 .4em ;
width: 100% ;
display: flex;
height: 5.85em ;
flex-shrink: 0 ;
position: relative;
align-items: flex-start ;
border-radius: inherit ;
justify-content: flex-end ;
background-color: transparent !important;
padding: .95em 0.6em 0 1.2em ;
transition: height var(--cubic-header), box-shadow var(--duration), padding var(--duration) ease-in-out ;
}
.player__header.open-header {
height: 100% ;
padding-left: 0 ;
padding-right: 0 ;
box-shadow: unset ;
}
.player__img {
width: 3.22em ;
height: 3.22em ;
border-radius: 1.32em ;
}
.player__img--absolute {
top: 1.4em ;
left: 1.2em ;
position: absolute ;
}
.slider {
flex-shrink: 0 ;
overflow: hidden ;
transition: width var(--cubic-header), height var(--cubic-header), top var(--cubic-header), left var(--cubic-header);
}
.slider.open-slider{
top: 0 ;
left: 0 ;
width: 100% ;
height: 14.6em ;
}
.slider__content {
display: flex ;
height: 100% ;
will-change : transform ;
transition: transform var(--cubic-slider);
}
.slider__img {
filter: brightness(75%) ;
}
.slider__name,
.slider__title {
overflow: hidden ;
white-space: nowrap ;
}
.text-wrap {
display: block ;
white-space: pre ;
width: fit-content ;
animation: text-wrap var(--duration-text-wrap) infinite ;
}
@keyframes text-wrap {
75%{
transform: translate3d(-51.5%, 0, 0) ;
}
100%{
transform: translate3d(-51.5%, 0, 0) ;
}
}
.player__button {
all: unset ;
z-index: 100 ;
width: 2.5em ;
height: 2.5em ;
cursor: pointer ;
}
.playlist {
transform: scale(0) ;
transition: transform calc(var(--duration) / 2) ;
}
.slider.open-slider .playlist {
transform: scale(1) ;
transition: transform var(--cubic-play-list) ;
}
.player__button--absolute--nw {
top: 5.5% ;
left: 5.5% ;
position: absolute ;
}
.player__button--absolute--center {
top: 0 ;
left: 0 ;
right: 0 ;
bottom: 0 ;
margin: auto ;
position: absolute ;
}
img[alt ="pause-icon"] {
display: none ;
}
.player__controls {
width: 77% ;
gap: .5em 0 ;
display: flex ;
flex-wrap: wrap ;
align-items: center ;
will-change: contents ;
align-content: center ;
justify-content: center ;
transition: transform var(--cubic-header) , width var(--cubic-header) ;
}
.player__controls.move {
width: 88% ;
transform: translate3d(-1.1em , calc(var(--parent-height) - 153%) , 0) ;
}
.player__context {
margin: 0 ;
width: 100% ;
display: flex ;
line-height: 1.8 ;
flex-direction: column ;
justify-content: center ;
text-transform: capitalize ;
}
.slider__context {
width: 56.28% ;
cursor: pointer ;
text-align: center ;
padding-bottom: .2em ;
will-change: contents ;
transition: width var(--cubic-header) ;
animation: calc(var(--duration) / 2) var(--cubic-slider-context) ;
}
@keyframes opacity {
0% {
opacity: 0 ;
}
90%{
opacity: 1 ;
}
}
.player__controls.move .slider__context{
width: 49.48% ;
}
.player__title {
font-size: .7em ;
font-weight: bold ;
color: white ;
}
.progres {
width: 90% ;
height: .25em ;
cursor: pointer ;
border-radius: 1em ;
touch-action : none ;
background-color: #e5e7ea ;
transition: width var(--cubic-header) ;
}
.player__controls.move .progres{
width: 98% ;
}
.progres__filled {
width: 0% ;
height: 100% ;
display: flex ;
position: relative ;
align-items: center ;
border-radius: inherit ;
background-color: #78adfe ;
}
.progres__filled::before {
right: 0 ;
width: .35em ;
content: " " ;
height: .35em ;
border-radius: 50% ;
position: absolute ;
background-color: #5781bd ;
}
.player__playlist {
height: 100% ;
overflow: auto ;
padding: 1.05em .9em 0 1.2em ;
}
.player__playlist::-webkit-scrollbar {
width: 0 ;
}
.player__song {
display: flex ;
cursor: pointer ;
margin-bottom: .5em ;
padding-bottom: .7em ;
border-bottom: .1em solid #d8d8d859 ;
}
.player__song .player__context {
line-height: 1.5 ;
margin-left: .65em ;
}
.player__song-name {
font-size: .88em ;
}
.player__song-time {
font-size: .65em ;
font-weight: bold ;
color: white ;
height: fit-content ;
align-self: flex-end ;
}
.audio {
display: none !important ;
}
</style>

<div class="player">
  <div class="player__header">
    <div class="player__img player__img--absolute slider">
      <button class="player__button player__button--absolute--nw playlist">
        <img src="http://physical-authority.surge.sh/imgs/icon/playlist.svg" alt="playlist-icon">
      </button>
      <button class="player__button player__button--absolute--center play">
        <img src="http://physical-authority.surge.sh/imgs/icon/play.svg" alt="play-icon">
        <img src="http://physical-authority.surge.sh/imgs/icon/pause.svg" alt="pause-icon">
      </button>
      <div class="slider__content">
        <img class="img slider__img" src="http://physical-authority.surge.sh/imgs/1.jpg" alt="cover">
        <img class="img slider__img" src="http://physical-authority.surge.sh/imgs/2.jpg" alt="cover">
        <img class="img slider__img" src="http://physical-authority.surge.sh/imgs/3.jpg" alt="cover">
        <img class="img slider__img" src="http://physical-authority.surge.sh/imgs/4.jpg" alt="cover">
        <img class="img slider__img" src="http://physical-authority.surge.sh/imgs/5.jpg" alt="cover">
        <img class="img slider__img" src="http://physical-authority.surge.sh/imgs/6.jpg" alt="cover">
        <img class="img slider__img" src="http://physical-authority.surge.sh/imgs/7.jpg" alt="cover">
      </div>
    </div>
    <div class="player__controls">
      <button class="player__button back">
        <img class="img" src="http://physical-authority.surge.sh/imgs/icon/back.svg" alt="back-icon">
      </button>
      <p class="player__context slider__context">
        <strong class="slider__name"></strong>
        <span class="player__title slider__title"></span>
      </p>
      <button class="player__button next">
        <img class="img" src="http://physical-authority.surge.sh/imgs/icon/next.svg" alt="next-icon">
      </button>
      <div class="progres">
        <div class="progres__filled"></div>
      </div>
    </div>
  </div>
  <ul class="player__playlist list">
      
  <!-- Track 1 -->
  <li class="player__song">
    <img class="player__img img" src="http://physical-authority.surge.sh/imgs/1.jpg" alt="cover">
    <p class="player__context">
      <b class="player__song-name">no time</b>
      <span class="flex">
        <span class="player__title">lastlings</span>
        <span class="player__song-time"></span>
      </span>
    </p>
    <audio class="audio" src="http://physical-authority.surge.sh/music/1.mp3"></audio>
  </li>
      
  <!-- Track 2 -->      
  <li class="player__song">
    <img class="player__img img" src="http://physical-authority.surge.sh/imgs/2.jpg" alt="cover">
    <p class="player__context">
      <b class="player__song-name">blinding lights</b>
      <span class="flex">
        <span class="player__title">the weeknd</span>
        <span class="player__song-time"></span>
      </span>
    </p>
    <audio class="audio" src="http://physical-authority.surge.sh/music/2.mp3"></audio>
  </li>
    
  <!-- Track 3 -->      
  <li class="player__song">
    <img class="player__img img" src="http://physical-authority.surge.sh/imgs/3.jpg" alt="cover">
    <p class="player__context">
      <b class="player__song-name">джованна</b>
      <span class="flex">
        <span class="player__title">enrasta</span>
        <span class="player__song-time"></span>
      </span>
    </p>
    <audio class="audio" src="http://physical-authority.surge.sh/music/3.mp3"></audio>
  </li>

  <!-- Track 4 -->
  <li class="player__song">
    <img class="player__img img" src="http://physical-authority.surge.sh/imgs/4.jpg" alt="cover">
    <p class="player__context">
      <b class="player__song-name">a man</b>
      <span class="flex">
        <span class="player__title">travis scott</span>
        <span class="player__song-time"></span>
      </span>
    </p>
    <audio class="audio" src="http://physical-authority.surge.sh/music/4.mp3"></audio>
  </li>Fertig!
      
  <!-- Track 4 -->       
  <li class="player__song">
    <img class="player__img img" src="http://physical-authority.surge.sh/imgs/5.jpg" alt="cover">
    <p class="player__context ">
      <b class="player__song-name">unforgetting</b>
      <span class="flex">
        <span class="player__title">zaxx</span>
        <span class="player__song-time"></span>
      </span>
    </p>
    <audio class="audio" src="http://physical-authority.surge.sh/music/5.mp3"></audio>
  </li>
      
  <!-- Track 5 -->
  <li class="player__song">
    <img class="player__img img" src="http://physical-authority.surge.sh/imgs/6.jpg" alt="cover">
    <p class="player__context">
      <b class="player__song-name">waharan</b>
      <span class="flex">
        <span class="player__title">Randall</span>
        <span class="player__song-time"></span>
      </span>
    </p>
    <audio class="audio" src="http://physical-authority.surge.sh/music/6.mp3"></audio>
  </li>

  <!-- Track 6 -->
  <li class="player__song">
    <img class="player__img img" src="http://physical-authority.surge.sh/imgs/7.jpg" alt="cover">
    <p class="player__context ">
      <b class="player__song-name">starlight feat mr gabriel <span class="uppercase">4am</span> remix</b>
      <span class="flex">
        <span class="player__title">jai wolf</span>
        <span class="player__song-time"></span>
      </span>
    </p>
    <audio class="audio" src="http://physical-authority.surge.sh/music/7.mp3"></audio>
  </li>
  </ul>
</div>

<script>
"use strict";
const bgBody = ["#0000ffcc"]; 
const body = document.body;
const player = document.querySelector(".player");
const playerHeader = player.querySelector(".player__header");
const playerControls = player.querySelector(".player__controls");
const playerPlayList = player.querySelectorAll(".player__song");
const playerSongs = player.querySelectorAll(".audio");
const playButton = player.querySelector(".play");
const nextButton = player.querySelector(".next");
const backButton = player.querySelector(".back");
const playlistButton = player.querySelector(".playlist");
const slider = player.querySelector(".slider");
const sliderContext = player.querySelector(".slider__context");
const sliderName = sliderContext.querySelector(".slider__name");
const sliderTitle = sliderContext.querySelector(".slider__title");
const sliderContent = slider.querySelector(".slider__content");
const sliderContentLength = playerPlayList.length - 1;
const sliderWidth = 100;
let left = 0;
let count = 0;
let song = playerSongs[count];
let isPlay = false;
const pauseIcon = playButton.querySelector("img[alt = 'pause-icon']");
const playIcon = playButton.querySelector("img[alt = 'play-icon']");
const progres = player.querySelector(".progres");
const progresFilled = progres.querySelector(".progres__filled");
let isMove = false;
function openPlayer() {
playerHeader.classList.add("open-header");
playerControls.classList.add("move");
slider.classList.add("open-slider");
}
function closePlayer() {
playerHeader.classList.remove("open-header");
playerControls.classList.remove("move");
slider.classList.remove("open-slider");
}
function next(index) {
count = index || count;
if (count == sliderContentLength) {
count = count;
return;
}
left = (count + 1) * sliderWidth;
left = Math.min(left, (sliderContentLength) * sliderWidth);
sliderContent.style.transform = `translate3d(-${left}%, 0, 0)`;
count++;
run();
}
function back(index) {
count = index || count;
if (count == 0) {
count = count;
return;
}
left = (count - 1) * sliderWidth;
left = Math.max(0, left);
sliderContent.style.transform = `translate3d(-${left}%, 0, 0)`;
count--;
run();
}
function changeSliderContext() {
sliderContext.style.animationName = "opacity";
sliderName.textContent = playerPlayList[count].querySelector(".player__title").textContent;
sliderTitle.textContent = playerPlayList[count].querySelector(".player__song-name").textContent;
if (sliderName.textContent.length > 16) {
const textWrap = document.createElement("span");
textWrap.className = "text-wrap";
textWrap.innerHTML = sliderName.textContent + " " + sliderName.textContent;
sliderName.innerHTML = "";
sliderName.append(textWrap);
}
if (sliderTitle.textContent.length >= 18) {
const textWrap = document.createElement("span");
textWrap.className = "text-wrap";
textWrap.innerHTML = sliderTitle.textContent + " " + sliderTitle.textContent;
sliderTitle.innerHTML = "";
sliderTitle.append(textWrap);
}
}
function changeBgBody() {
body.style.backgroundColor = bgBody[count];
}
function selectSong() {
song = playerSongs[count];
for (const item of playerSongs) {
if (item != song) {
item.pause();
item.currentTime = 0;
}
}
if (isPlay) song.play();
}
function run() {
changeSliderContext();
changeBgBody();
selectSong();
}
function playSong() {
if (song.paused) {
song.play();
playIcon.style.display = "none";
pauseIcon.style.display = "block";
}else{
song.pause();
isPlay = false;
playIcon.style.display = "";
pauseIcon.style.display = "";
}
}
function progresUpdate() {
const progresFilledWidth = (this.currentTime / this.duration) * 100 + "%";
progresFilled.style.width = progresFilledWidth;
if (isPlay && this.duration == this.currentTime) {
next();
}
if (count == sliderContentLength && song.currentTime == song.duration) {
playIcon.style.display = "block";
pauseIcon.style.display = "";
isPlay = false;
}
}
function scurb(e) {
const currentTime = ( (e.clientX - progres.getBoundingClientRect().left) / progres.offsetWidth ) * song.duration;
song.currentTime = currentTime;
}
function durationSongs() {
let min = parseInt(this.duration / 60);
if (min < 10) min = "0" + min;
let sec = parseInt(this.duration % 60);
if (sec < 10) sec = "0" + sec;
const playerSongTime = `${min}:${sec}`;
this.closest(".player__song").querySelector(".player__song-time").append(playerSongTime);
}
changeSliderContext();
sliderContext.addEventListener("click", openPlayer);
sliderContext.addEventListener("animationend", () => sliderContext.style.animationName ='');
playlistButton.addEventListener("click", closePlayer);
nextButton.addEventListener("click", () => {
next(0)
});
backButton.addEventListener("click", () => {
back(0)
});
playButton.addEventListener("click", () => {
isPlay = true;
playSong();
});
playerSongs.forEach(song => {
song.addEventListener("loadeddata" , durationSongs);
song.addEventListener("timeupdate" , progresUpdate);
});
progres.addEventListener("pointerdown", (e) => {
scurb(e);
isMove = true;
});
document.addEventListener("pointermove", (e) => {
if (isMove) {
scurb(e);
song.muted = true;
}
});
document.addEventListener("pointerup", () => {
isMove = false;
song.muted = false;
});
playerPlayList.forEach((item, index) => {
item.addEventListener("click", function() {
if (index > count) {
next(index - 1);
return;
}
if (index < count) {
back(index + 1);
return;
}
});
});
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
