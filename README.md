# Re4son-Pi-TFT-Setup

A tool for setting up TFT displays on a Raspberry Pi. This program is heavily based on Adafruit's PiTFT Helper.

This setup tool is used in [Sticky Finger's Kali Pi](https://www.whitedome.com.au/kali-pi).

## TFT Documentation

Products:
The following products are fully supported:

- [4D Systems 4DPi-24-HAT](http://www.4dsystems.com.au/product/4DPi_24_HAT)
- [4D Systems 4DPi-32](http://www.4dsystems.com.au/product/4DPi_32)
- [4D Systems 4DPi-35](http://www.4dsystems.com.au/product/4DPi_35)
- [PiTFT - Assembled 320x240 2.8" TFT+Touchscreen for Raspberry Pi](https://www.adafruit.com/product/1601)
- [PiTFT - Assembled 480x320 3.5" TFT+Touchscreen for Raspberry Pi](https://www.adafruit.com/product/2097)
- [Adafruit PiTFT 2.2" HAT Mini Kit - 320x240 2.2" TFT - No Touch](https://www.adafruit.com/product/2315)
- Elecrow 3.5"
- JBTek 3.5"
- KeDei 3.5"
- Kuman 3.5"
- Osoyoo 3.5"
- [Raspberry Pi 7" Touch Display - Rotate display 180 so power cable is at the top](https://www.raspberrypi.org/products/raspberry-pi-touch-display/)
- [Sainsmart 3.5"](http://www.sainsmart.com/sainsmart-3-5-inch-tft-lcd-320-480-touch-screen-display-for-raspberry-pi-2-b-b.html)
- [Waveshare 3.2"](http://www.waveshare.com/wiki/3.2inch_RPi_LCD_(B))
- [Waveshare 3.5"](http://www.waveshare.com/wiki/3.5inch_RPi_LCD_(A))
- [Waveshare 5"](http://www.waveshare.com/wiki/5inch_HDMI_LCD)

The following products may need some manual calibration:
- Elecfreaks 2.2"
- [Hotmcu HY28B 2.8"](http://www.hotmcu.com/28-touch-screen-tft-lcd-with-all-interface-p-63.html)
- JBTek
- [Sainsmart 3.2"](http://www.sainsmart.com/sainsmart-3-2-tft-lcd-module-320-240-touch-screen-display-for-raspberry-pi.html)
- [Waveshare 4"](http://www.waveshare.com/wiki/4inch_RPi_LCD_(A))



## Getting Started: Kernel & Setup Tool Installation

First, make sure /boot is mounted:
```sh
sudo mount | grep /boot
```
If /boot is not mounted, mount it now:
```sh
sudo mount /dev/mmcblk0p1 /boot
```

Install Sticky Finger's Kali-Pi Kernel:

```sh
cd ~
wget  -O re4son_kali-pi-tft_kernel_current.tar.xz https://whitedome.com.au/re4son/downloads/11299/
tar -xJf re4son_kali-pi-tft_kernel_current.tar.xz
cd re4son_kali-pi-tft_kernel_4*
sudo ./install.sh
```
Reboot.

## Updating Re4son-Pi-TFT-Setup

This setup tool can be found in the root directory folder of the kernel package.
To update it to the latest version, just run:

```sh
./re4son-pi-tft-setup -u
```

## Using Re4son-Pi-TFT-Setup

`re4son-pi-tft-helper` must be run with root privileges, and takes a parameter
specifying the type of TFT to configure.  Invoke it like so:

```sh
sudo re4son-pi-tft-setup -t 35r -d /root
```

For a full list of available options, check the help:

```sh
re4son-pi-tft-setup -h
```

## Removing TFT settings

To reset all settings, just run:

```sh
re4son-pi-tft-setup -r
```
 or

```sh
re4son-pi-tft-setup -r -d /root
``` 
 
