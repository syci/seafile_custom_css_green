# Dark theme for the Seafile Server webinterface
Dark theme (grey / green) for the Seafile server webinterface

Tested with Seafile Server 6.0.7.

## Information

**IMPORTANT:** The theme is in a very early alpha state. But If you want to give it a try and you are using the ***custom.css*** for the light theme, be sure you have a backup of the actual ***custom.css***.

## Installation

Copy the file ***custom.css*** to seahubdata/custom and add the following line to ***conf/seahub_settings.py***:

```bash
BRANDING_CSS = 'custom/custom.css'
```
Now restart seahub and seafile server. For example if you are using systemd and unit files:

```bash
sudo systemctl stop seahub.service
sudo systemctl restart seafile.service
sudo systemctl start seahub.service
```

## Screenshots

First screenshots with dark elements.

<img src="https://github.com/focmb/seafile_custom_css_green/blob/dark/screenshots/screenshot1_dark.png" alt="Login" width="300">
<img src="https://github.com/focmb/seafile_custom_css_green/blob/dark/screenshots/screenshot2_dark.png" alt="Login" width="900">
