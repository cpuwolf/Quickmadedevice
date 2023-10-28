# Quickmadedevice

Quickmade devices USB handling plugin for X-Plane 11/12. It has great extensibility to add more aircrafts on your own.

its built-in Lua Language engine is easy for programming beginner

https://x-plane.vip/quickmade/


for MSFS2020 support

https://www.quickmadesim.com/

https://sourceforge.net/projects/qmdevsimconnect/

# Features

 * zero framerate(FPS) impact
 * joystick keys auto assignment (manually assign hundreds of keys is a great pain)
 * rotatory knob acceleration
 * Lua language engine built-in
 * easy debug: instant reload lua files without restarting X-Plane
 * aircraft cold and dark sync
 * aircraft simulated failure sync
 * running on Win/Lin/Mac
 * Native Apple ARM support


## Quickmade Products ##

### QGMC710

  * Hotstart TBM-900
  * and General Aviation aircrafts
    https://www.youtube.com/embed/bnwsJ89BorU
 

### QMCP737C

   * ZIBO Boeing B738
   * Level-up Boeing B736/737/739
   * MAX team design B737MAX
   * IXEG B737-300
   * Flightfactor B757/767
   * Flightfactor B777
   * Toliss A319/A321
   * and General Aviation aricrafts
     https://www.youtube.com/embed/NRezZiCWqME

### QCDU B737/A320

   * ZIBO Boeing B738
   * Level-up Boeing B736/B737/B739
   * IXEG B737-300
   * Flightfactor B757/767
   * Flightfactor B777
   * Flightfactor FF320
   * and General Aviation aircrafts
  
### QG1K PFD/MFD

  * hotstart TBM-900
  * and General Aviation aircrafts with G1000
  
  
### QFCU

  * Flightfactor A320
  * Toliss A319/A321/A340
  * JARDesign A330/A320

## Download

https://github.com/cpuwolf/Quickmadedevice/releases

## Install on Windows

installer is provided

Qmdev_setup.exe is for Windows user only


![qmdev](img/qmdevinstaller.gif)

## Auto Key assignment (not a must)

starting from V4.0, auto key assignment is used to clear your native X-Plane 11/12 key assginment
under X-Plane plugin menu, you can find qmdev plugin, there will shows up a auto key assignment window, follow the window to automatically clear buttons


![qmdev](img/autokey.JPG)



## More documents

https://github.com/cpuwolf/Quickmadedevice/wiki

## Screenshot ##

![qmdev](img/qmdev_setup.jpg)
![qmdev](img/nocost.jpg)

### Install on Linux/MacOS ###
java -jar Qmdev_Setup.jar

#### Ubuntu18.04 openJDK requirement ####

sudo apt install openjdk-11-jre

#### Linux Manual Configuration ####

edit hidraw device access permission

sudo vim /etc/udev/rules.d/99-joysticks.rules

KERNEL=="event*", NAME="input/%k", MODE="0666", GROUP="input"

KERNEL=="hidraw*", SUBSYSTEM=="hidraw", MODE="0666", GROUP="input"



#### Linux Kernel contribution ####
fix Linux Kernel joystick button max number limitation

https://patchwork.kernel.org/patch/11657985/

## Version Info ##
### V2.0 ###
optimize performance further more
add new keyword DFKEY to .cfg
add disfast dataref for temporarily disabling fast key
add QCDU, QG1K devices

### V5.0 ###
remove dependency of FlyWithLua, because Flywithlua costs fps, which cannot meet my expectation
introduce builtin ulua

### V6.0 ###
native MacOS M1 support
remove all .cfg file, and add content into lua

### V6.1 ###
add pop up window while it is reading the lua files

### V6.3 ###

This update requires you to update QFCU firmware
https://www.quickmadesim.com/?page_id=658&lang=en

Core Changes:

 * Qmdev core a bug fix in reading back wrong Dataref value
 * update X-Plane SDK 4.0.1
 * a USB log error fix

Lua scripts Changes:

 * add QFCU default XP12 A333 support

 * Update Toliss Airbus XP12 QFCU brightness control change
 * Update Toliss Airbus XP12 QFCU power on/off logic
 * Update Toliss Airbus XP12 QCDU power on/off logic
 * Update IXEG B737 classic plus XP12 QMCP737 A/T LED light
 * Update IXEG B737 classic plus XP12 QCDU EXEC light

 * Update ZIBO B737 XP12 QCDU EXEC light
 * Update Flightfactor B757 XP12 QCDU EXEC/MSG lights
 * Update Flightfactor B757 XP12 QMCP737C IAS/MACH logic
 * Update Flightfactor A320 XP12 QFCU power on/off logic
 * Update Flightfactor A320 XP12 QCDU power on/off logic

 * fix Toliss Airbus XP12 QFCU SPD/HDG preselect function
 * fix Toliss Airbus XP12 QFCU EFIS Baro bias 
 * fix Flightfactor A320 XP12 QFCU SPD/HDG preselect function
 * fix JarDesign Airbus QFCU HDG/ALT/BARO rotation function


## For Developers ##

How to write your own aircraft config file

https://github.com/cpuwolf/Quickmadedevice/wiki/Qmdev-.cfg-files

How to write your own .lua scripts file

https://github.com/cpuwolf/Quickmadedevice/wiki/Qmdev-.lua-files
