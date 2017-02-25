# Content/Inhalt

* [Content/Inhalt](#contentinhalt)
   * [English README: Custom css file for the Seafile server](#english-readme-custom-css-file-for-the-seafile-server)
      * [Intro](#intro)
      * [Installation](#installation)
      * [Notes](#notes)
      * [Dark theme](#dark-theme)
   * [Deutsche README: Eigene css-Datei für den Seafile-Server](#deutsche-readme-eigene-css-datei-für-den-seafile-server)
      * [Intro](#intro-1)
      * [Installation](#installation-1)
      * [Sonstiges](#sonstiges)
      * [Dunkles Thema](#dunkles-thema)
   * [Screenshots](#screenshots)

# English README: Custom css file for the Seafile server

## Intro

The Seafile server comes with a standard template that does not look bad, but does not like everyone. This can be changed by overwriting desired parts of the template with own values.

With the ***custom.css*** from this repository, the default color **orange** of the elements is changed to **green**.

## Installation

Copy the file ***custom.css*** to ***seahub-data/custom*** and add the following line to ***conf/seahub-settings.py***:

    BRANDING_CSS = 'custom/custom.css'

Finally, the Seafile server (and Seahub) must be restarted. For example in Debian Jessie this can be done with:

```bash
sudo systemctl stop seahub.service
sudo systemctl stop seafile.service
sudo systemctl start seafile.service
sudo systemctl start seahub.service
```

## Notes

- the icons for folders are not changed and still have the color orange. I'm currently looking for a way to change the folder icon color so that the changes will be kept within a server update.
- ***custom.css*** tested with Seafile Server 6.0.7

## Dark theme

You will find a very eraly alpha version of a dark theme in the branch [***dark***](../../tree/dark) of this repo.

# Deutsche README: Eigene css-Datei für den Seafile-Server

## Intro

Der Seafile-Server mit mit einem Standard-Template ausgeliefert, das grundsätzlich nicht schlecht aussieht, aber doch nicht jedem gefällt. Das kann man ändern, in dem man gewünschte Teile des Templates mit eigenen Werten überschreibt.

Mit Hilfe der ***custom.css*** aus diesem Repository wird die Standardfarbe **orange** der Elemente in **grün** geändert.

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
## Sonstiges

- die Icons'für Ordner und ähnliches sind nich nicht geändert und haben noch die Farbe orange. Ich suche zur Zeit noch eine Möglichkeit, dass so zu ändern, dass die Änderung bei einem Server-Update erhalten bleibt.
- ***custom.css*** getestet mit Seafile Server 6.0.7

## Dunkles Thema

Eine frühe Alpha-Version des dunklen Themes ist im Branch [***dark***](../../tree/dark) dieses Repos zu finden.

# Screenshots

<img src="https://raw.githubusercontent.com/focmb/seafile_custom_css_green/master/screenshots/screenshot1.png" alt="Login" width="300"> <img src="https://raw.githubusercontent.com/focmb/seafile_custom_css_green/master/screenshots/screenshot2.png" alt="Navbar" width="300">
<img src="https://raw.githubusercontent.com/focmb/seafile_custom_css_green/master/screenshots/screenshot3.png" alt="Main" width="600">
