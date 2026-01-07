
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.boxContainerWrapper {
  margin: 0;
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  padding: 2rem;
  align-items: center;
  justify-content: center;    
}
.boxContainerItem {
  --bgc: hsl(0 0% 100%);
  width: 10rem;
  aspect-ratio: 1/1;
  border: 1.5rem solid #0000;
  background:
    linear-gradient(120deg,
      color-mix(in oklab, var(--bgc), hsl(0 0% 0%) 10%) calc(50% - 1px),
      var(--bgc) calc(50% + 1px)
    ) border-box;
  position: relative;
  isolation: isolate;
  &::before{
    content: "";
    inset: 0;
    position: absolute;
    z-index: -1;
    border-radius: 2px;
    background-color: hsl(0 0% 100% / .25);
    backdrop-filter: blur(4px);
    box-shadow: 
      inset 1px 1px hsl(0 0 100% / .25),
      inset -1px -1px hsl(0 0 0% / .25),
      10px 10px 10px hsl( 0 0 0% / .25)
  }
}
</style>
<div class="boxContainerWrapper">
<div class="boxContainerItem" style="--bgc: #fdeb4c"></div>
<div class="boxContainerItem" style="--bgc: #fcc12c"></div>
<div class="boxContainerItem" style="--bgc: #fb562f"></div>
<div class="boxContainerItem" style="--bgc: #f13f3d"></div>
<div class="boxContainerItem" style="--bgc: #884ab9"></div>
<div class="boxContainerItem" style="--bgc: #b53bb4"></div>
<div class="boxContainerItem" style="--bgc: #e82a8f"></div>
<div class="boxContainerItem" style="--bgc: #f91876"></div>
<div class="boxContainerItem" style="--bgc: #5261be"></div>
<div class="boxContainerItem" style="--bgc: #4078d3"></div>
<div class="boxContainerItem" style="--bgc: #54a4ea"></div>
<div class="boxContainerItem" style="--bgc: #29c8d9"></div>
<div class="boxContainerItem" style="--bgc: #b0d459"></div>
<div class="boxContainerItem" style="--bgc: #93cf55"></div>
<div class="boxContainerItem" style="--bgc: #45b567"></div>
<div class="boxContainerItem" style="--bgc: #24c0b6"></div>
</div>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
