
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
#### Sidebar-Menü links ausgerichtet
```
<!-- Für die Woltlab Suite 3.x und 5.x -->
<style>
 @media screen and (min-width: 1025px) {
    .pageContainer {
        margin-left: 179px;
    }
    .pageHeaderPanel {
        background: transparent
    }
    .mainMenu {
        flex: 1;
        width: 179px;
        height: 100% !important;
        background: rgb(58 109 156);
        margin-top: 36px;
        position: fixed;
        left: 0;
    }
    .mainMenu .boxMenu {
        display: contents;
    }
    .mainMenu .boxMenu>li {
        display: contents;
        overflow: hidden;
        z-index: 999;
    }
    .boxMenuHasChildren fa-icon {
        position: absolute;
        right: 5px;
    }
    .boxMenuDepth1 {
        margin: -50px 0  0 179px;
    }
    .userPanel {
        position: absolute;
        left: 0;
    }
    .userPanel .userAvatarImage {
        width: 16px;
        height: 16px;
        margin-left: 10px;
    }
    .userPanel>ul>li>a {
        height: 36px;
        padding: 0 5px 0 0;
    }
    .userPanel .icon {
        font-size: 16px;
    }
    .searchBarOpen .pageHeaderSearch {
        margin-left: 179px;
    }
}
</style>

<!-- Für die Woltlab Suite 6.x -->
<style>
@media screen and (min-width: 1025px) {
    .pageContainer {
        margin-right: 200px;
    }
    .pageHeaderPanel {
        background: transparent
    }
    .mainMenu {
        flex: 1;
        width: 200px;
        height: 100% !important;
        background: rgb(58 109 156);
        position: fixed;
        right: 0;
    }
    .mainMenu .boxMenu {
        display: contents;
    }
    .mainMenu .boxMenu>li {
        display: contents;
        overflow: hidden;
        z-index: 999;
    }
    .mainMenu .boxMenu>li>a>span {
        position: absolute;
        right: 10px;
    }
    .mainMenu .boxMenu>li>a>.boxMenuLinkOutstandingItems {
        position: relative;
        left: 10px;
    }
    .boxMenuHasChildren fa-icon {
        position: absolute;
        left: 5px;
    }
    .boxMenuDepth1 {
        margin: -50px 0 0 -162px;
    }
    .userPanel {
        position: absolute;
        left: 0;
    }
    .mainMenu .boxMenu>.boxMenuHasChildren>a::after {
       content: "\f0d9";
       display: block;
       font-family: "FontAwesome";
   }
}
</style>
```
#### Sidebar-Menü rechts ausgerichtet
```
<!-- Für die Woltlab Suite 3.x und 5.x -->
<style>
@media screen and (min-width: 1025px) {
    .pageContainer {
        margin-right: 179px;
    }
    .pageHeaderPanel {
        background: transparent
    }
    .mainMenu {
        flex: 1;
        width: 179px;
        height: 100% !important;
        background: rgb(58 109 156);
        position: fixed;
        right: -20px;
    }
    .mainMenu .boxMenu {
        display: contents;
    }
    .mainMenu .boxMenu>li {
        display: contents;
        overflow: hidden;
        z-index: 999;
    }
    .mainMenu .boxMenu>li>a>span {
        position: absolute;
        right: 10px;
    }
    .mainMenu .boxMenu>li>a>.boxMenuLinkOutstandingItems {
        position: relative;
        left: 10px;
    }
    .boxMenuHasChildren fa-icon {
        position: absolute;
        left: 5px;
    }
    .boxMenuDepth1 {
        margin: -50px 0 0 -162px;
    }
    .userPanel {
        position: absolute;
        right: 0;
    }
    .userPanel .userAvatarImage {
        width: 16px;
        height: 16px;
        margin-left: 10px;
    }
    .userPanel>ul>li>a {
        height: 36px;
        padding: 0 5px 0 0;
    }
    .userPanel .icon {
        font-size: 16px;
    }
    .pageHeaderSearchInputContainer {
        position: fixed;
        right: 179px;
    }
}
</style>

<!-- Für die Woltlab Suite 6.x -->
<style>
@media screen and (min-width: 1025px) {
    .pageContainer {
        margin-right: 166px;
    }
    .pageHeaderPanel {
        background: transparent
    }
    .mainMenu {
        flex: 1;
        width: 166px;
        height: 100% !important;
        background: rgb(58 109 156);
        position: fixed;
        right: -20px;
        top: 36px
    }
    .mainMenu .boxMenu {
        display: contents;
    }
    .mainMenu .boxMenu>li {
        display: contents;
        overflow: hidden;
        z-index: 999;
    }
    .mainMenu .boxMenu>li>a>span {
        position: absolute;
        right: 10px;
    }
    .mainMenu .boxMenu>li>a>.boxMenuLinkOutstandingItems {
        position: relative;
        left: 10px;
    }
    .boxMenuHasChildren fa-icon {
        position: absolute;
        left: 5px;
    }
    .boxMenuDepth1 {
        margin: -50px 0 0 -182px;
    }
    .userPanel {
        position: absolute;
        right: 0;
    }
    .userPanel .userAvatarImage {
        width: 16px;
        height: 16px;
        margin-left: 10px;
    }
    .userPanel>ul>li>a {
        height: 36px;
        padding: 0 5px 0 0;
    }
    .userPanel>ul>li>a fa-icon {
        font-size: 16px !important;
    }
    .pageHeaderSearchInputContainer {
        position: fixed;
        right: 166px;
    }
}
</style>
```

### Benutzung:
1.  Gehe zu:  Anpassung  ➞  Stile ➞ Filter: `DEIN STIL` ➞ Tab: `Erweiterte Einstellungen`
2.  Füge dort den o.g. Quellcode ein und passe diesen an deine Bedürfnisse an und speichere ab.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
