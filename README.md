# klte-ubports-install-instructions
This repository has all the instructions for installing UBTouch to your klte device.

WARNING: this may break your device. I am not liable for if you break your device, with these instructions.

How to Install Ubuntu Touch
---------------------------

Before continuing, you should read these pages to have an understanding of how Ubuntu Touch, and Halium works:
* [Halium Documentation](https://docs.halium.org/en/latest/index.html)
* [Ubuntu Touch Documentation](https://docs.ubports.com/en/latest/)

To install Ubuntu Touch on your Samsung S5, you need the following tools:
* The [halium-install](https://github.com/Halium/halium-scripts/blob/master/halium-install) script, to push the UBTouch rootfs, and the system.img files to the device,
* [Heimdall](https://glassechidna.com.au/heimdall/#downloads), to install [TWRP](https://dl.twrp.me/klte/), if not already installed, and to install the halium-boot.img file to the boot partition.
* [TWRP](https://dl.twrp.me/klte/), installed on your device, to allow the halium-install script to work correctly.
* 
