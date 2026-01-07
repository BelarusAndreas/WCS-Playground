
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
:root {
    --hue: 223;
    --bg: hsl(var(--hue),10%,90%);
    --fg: hsl(var(--hue),10%,10%);
    --primary: hsl(var(--hue),90%,50%);
    --trans-dur: 0.3s;
    --trans-timing: cubic-bezier(0.65,0,0.35,1);
    font-size: calc(16px + (24 - 16) * (100vw - 320px) / (2560 - 320));
}
a {
    color: var(--primary);
    transition: color var(--trans-dur);
}
.timeline {
    margin: auto;
    padding: 0 1.5em;
    width: 100%;
    max-width: 36em;
}
.timeline__arrow {
    background-color: transparent;
    border-radius: 0.25em;
    cursor: pointer;
    color: white;
    flex-shrink: 0;
    margin-inline-end: 0.25em;
    outline: transparent;
    width: 2em;
    height: 2em;
    transition:
        background-color calc(var(--trans-dur) / 2) linear,
        color var(--trans-dur);
    -webkit-appearance: none;
    appearance: none;
    -webkit-tap-highlight-color: transparent;
}
.timeline__arrow:focus-visible,
.timeline__arrow:hover {
    background-color: hsl(var(--hue),10%,50%,0.4);
}
.timeline__arrow-icon {
    display: block;
    pointer-events: none;
    transform: rotate(-90deg);
    transition: transform var(--trans-dur) var(--trans-timing);
    width: 100%;
    height: auto;
}
.timeline__date {
    font-size: 0.833em;
    line-height: 2.4;
}
.timeline__dot {
    background-color: currentColor;
    border-radius: 50%;
    display: inline-block;
    flex-shrink: 0;
    margin: 0.625em 0;
    margin-inline-end: 1em;
    position: relative;
    width: 0.75em;
    height: 0.75em;
}
.timeline__item {
    position: relative;
    padding-bottom: 2.25em;
}
.timeline__item:not(:last-child):before {
    background-color: currentColor;
    content: "";
    display: block;
    position: absolute;
    top: 1em;
    left: 3.25em;
    width: 0.125em;
    height: 100%;
    transform: translateX(-50%);
}
[dir="rtl"] .timeline__arrow-icon {
    transform: rotate(90deg);
}
[dir="rtl"] .timeline__item:not(:last-child):before {
    right: 2.625em;
    left: auto;
    transform: translateX(50%);
}
.timeline__item-header {
    display: flex;
}
.timeline__item-body {
    border-radius: 0.375em;
    overflow: hidden;
    margin-top: 0.5em;
    margin-inline-start: 4em;
    height: 0;
}
.timeline__item-body-content {
    background-color: hsl(var(--hue),10%,50%,0.2);
    opacity: 0;
    padding: 0.5em 0.75em;
    visibility: hidden;
    transition:
        opacity var(--trans-dur) var(--trans-timing),
        visibility var(--trans-dur) steps(1,end);
}
.timeline__meta {
    width: 100%;
}
.timeline__title {
    font-size: 1.5em;
    line-height: 1.333;
}
.timeline__item-body--expanded {
    height: auto;
}
.timeline__item-body--expanded .timeline__item-body-content {
    opacity: 1;
    visibility: visible;
    transition-delay: var(--trans-dur), 0s;
}
.timeline__arrow[aria-expanded="true"] .timeline__arrow-icon {
    transform: rotate(0);
}    
</style>


<svg display="none">
    <symbol id="arrow">
        <polyline points="7 10,12 15,17 10" fill="none" stroke="currentcolor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" />
    </symbol>
</svg>

<div id="timeline" class="timeline">
    <div class="btn-group">
        <button class="btn" type="button" data-action="expand">Alle anzeigen</button>
        <button class="btn" type="button" data-action="collapse">Alle ausblenden</button>
    </div>
    
    <!-- Timeline Item 1 -->
    <div class="timeline__item">
        <div class="timeline__item-header">
            <button class="timeline__arrow" type="button" id="item1" aria-labelledby="item1-name" aria-expanded="false" aria-controls="item1-ctrld" aria-haspopup="true" data-item="1">
                <i class="fa fa-angle-down timeline__arrow-icon" aria-hidden="true"  width="24px" height="24px"><use href="#arrow" /></i>
            </button>
            <span class="timeline__dot"></span>
            <span id="item1-name" class="timeline__meta">
                <time class="timeline__date" datetime="2000-01-01">1. Januar 2000</time><br>
                <strong class="timeline__title">Titel 1</strong>
            </span>
        </div>
        <div class="timeline__item-body" id="item1-ctrld" role="region" aria-labelledby="item1" aria-hidden="true">
            <div class="timeline__item-body-content">
                <p class="timeline__item-p">Eine Beschreibung zum 1. Eintrag.</p>
            </div>
        </div>
    </div>
    
    <!-- Timeline Item 2 -->
    <div class="timeline__item">
        <div class="timeline__item-header">
            <button class="timeline__arrow" type="button" id="item2" aria-labelledby="item2-name" aria-expanded="false" aria-controls="item2-ctrld" aria-haspopup="true" data-item="2">
                <i class="fa fa-angle-down timeline__arrow-icon" aria-hidden="true"  width="24px" height="24px"><use href="#arrow" /></i>
            </button>
            <span class="timeline__dot"></span>
            <span id="item2-name" class="timeline__meta">
                <time class="timeline__date" datetime="2000-12-31">31.12.2000</time><br>
                <strong class="timeline__title">Titel 2</strong>
            </span>
        </div>
        <div class="timeline__item-body" id="item2-ctrld" role="region" aria-labelledby="item2" aria-hidden="true">
            <div class="timeline__item-body-content">
                <p class="timeline__item-p">Eine Beschreibung zum 2. Eintrag.</p>
            </div>
        </div>
    </div>
    
    <!-- Timeline Item 3 -->
    <div class="timeline__item">
        <div class="timeline__item-header">
            <button class="timeline__arrow" type="button" id="item3" aria-labelledby="item3-name" aria-expanded="false" aria-controls="item3-ctrld" aria-haspopup="true" data-item="3">
                <i class="fa fa-angle-down timeline__arrow-icon" aria-hidden="true"  width="24px" height="24px"><use href="#arrow" /></i>
            </button>
            <span class="timeline__dot"></span>
            <span id="item3-name" class="timeline__meta">
                <time class="timeline__date" datetime="2001-03-15">15. März 2001</time><br>
                <strong class="timeline__title">Titel 3</strong>
            </span>
        </div>
        <div class="timeline__item-body" id="item3-ctrld" role="region" aria-labelledby="item3" aria-hidden="true">
            <div class="timeline__item-body-content">
                <p class="timeline__item-p">Eine Beschreibung zum 3. Eintrag.</p>
            </div>
        </div>
    </div>
    
</div>

<script>
window.addEventListener("DOMContentLoaded",() => {
    const ctl = new CollapsibleTimeline("#timeline");
});
class CollapsibleTimeline {
    constructor(el) {
        this.el = document.querySelector(el);
        this.init();
    }
    init() {
        this.el?.addEventListener("click",this.itemAction.bind(this));
    }
    animateItemAction(button,ctrld,contentHeight,shouldCollapse) {
        const expandedClass = "timeline__item-body--expanded";
        const animOptions = {
            duration: 300,
            easing: "cubic-bezier(0.65,0,0.35,1)"
        };
        if (shouldCollapse) {
            button.ariaExpanded = "false";
            ctrld.ariaHidden = "true";
            ctrld.classList.remove(expandedClass);
            animOptions.duration *= 2;
            this.animation = ctrld.animate([
                { height: `${contentHeight}px` },
                { height: `${contentHeight}px` },
                { height: "0px" }
            ],animOptions);
        } else {
            button.ariaExpanded = "true";
            ctrld.ariaHidden = "false";
            ctrld.classList.add(expandedClass);
            this.animation = ctrld.animate([
                { height: "0px" },
                { height: `${contentHeight}px` }
            ],animOptions);
        }
    }
    itemAction(e) {
        const { target } = e;
        const action = target?.getAttribute("data-action");
        const item = target?.getAttribute("data-item");
        if (action) {
            const targetExpanded = action === "expand" ? "false" : "true";
            const buttons = Array.from(this.el?.querySelectorAll(`[aria-expanded="${targetExpanded}"]`));
            const wasExpanded = action === "collapse";
            for (let button of buttons) {
                const buttonID = button.getAttribute("data-item");
                const ctrld = this.el?.querySelector(`#item${buttonID}-ctrld`);
                const contentHeight = ctrld.firstElementChild?.offsetHeight;
                this.animateItemAction(button,ctrld,contentHeight,wasExpanded);
            }
        } else if (item) {
            const button = this.el?.querySelector(`[data-item="${item}"]`);
            const expanded = button?.getAttribute("aria-expanded");
            if (!expanded) return;
            const wasExpanded = expanded === "true";
            const ctrld = this.el?.querySelector(`#item${item}-ctrld`);
            const contentHeight = ctrld.firstElementChild?.offsetHeight;
            this.animateItemAction(button,ctrld,contentHeight,wasExpanded);
        }
    }
}
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
