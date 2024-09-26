# How to use IC Card Reader

## Environment

- Windows 11
- RaspberryPi 4
- PaSoRi RC-S380

## Windows Settings

Install Zadig and Libusb from the links below.

### Zadig

[Zadig](https://zadig.akeo.ie/)

Connect your RC-S380 to USB Port and choose RC-S380/s in toggle list.
Set Driver to "WinUSB" and install driver.

### libusb

[libusb](https://libusb.info/)

Copy "VS2015-x64\dll\libusb-1.0.dll" to "C:\Windows\System32"
Copy "VS2015-x64\dll\libusb-1.0.dll" to "C:\\Windows\SysWOW64"

## RaspberryPi Settings

### Insttall

```bash
sudo pip3 install nfcpy
sudo apt install libusb-dev python-usb
```

### Give Authority

```bash
SUBSYSTEM=="usb", ACTION=="add", ATTRS{idVendor}=="054c", ATTRS{idProduct}=="06c3", GROUP="plugdev"
```
