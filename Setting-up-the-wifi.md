## Setting up the wifi

Wifi configuration is done via the sdcard.

On the sdcard create the directories `/config/overlay/etc`:

![Overlay Filesystem](https://github.com/openmiko/openmiko/raw/master/doc/img/overlay_filesystem.png)

In the `etc` directory copy the file [`wpa_supplicant.conf`](https://github.com/openmiko/openmiko/blob/master/overlay_minimal/etc/wpa_supplicant.conf). Edit this file and plug in your wifi name and password.

Insert the sdcard into the camera and reboot. OpenMiko will copy this directory over to the `/config` partition (which is persistent flash storage). This method can also be used to overwrite other files. For example:


- `/etc/passwd` and `/etc/shadow` can be overwritten to make sure password changes are persistent
- `/config/overlay/etc/dropbear/dropbear_ecdsa_host_key` can be used to have a persistent SSH signature
