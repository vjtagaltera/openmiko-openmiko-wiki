## Troubleshooting

If you can't seem to get up and running here are some things to check:

- Make sure you are using unix style line endings in wpa_supplicant.conf (this was fixed in a later release)
- Inside wpa_supplicant.conf the `psk` and `ssid` settings need to have double quotes around the string. For example `psk="password_keep_double_quotes"`
- Make sure the file does not have a `.txt` extension. The file should show up as `wpa_supplicant.conf`. `Not wpa_supplicant.conf.txt`
- The `config/overlay/etc` directory is *cAsE sEnsItiVe*. Make sure it is all lowercase.
- Make sure if you are creating .conf and .json files on a Windows machine you are using the UNIX (LF) line ending not Windows (CR LF). This can be checked in Notepad++ by turning on "Show All Characters" and changed in Settings>Preferences>New Document>Format Unix (LF).
- The MAC address does change when flashing from the one on the sticker. Check your router to see the new DHCP address.
- There are some reports that assigning a static IP / DHCP reservation does help the WyzeCam connect to the network
- Logs should appear on the sdcard if the system is properly booting
- Some WyzeCams have a buggy bootloader from the factory and won't flash anything. The only way around this is to flash a new bootloader.
- If you flashed the custom HD Dafang bootloader you will need to revert to the original one. A copy of the old WyzeCam V2 original bootloader is here: https://github.com/openmiko/openmiko/blob/master/stock_firmware/wyzecam_v2/wyzecam_v2_stock_bootloader.bin
- Join the Slack and ask a question for more help


## Issues and support

If you encounter an issue which you think is a bug in the OpenMiko or the associated libraries, you are welcome to submit it here on Github: https://github.com/openmiko/openmiko/issues.

Please provide as much context as possible:

- buildroot core version which you are using;
- kernel version and modules you have enable;
- build root packages you are trying to integrate;
- when encountering an issue which happens at run time, attach serial output. Wrap it into a code block, just like the code;
- for issues which happen at compile time, enable verbose compiler output in the buildroot preferences, and attach that output (also inside a code block);
- development board model and brand;
- other settings (board choice, flash size, etc.).


## Contributing

Pull requests are welcome. For fixes of code and documentation, please go ahead and submit a pull request.
