
### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<div id="app"></div>
<script src="https://unpkg.com/webamp"></script>

<!-- Script für einfachen WinAmp Musik Player -->
<script>
    const app = document.getElementById("app")
    const webamp = new Webamp();
    webamp.renderWhenReady(app);
</script>

<!-- ODER (!) -->

<!-- Script für WinAmp Musik Player mit Playlist -->
<script>
      const Webamp = window.Webamp;
      const webamp = new Webamp({
        initialTracks: [
          {
            metaData: {
              artist: "ARTIST",
              title: "TITEL",
            },
            url: "URL ZUR MP3 DATEI",
            duration: SPIELZEIT,
          },
          // Weitere Einträge
        ],
      });
      webamp.renderWhenReady(document.getElementById("app"));
    </script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
