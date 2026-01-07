
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<select name="select" onchange="location = this.value;" style="width: 100%;">
  <optgroup label="Benutzerkonto">    
    <option value="#">Bitte auswahl treffen</option>
    <option value="{$__wcf->getPath('wcf')}index.php?account-management/">Verwaltung</option>
    <option value="{$__wcf->getPath('wcf')}index.php?account-security/">Sicherheit</option>
    <option value="{$__wcf->getPath('wcf')}index.php?avatar-edit/">Avatar</option>
    <option value="{$__wcf->getPath('wcf')}index.php?signature-edit/">Signatur</option>
  </optgroup>
  <optgroup label="Einstellungen">
    <option value="{$__wcf->getPath('wcf')}index.php?settings/">Einstellungen</option>
    <option value="{$__wcf->getPath('wcf')}index.php?settings/&category=privacy">Privatsphäre</option>
    <option value="{$__wcf->getPath('wcf')}index.php?notification-settings/">Benachrichtigungen</option>
  </optgroup>
  <optgroup label="Community">
    <option value="{$__wcf->getPath('wcf')}index.php?notification-list/">Benachrichtigungen</option>
    <option value="{$__wcf->getPath('wcf')}index.php?following/">Benutzer, denen ich folge</option>
    <option value="{$__wcf->getPath('wcf')}index.php?ignored-users/">Blockierte Benutzer</option>
  </optgroup>
</select>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
