# dellintosh

https://www.tonymacx86.com/threads/guide-dell-xps-15-9560-4k-touch-1tb-ssd-32gb-ram-100-adobergb.224486/

## ssd samsung PM961

insert patches.plist to config.plist in "KextsToPatch"

## wifi
killer --> dw1830 (23eur from aliexpress.com)

https://www.windowscentral.com/upgrade-wifi-dell-xps-15

## Trackpad

http://osxdaily.com/2015/04/29/change-scrolling-speed-mouse-trackpad-mac/

## Mac App Store

For sign-in to work interface must be en0. If not: delete "all" network interfaces and then:

    sudo rm -rf /Library/Preferences/SystemConfiguration/NetworkInterfaces.plist

And reboot.

## iCloud

`brew cask install clover-configurator` and magic wand a serial.

SerialNumber: serial
BoardSerialNumber: serial + 5 hex so that length == 17
SmUUID: `uuidgen`

## TODO

 - bluetooth + wifi makes wifi to go super slow after sleep. disabled bluetooth in bios.
 - kaby lake speed thing
 - post ssd config back to the thread


## WIP:
http://touch-base.com/touch_device_list.asp
 * Didn't work. Looks and feels like shit.
