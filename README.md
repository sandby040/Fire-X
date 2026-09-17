# Stube NOVA Repository

Kodi-Repository-Ausgabe.

Upload-Inhalt auf GitHub/GitHub Pages:
- addons.xml
- addons.xml.md5
- alle addon-id Ordner mit ZIP-Dateien

Repository-Installer:
- repository.stube.nova/repository.stube.nova-1.0.0.zip

Base URL in diesem Build:
- https://sandby040.github.io/stube-kodi-repo/

Neu bauen:
```powershell
python build_kodi_repo.py --base-url https://DEINNAME.github.io/stube-kodi-repo/
```

Hinweis:
- pvr.iptvsimple, pvr.stalker und script.module.pvr sind enthalten.
- M3U/EPG/Bridge-Dateien liegen in Kodi normalerweise unter userdata/addon_data.
  Dafuer wird zusaetzlich service.stube.livetv.data gebaut.
- service.stube.livetv.data spiegelt verwaltete Live-TV-Dateien beim Start nach userdata/addon_data.
- MAC-/Token-/Session-Dateien werden bewusst nicht in das Datenpaket gepackt.
