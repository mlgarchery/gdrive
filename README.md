# Building my own Gdrive web app using Snapcraft and Brave browser

Okay so I wanted to create a web app completely separated from my usual browser instance, so that I can switch to this app (Google Drive) more easily during my workflow (I am using 
GNOME as my desktop manager).

After a failure to create fake apps playing with the WM_CLASS and xdotool,
I decided to use the jackhammer: Snapcraft. In order to create a whole new app. The resulting snap is of size 260MB.

Thanks to Brave being awesome and open source, a [snapcraft.yaml](https://github.com/brave/brave-browser-snap) was available for snaping brave.

I just changed the snapcraft.yaml to rename the snap app name, added a part to dump gdrive.desktop and a google_drive.png file at the right spot,
in the snap usr/share/ folder.



## Build the snap

`snapcraft`

If you want to use lxd:
`snapcraft --use-lxd`

## Install the resulting .snap (in devmode)

`snap install --devmode gdrive_<version>_amd64.snap`

## Launch !

`gdrive`
