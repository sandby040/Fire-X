# Fire X

Stand 03.10.2026: N3 (plugin.program.nova.installer) ist enthalten.
Updates ersetzen vollständige Add-on-Programmordner nach ZIP-Prüfung und mit
Rücknahme bei fehlgeschlagenem Austausch. Stalker-Portal und Talker 3 behalten
den bisherigen Datei-Overlay-Modus. Benutzerprofile, Favoriten, MAC/Token,
HM und globale Kodi-Einstellungen werden nicht als Add-on-Code ersetzt.
ResolveURL (global), FFmpeg und Inputstream werden nicht pauschal freigegeben.

Archiv-Navigator enthält auch benötigte source-less .pyc-Module und die
angepassten Anbieter-Module als eingebetteten Code, ohne private Cookies/Logins.
Provider-Domain-Defaults werden aktualisiert, explizite persönliche Mirrors
bleiben erhalten. Alte Pakete bleiben mit unverändertem Versionsnamen erhalten.
Für inhaltliche Änderungen wird eine höhere Paketversion veröffentlicht, nicht
heimlich die gleiche ZIP-Version ersetzt. Neu bauen über build_kodi_repo.py
verwendet nun die inkrementelle Vollpaket-Publikation.

Alte Fire-X-Dienste übernehmen die neue Update-Mechanik beim ersten Start.
Beim nächsten Start erfolgt die einmalige Bereinigung eventueller Overlay-Reste,
aber nur bei vollständig übereinstimmenden gelieferten Dateien. Lokal geänderten
Code setzt diese Migration nicht ungefragt zurück. Der Dienst bleibt still,
außer wenn tatsächlich Updates installiert wurden; anschließend Nova neu starten.

Kodi-Repository-Ausgabe.

Upload-Inhalt auf GitHub/GitHub Pages:
- addons.xml
- addons.xml.md5
- alle addon-id Ordner mit ZIP-Dateien

Repository-Installer:
- repository.stube.nova/repository.stube.nova-1.0.0.zip

Base URL in diesem Build:
- https://sandby040.github.io/Fire-X/

Neu bauen:
```powershell
python build_kodi_repo.py --base-url https://sandby040.github.io/Fire-X/
```

Hinweis:
- pvr.iptvsimple, pvr.stalker und script.module.pvr sind enthalten.
- M3U/EPG/Bridge-Dateien liegen in Kodi normalerweise unter userdata/addon_data.
  Dafuer wird zusaetzlich service.stube.livetv.data gebaut.
- service.stube.livetv.data spiegelt verwaltete Live-TV-Dateien beim Start nach userdata/addon_data.
- MAC-/Token-/Session-Dateien werden bewusst nicht in das Datenpaket gepackt.
