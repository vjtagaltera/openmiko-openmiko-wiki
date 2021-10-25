# OpenMiko

OpenMiko is custom opensource firmware for cameras that use the Ingenic T20 chip.
These cameras include the Wyzecam V2 and Xiaomi Xiaofang.

The firmware aims to provide an an alternative to the closed source out of box firmwares which can often be riddled with bugs and security holes. Privacy is also a concern as it is difficult to tell if out of box firmware reaches out to other servers or is broadcasting metadata.

## Features

- No app to download
- Support for common protocols such as RTSP and MJPEG
- SSH server
- ffmpeg
- mjpg-streamer
- Easily add or compile your own applications
- Supported by OctoPrint (https://community.octoprint.org/t/wyze-cam-v2-and-octoprint-as-of-28dec2020/27081)

## Differences between this project and DaFang Hacks / OpenFang

This project is focused on providing a better foundation for developers and end users.
At the time of this project OpenFang was relatively quiet. DaFang Hacks has some activity
but I felt the way it was made was not necesssarily conducive to developing on a solid platform.

This project generously uses the code from both projects and it is much appreciated.

A few of the quality of life improvements in this project aimed at developers:

- A standardized toolchain based on [Buildroot](https://buildroot.org/)
- Docker image for development with precompiled artifacts available for download
- A compiled `uboot` based bootloader with USB ethernet and ext4. Load kernel images (`uImage.lzma`)
via TFTP for faster development.


## For end users

This firmware is a drop in replacement for the stock firmware. Care has been taken to ensure the firmware is compatible with the current flashing methods available. This means there is no need to rewrite the bootloader and that future firmware releases from the original manufacturer should continue to work.

For help join our Slack Channel:

https://join.slack.com/t/openmiko/shared_invite/zt-vcu9bpqt-VbEhxli_jHapEyj1Xu0ZAg

## Overview

At the present time, this repository only contains kernel and rootfs for cameras using Inegnic T20 SOC. To ease identifying these cameras please use the pictures below. A more detailed technical description can be found [here](doc/overview.md).

Ingenic T20X (128Mb DDR) | &nbsp;
:-- | --:
| ![Wyze Cam v2](https://github.com/openmiko/openmiko/raw/master/doc/wyzecam_v2/img/wyzecam_v2.jpg) | Wyze Cam V2 | 
| ![Xiaomi Dafang](https://github.com/openmiko/openmiko/raw/master/doc/xiaomi_dafang/img/xiaomi_dafang.jpg) | Xiaomi Dafang |
| ![Wyze Cam Pan](https://github.com/openmiko/openmiko/blob/master/doc/WYZECP1/img/wyzecam_pan.jpg) | Wyze Cam Pan |

If you have a device with a Ingenic T10 SOC, consider using for now https://github.com/EliasKotlyar/Xiaomi-Dafang-Hacks

If you have a classic XiaoFang with a ARM-Processor, consider using https://github.com/samtap/fang-hacks
