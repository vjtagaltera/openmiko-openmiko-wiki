## Settings

Settings can be changed by editing /etc/videocapture_settings.json. However the changes will not persist unless you write them to the flash. To ease saving these settings copy the file to `/config/overlay/etc/videocapture_settings.json`. The files in /config are mounted to the flash chip and will survive reboots.

```
"general_settings": {
	"flip_vertical": 0,			// 1 flips image along vertical axis, 0 disables
	"flip_horizontal": 0,		// 1 flips image along horizontal axis, 0 disables
	"show_timestamp": 1 		// 1 enables timestamp, 0 disables
},
```

### Writing Config Files

On boot it is possible to put files on the sdcard and have them copied permanently to the configuration storage area of the camera.

You should create a directory called `config` on the sdcard.

Inside this directory create more directories. In particular create `/config/overlay/etc` and any files you want to write to the camera. For example to change the wifi module that is loaded create a file `<SDCARD>/config/overlay/etc/openmiko.conf`.

In `openmiko.conf` copy the default one from https://github.com/openmiko/openmiko/blob/master/overlay_minimal/etc/openmiko.conf and change the line that says `WIFI_MODULE=8189fs` to `WIFI_MODULE=8189es`.


### profile

```
0 - profile Constrained Baseline
1 - profile Main
2 - profile High
```

### Resetting the configuration

While the camera is started hold down reset button for at least 6 seconds.
After 6 seconds the blue LED should turn on and pulse 3 heartbeats. The `/config` partition (which is mounted to the persistent flash memory itself) will be removed.
