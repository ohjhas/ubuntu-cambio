# Ubuntu Cambio
Custom Ubuntu 22.04 iso to install on the MS Surface Clone RCA Cambio W101 V2 that comes with all stuff, like SileadTouchScreen Drivers, or other things.

# Tablet Images
![image](https://github.com/user-attachments/assets/6e3e5650-c788-470a-9db7-b010d2950200)
![image](https://github.com/user-attachments/assets/9d30671b-f657-4e2f-9591-7af6b86a6cb1)

# How to install

Boot into the USB drive with the iso flashed on it

Wait for it to boot

(Note: you will see a glitched grub in most cases, but don't worry, thats normal! just press enter to boot into the installation environment)

Go into the LiveCD

Open a terminal and run:

```
sudo preparetoinstall
```

This command will download necessary files so installation won't fail (It will download 32 bit GRUB Binaries so the 32 bit bootloader will bot x64 OS)

(Wifi connection is mandatory)

After the command finishes, now you can open Ubiquity (ubuntu desktop installer) and follow the steps (it is recommended to do manual partitioning to make a swap)

Install base/minimum system and no additional firmware/media formats, otherwise probably installation will freeze, but you can anyways try

Also connect to WiFi just in case

Done!

If you have any issues contact me on TG @frpixie2007

# Sources
https://github.com/devinsmith/rca-cambio-linux

https://linuxiumcomau.blogspot.com/2022/05/adding-32-bit-grub-bootloader-to-boot.html

https://github.com/onitake/gsl-firmware

# Workarounds


# Calibrating

Run xinput_calibrator under the original screen rotation; touch (preferably using a stylus) each one of the 4 corners on the screen to generate the calibration matrix:

```
xrandr --orientation normal

xlibinput_calibrator --show-xinput-cmd

xrandr --orientation right
```

The touchscreen should be now calibrated; update the udev settings with the values displayed by xlibinput_calibrator for the xinput command.
