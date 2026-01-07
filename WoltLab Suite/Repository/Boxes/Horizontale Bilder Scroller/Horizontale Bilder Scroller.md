### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
:root {
  --color-fg: #325c84;
  --color-bg: #000;
}
.scroll-x {
  max-width: 100%;
  overflow-x: auto;
  overscroll-behavior-x: contain;
  scrollbar-color: var(--color-fg) var(--color-bg);
}
.wrapper {
  --size: clamp(12rem, 1rem + 50vw, 20rem);
  --gutter: 2rem;
  --gap: 0.5rem;
  scroll-snap-type: x mandatory;
  display: grid;
  padding-block: var(--gutter);
  grid-template-columns:
    [full-start] 1fr
    [content-start]
    min(var(--size), 100% - var(--gutter) * 2)
    [content-end]
    1fr [full-end];
}
.items {
  grid-area: content;
  display: flex;
  gap: var(--gap);
  &::after {
    content: "";
    padding-inline-end: max(
      var(--gutter),
      (100vw - var(--size)) / 2 - var(--gutter)
    );
  }
  > * {
    display: grid;
    place-content: center;
    flex-shrink: 0;
    inline-size: var(--size);
    aspect-ratio: 5 / 5;
    scroll-snap-align: center;
    font-size: 2rem;
    font-weight: 600;
    color: white;
    border-radius: 0.5rem;
  }
}
@supports (animation-timeline: view()) {
  .items > * {
    --scale: 0.8;
    --offset: var(--gap);
    animation: scale linear both, fade linear both;
    animation-timeline: view(inline);
    animation-range: cover 30% cover 70%, cover 5% cover 95%;
  }
  @keyframes scale {
    from,
    to { scale: var(--scale); }
    50% { scale: 1; }
    from { translate: var(--offset) 0; }
    to { translate: calc(var(--offset) * -1) 0; }
  }
  @keyframes fade {
    from,
    to { opacity: 0; }
    10%,
    90% { opacity: 1; }
  }
}
.item-image {
  width: 100%;
  height: 100%;
}
</style>

<div class="wrapper scroll-x">
  <ul class="items">
    <li>
      <img src="URL_ZUM_BILD" class="item-image">
    </li>
    <li>
      <img src="URL_ZUM_BILD" class="item-image"> 
    </li>
    <li>
      <img src="URL_ZUM_BILD" class="item-image"> 
    </li>
    <li>
      <img src="URL_ZUM_BILD" class="item-image"> 
    </li>
    <li>
      <img src="URL_ZUM_BILD" class="item-image"> 
    </li>
    <li>
      <img src="URL_ZUM_BILD" class="item-image"> 
    </li>
    <li>
      <img src="URL_ZUM_BILD" class="item-image"> 
    </li>
    <li>
      <img src="URL_ZUM_BILD" class="item-image"> 
    </li>
    <li>
      <img src="URL_ZUM_BILD" class="item-image"> 
    </li>
    <li>
      <img src="URL_ZUM_BILD" class="item-image"> 
    </li>
  </ul>
</div>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.

