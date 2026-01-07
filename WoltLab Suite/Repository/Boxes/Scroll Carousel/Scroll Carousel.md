### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
$slide-size: 15%;
$slide-color: #B63533;
$reflection-color: darken($slide-color,65);
$text-color: #fff;
$background-color: #273448;

.scrollsnap-carousel {
    overflow-x:auto;
    overflow-y:hidden;
    width:100%;
    height:100%;
    max-width:100%;
    scroll-snap-type: x mandatory;
    white-space:nowrap;
    padding:100px 0 0 0;
    .slide {
        display:inline-block;
        height:$slide-size;
        width:$slide-size;
        flex:0 0 $slide-size;
        scroll-snap-align: center;
        view-timeline-name: --li-in-and-out-of-view;
        view-timeline-axis: inline;
        animation: linear move-to-top both;
        animation-timeline: --li-in-and-out-of-view;
        perspective: 40em;
        position:relative;
        color:$text-color;
        transform-origin:bottom;
        &:first-of-type {
            margin-left:50%;
        }
        &:last-of-type {
            margin-right:50%;
        }
        .content {
            border-radius:10px;
            width:100%;
            padding-bottom:100%;
            background:$slide-color;
            animation: linear rotateSlide both;
            animation-timeline: --li-in-and-out-of-view;
            position:relative;
            .content-wrapper {
                position:absolute;
                width:100%;
                height:100%;
                display:flex;
                align-items:center;
                justify-content:center;
                animation: linear fadeContent both;
                animation-timeline: --li-in-and-out-of-view;
                &:after {
                    content:'';
                    display:block;
                    width:100%;
                    height:50%;
                    position:absolute;
                    background: linear-gradient($reflection-color, $background-color);
                    top:100%;
                    left:0;
                    border-radius:10px 10px 0 0;
                }
            }
        }
    }
}

@keyframes rotateSlide {
    0% {
        transform: translateX(-150%) rotateY(-45deg) translateZ(4em) scale(0.5);
        background:$background-color;
    }
    50% {
        transform: rotateY(0deg) translateZ(1em) scale(1.25);
        background:$slide-color;
    }
    100% {
        transform: translateX(150%) rotateY(45deg) translateZ(4em) scale(0.65);
        background:$background-color;
    }
}
@keyframes fadeContent {
    0% { opacity:0; }
    50% { opacity:1; }
    100% { opacity:0; }
}
@keyframes move-to-top {
    0% { z-index: 1; }
    50% { z-index: 100; }
    100% { z-index: 1; }
}
</style>

<div class="scrollsnap-carousel">
    <div class="slide">
        <div class="content">
            <div class="content-wrapper">
                Slide 1
            </div>
        </div>
    </div>
    <div class="slide">
        <div class="content">
            <div class="content-wrapper">
                Slide 2
            </div>
        </div>
    </div>
    <div class="slide">
        <div class="content">
            <div class="content-wrapper">
                Slide 3
            </div>
        </div>
    </div>
    <div class="slide">
        <div class="content">
            <div class="content-wrapper">
                Slide 4
            </div>
        </div>
    </div>
    <div class="slide">
        <div class="content">
            <div class="content-wrapper">
                Slide 5
            </div>
        </div>
    </div>
    <div class="slide">
        <div class="content">
            <div class="content-wrapper">
                Slide 6
            </div>
        </div>
    </div>
    <div class="slide">
        <div class="content">
            <div class="content-wrapper">
                Slide 7
            </div>
        </div>
    </div>
    <div class="slide">
        <div class="content">
            <div class="content-wrapper">
                Slide 8
            </div>
        </div>
    </div>
</div>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

