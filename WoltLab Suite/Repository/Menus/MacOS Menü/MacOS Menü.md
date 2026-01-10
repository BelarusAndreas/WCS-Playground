
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
Template
```
<div class="macosMenu">

<div class="blocks">
  <!-- Dashboard -->
  <a href="_DEINE_URL_" class="block blockDashboard jsTooltip" title="Dashboard">
    <div class="block__item">
      <i class="fa fa-home" aria-hidden="true"></i>
    </div>
  </a>
  <!-- Artikel -->
  <a href="index.php?article-list/" class="block blockArticle jsTooltip" title="Artikel">
    <div class="block__item">
      <i class="fa fa-newspaper-o" aria-hidden="true"></i>
    </div>
  </a>
  <!-- Forum -->
  <a href="_DEINE_URL_/forum/" class="block blockForum jsTooltip" title="Forum">
    <div class="block__item">
      <i class="fa fa-comments-o" aria-hidden="true"></i>
    </div>
  </a>
  <!-- Mitglieder -->
  <a href="index.php?members-list/" class="block blockMembers jsTooltip" title="Members">
    <div class="block__item">
      <i class="fa fa-users" aria-hidden="true"></i>
    </div>
  </a>
  <!-- Profil -->
  <a href="index.php?account-management/" class="block blockProfile jsTooltip" title="Profil">
    <div class="block__item">
      <i class="fa fa-user-circle" aria-hidden="true"></i>
    </div>
  </a>
  <!-- Notification -->
  <a href="index.php?notification-list/" class="block blockNotification jsTooltip" title="Benachrichtigungen">
    <div class="block__item">
      <i class="fa fa-bell-o" aria-hidden="true"></i>
    </div>
  </a>
  <!-- Konversation -->
  <a href="index.php?conversation-list/" class="block blockConversation jsTooltip" title="Konversationen">
    <div class="block__item">
      <i class="fa fa-comments" aria-hidden="true"></i>
    </div>
  </a>
  <!-- Logout -->
  <a href="https://wcs-playground.xyz/index.php?logout/" class="block blockLogout jsTooltip" title="Logout">
    <div class="block__item">
      <i class="fa fa-power-off" aria-hidden="true"></i>
    </div>
  </a>
</div>

</div>
```

CSS
```
.macosMenu {
    background-color: rgba(0, 0, 0, 0.5);
    backdrop-filter: blur(10px);
    border: 1px solid #ccc;
    border-radius: 3px;
    position: fixed;
    bottom: 0;
    margin: auto;
    width: 50%;
    left: 25%;
    right: 25%;
    padding: 3px;
}
.blocks {
    display: flex;
    list-style-type: none;
    padding: 2px;
    border-radius: 5px;
    gap: 5px;
    align-items: center;
    justify-content: center;
    align-content: center;
}
.block {
    width: 48px;
    height: 48px;
    box-shadow: 0px 0px 2px #ccc;
    border-radius: 3px;
    display: grid;
    place-items: center;
}
.block:hover {
    animation-name: bounce;
    animation-timing-function: linear;
    animation-duration: 0.5s;
    animation-iteration-count: 2;
}
@keyframes bounce {
    0%   { transform: translateY(0); }
    10%   { transform: translateY(-5px); }
    25%  { transform: translateY(-10px); }
    10%   { transform: translateY(-5px); }
    0% { transform: translateY(0); }
}
.block i {
    color: #fff;
    font-size: 1.4em;
}
.blockDashboard {background: rebeccapurple;}
.blockArticle {background: royalblue;}
.blockForum {background: cyan;}
.blockMembers {background: forestgreen;}
.blockProfile {background: chartreuse;}
.blockNotification {background: yellow;}
.blockConversation {background: darkorange;}
.blockLogout {background: darkred;}
```

### Benutzung:
1.  Gehe zu ACP  ➞  Anpassung  ➞  Templates  ➞  Filter: `DEIN STIL`  ➞  + Template hinzufügen
2.  Vergebe dem Template nun den Namen  macosMenu.
3.  Füge dort den obigen HTML-Quellcode ein und passe diesen an deinen Bedürfnissen an und speichere ab.
4.  Gehe zu ACP  ➞  Anpassung  ➞  Templates  ➞  Filter: `DEIN STIL`  ➞  Suche:  `footer`  
     **Hinweis**:  Sollte das Template  `footer`  noch nicht in der Templategruppe vorhanden sein, so kopiere dieses zuvor aus der Standard-Templategruppe!
5.  Suche dort nach  `</body>`  und füge davor in einer neuen Zeile  `{include file='macosMenu'}`  ein und speichere ab.
6.  Fertig!


