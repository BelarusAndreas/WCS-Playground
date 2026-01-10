
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
Template
```
<li class="boxMenuHasChildren">
  <a class="boxMenuLink" href="#">Extended Menu</a>
  <ol class="boxMenuDepth1">
    <li>
      <a class="boxMenuLink" href="#">Sub 1</a>
    </li>
    <li>
      <a class="boxMenuLink" href="#">Sub 2</a>
    </li>
    <li>
      <a class="boxMenuLink" href="#">Sub 3</a>
    </li>
  </ol>
</li>    
```

### Benutzung:
1.  Gehe zu ACP  ➞  Anpassung ➞  Templates  ➞  Filter: `DEIN STIL`  ➞  + Template hinzufügen
2.  Füge dort den obigen Quellcode ein und passe diesen an deinen Bedürfnissen an
3.  Vergebe den Template nun den Namen  `extendedMenu`  und speichere ab.
4.  Gehe zu ACP Anpassung  ➞  Templates  ➞  Filter: `DEIN STIL` ➞  Suche: `__menu`  
     **Hinweis:** Sollte das Template  `__menu`  noch nicht vorhanden sein, so kopiere dieses aus der Standard-Templategruppe in die deines Stils.
5.  Suche nach  `{event name='menuAfter'}`  und füge  **davor**  in einer neuen Zeile  `{include file='extendedMenu'}`  ein und speichere ab.
6.  Fertig!



