
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
Template
```
<li class="boxMenuHasChildren myNewMenuEntry">
  <a href="#">Shop</a>
  <ul id="mega-menu">
    <li class="active-menu-item">
      <ol class="boxMenuDepth1" style="height: 450px;">
        <div class="gridLayout row">
          <!-- 1. Block -->
          <div class="gridBox col-md-3">
            <h2 class="gridBoxTitle gridBoxContentCenter">Links</h2>
            <div class="gridBoxContent gridBoxContentCenter">
              <img src="https://via.placeholder.com/150">
              <p class="gridBoxMargin">Description</p>
              <div class="gridBoxPadding4">
                <a href="#" class="button">More</a>
              </div>
            </div>
          </div>
          <!-- 2. Block -->
          <div class="gridBox col-md-3">
            <h2 class="gridBoxTitle gridBoxContentCenter">Links</h2>
            <div class="gridBoxContent gridBoxContentCenter">
              <img src="https://via.placeholder.com/150">
              <p class="gridBoxMargin">Description</p>
              <div class="gridBoxPadding4">
                <a href="#" class="button">More</a>
              </div>
            </div>
          </div>
          <!-- 3. Block -->
          <div class="gridBox col-md-3">
            <h2 class="gridBoxTitle gridBoxContentCenter">Links</h2>
            <div class="gridBoxContent gridBoxContentCenter">
              <img src="https://via.placeholder.com/150">
              <p class="gridBoxMargin">Description</p>
              <div class="gridBoxPadding4">
                <a href="#" class="button">More</a>
              </div>
            </div>
          </div>
          <!-- 4. Block -->
          <div class="gridBox col-md-3">
            <h2 class="gridBoxTitle gridBoxContentCenter">Links</h2>
            <div class="gridBoxContent gridBoxContentCenter">
              <img src="https://via.placeholder.com/150">
              <p class="gridBoxMargin">Description</p>
              <div class="gridBoxPadding4">
                <a href="#" class="button">More</a>
              </div>
            </div>
          </div>
        </div>
      </ol>
    </li>
  </ul>
</li>
```
### Benutzung:
1.  Gehe zu  Anpassung  ➞  Templates
2.  Wähle unter Templates (falls dort nicht schon markiert) über den Filter Deinen Style aus.
3.  Lege mit einen klick auf  + Template hinzufügen  ein neues Template an.
4.  Wähle als Templatename: `MegaMenu`
5.  Füge dann den HTML-Quellcode (siehe oben) ein und speicher das Template ab.
6.  Passe anschließend ggfls, die CSS ID's bzw. Klassen nach Deinen Bedürfnissen an.  
    Beachte dazu auch die  height:-Angabe im Quelltext, welche entweder ersetzt, angepasst oder entfernt werden müsste.

Um das Template nun einzubinden und anzeigen zu lassen gehe wie folgt vor:

1.  Gehe zu  Anpassungen ➞  Templates  ➞  DEIN_STYLE  ➞  und suche das Template:  `__menu`
2.  Klicke hier auf  bearbeiten.
3.  Suche nun nach der Zeile  `{event name='menuAfter'}`  (relativ weit oben).
4.  Füge  **davor**  folgendes in einer neuen Zeile ein:  `{include file='MegaMenu'}`  und speicher dieses ab.
5.  Fertig!





