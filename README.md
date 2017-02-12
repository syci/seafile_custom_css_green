# Eigene css-Datei für den Seafile-Server

Der Seafile-Server mit mit einem Standard-Template ausgeliefert, das grundsätzlich nicht schlecht aussieht, aber doch nicht jedem gefällt. Das kann man ändern, in dem man gewünschte Teile des Templates mit eigenen Werten überschreibt.

Mit Hilfe der ***custom.css*** aus diesem Repository wird die Standardfarbe **orange** der Elemente in **grün** geändert.

**INFO:** Die Icons'für Ordner und ähnliches sind nich nicht geändert und haben noch die Farbe orange. Ich suche zur Zeit noch eine Möglichkeit, dass so zu ändern, dass die Änderung bei einem Server-Update erhalten bleibt.

## Installation

Dazu muss man die Datei namens ***custom.css*** in den Ordner ***seahub-data/custom*** kopieren und im conf-Ordner des Seafile-Servers die Datei seahub_settings.py angepassen, in dem folgender Eintrag hinzugefügt wird:

    BRANDING_CSS = 'custom/custom.css'

Zuletzt muss noch der Seafile-Server (und Seahub) neugestartet werden. Das erfolgt zum Beispiel bei Debian Jessie mit:

```bash
sudo systemctl stop seahub.service
sudo systemctl stop seafile.service
sudo systemctl start seafile.service
sudo systemctl start seahub.service
```

## Screenshots

<img src="https://raw.githubusercontent.com/focmb/seafile_custom_css_green/master/screenshot1.png" alt="Login" width="300"> <img src="https://raw.githubusercontent.com/focmb/seafile_custom_css_green/master/screenshot2.png" alt="Navbar" width="300">
