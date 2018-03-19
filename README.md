# Content/Inhalt

* [Content/Inhalt](#contentinhalt)
   * [English README: Custom css file for the Seafile server](#english-readme-custom-css-file-for-the-seafile-server)
      * [Intro](#intro)
      * [Installation](#installation)
      * [Notes](#notes)
      * [Dark theme](#dark-theme)
 
# English README: Custom css file for the Seafile server

## Intro

The Seafile server comes with a standard template that does not look bad, but does not like everyone. This can be changed by overwriting desired parts of the template with own values.

With the ***custom.css*** from this repository, the default color **orange** of the elements is changed to **green**.

## Installation

Copy the file ***custom.css*** to ***seahub-data/custom*** and add the following line to ***conf/seahub-settings.py***:

    BRANDING_CSS = 'custom/custom.css'

To change the icon color for folder icons you have to copy the file folder-192.png from the img folder of this repo into the seahub folder (***seafile-server-latest/seahub/media/img***) on your server and rename it to folder-24.png. But before please create a backup of your original file. After an update of the Seafile server this change will be reverted and you have to copy it again.

If you want to use the green Favicon copy the ***favicon.png*** to ***seahub-data/custom*** and add the following line to your ***conf/seahub-settings.py***:
    
    FAVICON_PATH = 'custom/favicon.png'

Finally, the Seafile server (and Seahub) must be restarted. For example in Debian Jessie this can be done with:

```bash
sudo systemctl stop seahub.service
sudo systemctl stop seafile.service
sudo systemctl start seafile.service
sudo systemctl start seahub.service
```

## Notes

- the icons for folders are not changed and still have the color orange. I'm currently looking for a way to change the folder icon color so that the changes will be kept within a server update.
- ***custom.css*** tested with Seafile Server 6.2.1
- At the top of the custom.css you will find two variables which define the main colors (dark and light). Here you can change the color to the color you want to use:

```css
:root {
    --darkMain: #008a3b; /*dark green*/
    --lightMain: #e2f1e7; /*light green*/
}
```

## Dark theme

You will find a very eraly alpha version of a dark theme in the branch [***dark***](../../tree/dark) of this repo.
