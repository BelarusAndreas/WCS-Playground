
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
<!-- Sidemenü links -->
@media screen and (min-width: 1025px) {
    .pageContainer {
        margin-left: 200px;
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
        margin: -50px 0  0 200px;
    }
    .userPanel {
        position: absolute;
        right: 0;
    }
    .mainMenu .boxMenu>.boxMenuHasChildren>a::after {
       content: "\f0da";
       display: block;
       font-family: "FontAwesome";
    }
}
</style>

<!-- Sidemenü rechts -->
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

### Benutzung:
1.  Gehe zu:  Anpassung  ➞  Stile ➞ Filter: `DEIN STIL` ➞ Tab: `Erweiterte Einstellungen`
2.  Füge dort den o.g. Quellcode ein und passe diesen an deine Bedürfnisse an und speichere ab.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
