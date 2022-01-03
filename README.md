# Quickmadedevice

Quickmade devices USB hid handling plugin for X-Plane 11

https://x-plane.vip/quickmade/


## Quickmade Products ##

### QGMC710

  * hotstart TBM-900
  * and General Aviation aircrafts
https://www.youtube.com/embed/bnwsJ89BorU
 

### QMCP737C

   * zibo Boeing 737
   * IXEG 737
   * Flightfactor 757/767
   * and General Aviation aricrafts
https://www.youtube.com/embed/NRezZiCWqME

### QCDU B737/A320

  * zibo Boeing 737
  * Flightfactor 757/767
  * Flightfactor FF320
  * and General Aviation aircrafts
  
### QG1K PFD/MFD

  * hotstart TBM-900
  * and General Aviation aircrafts with G1000
  
  
### QFCU

  * Flightfactor 320
  * Toliss A319/A321

## Feature ##

* no framerate impact
* rotation acceleration
* joystick keys auto assignment

## Download

https://github.com/cpuwolf/Quickmadedevice/releases

## Install on Windows

installer is provided

Qmdev_setup.exe is for Windows user only


![qmdev](img/qmdevinstaller.gif)

## Auto Key assignment (not a must)

starting from V4.0, auto key assignment is used to clear your native X-Plane 11 key assginment
under X-Plane plugin menu, you can find qmdev plugin, there will shows up a auto key assignment window, follow the window to automatically clear buttons


![qmdev](img/autokey.JPG)



## More documents

https://github.com/cpuwolf/Quickmadedevice/wiki

## Screenshot ##

![qmdev](img/qmdev_setup.jpg)
![qmdev](img/nocost.jpg)

### Install on Linux/MacOS ##
java -jar Qmdev_Setup.jar

## Linux Manual Configuration ##

edit hidraw device access permission

sudo vim /etc/udev/rules.d/99-joysticks.rules

KERNEL=="event*", NAME="input/%k", MODE="0666", GROUP="input"

KERNEL=="hidraw*", SUBSYSTEM=="hidraw", MODE="0666", GROUP="input"



### Linux Kernel contribution ###
fix Linux Kernel joystick button max number limitation

https://patchwork.kernel.org/patch/11657985/

## Version Info ##
### V2.0 ###
optimize performance further more
add new keyword DFKEY to .cfg
add disfast dataref for temporarily disabling fast key
add QCDU, QG1K devices

