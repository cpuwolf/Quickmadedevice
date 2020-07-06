# Quickmadedevice

Quickmade devices USB hid handling plugin for X-Plane 11

https://x-plane.vip/quickmade/

## Quickmade Products ##

* QGMC710
* QMCP737C 


## feature ##

* no framerate impact
* rotation acceleration
* joystick keys auto assignment


## Linux ##

edit hidraw device access permission

sudo vim /etc/udev/rules.d/99-joysticks.rules

KERNEL=="hidraw*", SUBSYSTEM=="hidraw", MODE="0666", GROUP="input"