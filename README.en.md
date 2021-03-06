# Mi 6 runs UOS

## Where to download

​	GitHub: [PreTest-0.0.1](https://github.com/BigfootACA/sagit-uos/releases/tag/PreTest-0.0.1)

​	OneDrive: [MI6-UOS-PreTest-0.0.1.7z](https://1drv.ms/u/s!AsDs1e5NdflSjluG9D3yo0WqhBl9?e=lFewBb)

​	BaiduNetdisk: [Code：n5vv](https://pan.baidu.com/s/1yZ9ddO2aIeJPPQIkPUPDKQ)

​	189 Cloud: [Code：z3ne](https://cloud.189.cn/t/uEBRZvRziay2)

​	Jianguoyun: [MI6-UOS-PreTest-0.0.1.7z](https://www.jianguoyun.com/p/DYJX_EkQhJfuCBjriMED)

​	Google Drive: [MI6-UOS-PreTest-0.0.1.7z](https://drive.google.com/file/d/1Oj50VvryFWSsOVtYhmxdtmfIpNYbZH6M/view?usp=sharing)

​	Weiyun: [MI6-UOS-PreTest-0.0.1.7z](https://share.weiyun.com/J7qf3V1o)

## Precautions

1. Flashing in the flashing package will cause **ALL USERDATA TO BE CLEARED**, including user data, internal storage, and Android system.
2. The flashing package has not been fully tested and only uses one Mi 6 for development, so it may not be able to start.
3. Due to the unofficial supported version, the system has not been optimized in any way, but it is not limited to freezes, crashes, unresponsiveness and other abnormalities during use.
4. This version is a preview version, and the stability of long-term use cannot be guaranteed. It is recommended to flash back to the Android system after use.
5. Due to technical reasons, the flashing package only supports a small number of functions, which may be fixed in future versions.
6. If you find a problem, please feedback in time, and you can also make some functional suggestions.
7. **Please do not reprint without authorization, otherwise legal responsibility will be pursued. **

## Installation Guide
### Install directly from the phone

1. **Backup your mobile phone first, otherwise the data will be gone after you refresh it, including software, photo albums, contacts, chat history, etc. **
2. Confirm that your phone has been unlocked ([Unlock Bootloader](http://en.miui.com/unlock/index.html)).
3. Download and install TWRP ([TWRP for Xiaomi 6](https://dl.twrp.me/sagit/)).
4. Download the latest version package and unzip it to obtain the flashing package UOSv20-Mi6_SAGIT-PreTest-0.0.1.zip.
5. Make sure that all the data you need has been backed up.
6. **When the battery power is less than 25%, the installation will be refused. When there is no charger, at least 80% of the power can be installed. **
7. Boot to TWRP (power button + volume up button in Mi 6).
8. Click "Advance" on the main screen of TWRP, enter "File Manager", find the flashing package, and copy it to directories other than /data, /system, /sdcard, and /cache (such as /tmp )
9. Back to the TWRP main screen, click "Install", and then select the flashing package you copied.
10. Slide the lower slider to start flashing.
11. After the installation is complete, click "Reboot System" and slide the slider to confirm. It may prompt "No OS Installed!" (No OS Installed!), please ignore.
12. After restarting, it will enter the UOS system.

### Install from computer using data cable

1. **Backup your mobile phone first, otherwise the data will be gone after you refresh it, including software, photo albums, contacts, chat history, etc. **
2. Confirm that your phone has been unlocked ([Unlock Bootloader](http://en.miui.com/unlock/index.html)).
3. Download and install TWRP ([TWRP for Xiaomi 6](https://dl.twrp.me/sagit/)).
4. Download the latest version package and unzip it.
5. Make sure that all the data you need has been backed up.
6. **When the battery power is less than 25%, the installation will be refused. When there is no charger, at least 80% of the power can be installed. **
7. Boot to TWRP (power button + volume up button in Mi 6).
8. Click "Advance" on the TWRP main screen, click "ADB Sideload", and slide the lower slider to enter Sideload mode.
9. Click flash.bat to start flashing.
10. After the installation is complete, return to the TWRP main screen, click "Reboot", click "System" in the submenu, and slide the slider to confirm. It may prompt "No OS Installed!", please ignore.
11. After restarting, it will enter the UOS system.
![Desktop experience](pics/in_uos.jpg)

## What will be updated in the next version

1. Coexist with Android, no need to clear userdata.
2. Install the boot into Recovery and use the boot menu to select boot.
3. Embedded TWRP in the boot menu
4. Fix some bugs and improve system experience.

## Known issues

1. Caton (of course)
2. The login interface cannot be displayed normally (change to automatic login)
3. Windows has no ECM network card driver (but Linux does)
4. Running the dmidecode kernel will crash and restart (then I deleted it)
5. Can't open the device manager (because of dmidecode problem)
6. The app store seems to be unavailable (finding the reason, hope the next version will work)
7. When the screen is turned off and then turned on again, the touch will fail (so turn off the automatic screen off)
8. When the charger is turned off, it will boot into the system (add the charger in the next version)

## Hardware information

Model: Mi 6

Chipset: Qualcomm Snapdragon 835 MSM8998

CPU: Kyro 280

Memory: 4GB/6GB

Storage: 64GB/128GB

Display: 1080x1920 IPS LED



## Software Information

The flashing package provides a UOS 20 Professional 1021.

The flashing package is composed of open source software, please check the flashing package for the specific list.

## Supported features

| Features          | Works | Notes                                                                                                               |
| ----------------- | ----- | ------------------------------------------------------------------------------------------------------------------- |
| Boot              | Yes   | Flash the boot partition or use fastboot boot to start the kernel                                                   |
| TTY terminal      | No    | Android kernel cannot use TTY terminal (fbcon)                                                                      |
| Display           | Yes   | The screen can be displayed by the frame buffer (msmfb) device, but there is a color cast caused by userspace       |
| Touch             | Yes   | The touch screen can be used, but may fail in some cases                                                            |
| Sound             | No    | No sound at all, may require Android userspace driver                                                               |
| Hardware accel    | No    | No drm, but a kgsl-3d device, but freedreno cannot be used                                                          |
| Camera            | No    | There is an identification device, but the kernel will report an error if it is used                                |
| Flash             | Yes   | Flash can be controlled, but Xorg does not support or is not configured                                             |
| Breathing light   | Yes   | Set to automatically light up when charging                                                                         |
| Key backlight     | Yes   | Key backlight can be controlled, but Xorg does not support or is not configured                                     |
| Screen backlight  | Yes   | Screen backlight can be controlled, but Xorg does not support or is not configured                                  |
| Power button      | Yes   | The power button can be triggered normally                                                                          |
| Button            | Yes   | Volume, menu, back, home button can be used, but Xorg does not support or is not configured                         |
| USB Host          | Yes   | Plug in OTG to use hub, mouse, keyboard, network card, U disk and other devices                                     |
| USB Gadget        | Yes   | Use the USB cable to connect to the computer to use the network card (Windows does not have a driver), serial, ADB  |
| Battery & Charger | Yes   | The battery and charger can be recognized normally, fastcharge can be used, but there are some additional equipment |
| Storage           | Yes   | UFS can recognize and read and write normally                                                                       |
| Fingerprint       | No    | Seems like none                                                                                                     |
| Infrared          | No    | Seems like none                                                                                                     |
| Sensor            | No    | Seems like none                                                                                                     |
| WiFi              | No    | Android userspace driver is required                                                                                |
| Bluetooth         | No    | Android userspace driver is required                                                                                |
| Mobile Data       | No    | Android userspace driver is required, and ModemManager does not know if it can support it                           |
| Phone dialing     | No    | Android userspace driver is required, and ModemManager does not know if it can support it                           |
| SMS               | No    | Android userspace driver is required, and ModemManager does not know if it can support it                           |
