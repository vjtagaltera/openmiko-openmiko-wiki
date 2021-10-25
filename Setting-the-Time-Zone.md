For those looking to understand how to set your timezone, there are instructions at this page: https://pubs.opengroup.org/onlinepubs/007904975/basedefs/xbd_chap08.html

The are further examples here: http://leaf.sourceforge.net/doc/buci-tz.html

As an example for my situation (Eastern Timezone), I've done the following:
```
echo EST5EDT > /etc/TZ # assigns the value now...
echo EST5EDT > /sdcard/config/overlay/etc/TZ # assign the value for reboots...
```
For pacific time:
```
PDT8PST
```