
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
CSS

    .conversationUsageBarButton {
        position: absolute;
        width: 100%;
        z-index: 999;
        border-radius: 0 0 2px 2px;
        bottom: 0;
        left: 0;
        overflow: hidden;
    }

Template
```
{assign var='conversationCount' value=$__wcf->getConversationHandler()->getConversationCount()}
{assign var='maxConversationCount' value=$__wcf->session->getPermission('user.conversation.maxConversations')}
<p class="conversationUsageBar conversationUsageBarButton{if $conversationCount/$maxConversationCount >= 1.0} red{elseif $conversationCount/$maxConversationCount > 0.9} yellow{/if}">
  <span style="width: {if $conversationCount/$maxConversationCount < 1.0}{@$conversationCount/$maxConversationCount*100|round:0}{else}100{/if}%">{#$conversationCount/$maxConversationCount*100}%</span>
</p>
```

### Benutzung:
1.  Gehe zu ACP  ➞  Anpassung  ➞  Templates  ➞  Filter: `DEIN STIL`  ➞  Suche:  `__userPanelConversationDropdown`
2.  Suche dort nach  `<span>{lang}wcf.conversation.conversations{/lang}`  und füge  **davor**  den obigen Template-Quellcode ein und passe diesen an deinen Bedürfnissen an und speichere ab.
3.  Gehe zu ACP ➞  Anpassung  ➞  Stile  ➞  Filter: `DEIN STIL`  ➞  Tab: `Erweiterte Einstellungen`
4.  Füge dort den obigen CSS-Quellcode ein und passe diesen an deinen Bedürfnissen an und speichere ab.
5.  Fertig

