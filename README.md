# klte-ubports-install-instructions
This repository has all the instructions for installing UBTouch to your klte device.

---

Before continuing, you should read these pages to have an understanding of how Ubuntu Touch, and Halium works:
- [Halium Documentation](https://docs.halium.org/en/latest/index.html),
- [Ubuntu Touch Documentation](https://docs.ubports.com/en/latest/).

---

**!!WARNING!!**
I am not responsible for your bricked device in any way, if you do not read the instructions

---

## Prerequisites
To install Ubuntu Touch on your Samsung Galaxy S5, the following things are required:
- A Linux computer, as I don't know how to use Odin to flash things to the BOOT partition,
- [An unlocked bootloader](https://www.quora.com/How-can-I-unlock-the-bootloader-of-my-SMG900F),
- [TWRP](https://dl.twrp.me/klte/) installed on your phone, for 
- [Heimdall](https://glassechidna.com.au/heimdall/), to flash the kernel onto the BOOT partition
- [ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/), to flash things onto your phone,
- Courage, as there is a small chance you may brick your device.

If you have all of these, **congratulations**, you can install Ubuntu Touch onto your phone.

---

## Installation
1. Clone this repo, which has the images and rootfs within it with: `git clone https://github.com/RealTheHexagon/klte-ubports-install-instructions.git`,
2. Clone the halium-install repo, which has all the scripts required to install UBTouch, with: `git clone https://gitlab.com/JBBgameich/halium-install.git`,
3. Make a backup of all your data, if you want to, by booting into the recovery, and selecting `backup`, and backing up onto a external drive, such as a Micro SD card, and make sure to have a Android image downloaded in case you want to switch back,
4. Wipe the device, by going to `Wipe > Advanced Wipe` and selecting:
    - Dalvik / ART Cache,
    - System,
    - Data,
    - Internal Storage,
    - Cache
        
        Make sure you have selected the right things, and you want to wipe your device, and then swipe to wipe.
5. Reboot your device into the download mode, and run this command: `heimdall flash --BOOT path/to/halium-boot.img`, making sure to replace `path/to/halium-boot.img` with the path to the `halium-boot.img` file. This is to flash the kernel of Ubuntu Touch.
6. As soon as the flashing has completed, make sure to boot back into recovery, making sure the device doesn't boot normally, i.e into the system.
7. Flash the system.img and rootfs together with: `path/to/halium-install/script -p ut path/to/rootfs.tar.gz path/to/system.img`, while the phone is booted in the recovery.
8. While the script is running, it will ask you to enter a password. This password will be the password that you will unlock the device with, so please remember this password.
9. You are done! Reboot into the system by going `Reboot > System`, making sure to accept that there is no OS installed, which there is, and denying to install the TWRP app. When booting up, you should see the Unity8 Logo, and soon see the setup wizard.

If anything goes wrong, eg the phone stays on the Unity8 Logo, please let me know by putting a issue on [this repo](https://github.com/RealTheHexagon/klte-ubports-install-instructions), and describing where it goes wrong.
