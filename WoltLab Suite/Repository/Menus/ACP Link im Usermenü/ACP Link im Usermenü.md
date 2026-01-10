
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
{* Das XXX ist mit der Benutzergruppen-ID des Administrators zu ersetzen! *}
{if XXX|in_array:$__wcf->user->getGroupIDs()}
<li>
  <a href="index.php/acp/" class="jsTooltip" title="Administration">
    <span class="icon icon32 fa-shield"></span>
  </a>
</li>
{/if}
```

### Benutzung:
1.  Gehe zu:  Anpassung  ➞  Templates ➞ Filter: DEIN STIL ➞ Suche: `pageHeaderUser`
2.  Suche dort nach `<!-- page search -->` und füge **davor** in einer neuen Zeile den obigen Quellcode ein und passe diesen an deinen Bedürfnissen an und speichere ab.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
