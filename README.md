# QuickmadeSim Device Plugin (Qmdev)

This is the QuickmadeSim device USB driver software designed for X-Plane 11/12 and MSFS 2020/2024.
It boasts powerful extensibility, with a built-in Lua language engine that is very friendly to programming beginners, allowing you to easily add support for your own aircraft.

**Official Website and Support:**
* Cross-platform support (X-Plane 11/12/MSFS2020/2024): https://www.quickmadesim.com/?page_id=194&lang=en

# Features

*   **Zero Performance Impact**: Absolutely no impact on game frame rates (FPS).
*   **Automatic Flight Device Key Assignment**: Say goodbye to the pain of manually setting hundreds of keys.
*   **Smooth Aircraft Switching**: Say goodbye to the hassle of searching the entire internet for configuration files.
*   **Rotary Knob Acceleration**: Optimizes your operational experience.
*   **Built-in Lua Language Engine**: Simple to use and easy to customize.
*   **Easy Debugging**: Instantly reload Lua scripts without restarting X-Plane, speeding up the development process.
*   **Aircraft State Synchronization**: Supports cold and dark cockpit state synchronization.
*   **Simulated Failure Synchronization**: Supports synchronization of simulated aircraft failure states.
*   **Cross-platform Operation**: Fully supports Windows, Linux, and Mac systems.
*   **Native Apple ARM Support**: Provides native support for Apple M-series chips.

## Game Compatibility List

Please check the detailed compatibility list via the following link:
[Quickmade Device Game Compatibility List](https://docs.qq.com/sheet/DWERFQnRmVUFZeHBi?tab=000001)

## Download

You can get the latest version of the plugin from the following address:
[Latest Version Download](https://gitee.com/cpuwolf/Quickmadedevice/releases)

## Installer

We provide an easy-to-use installation wizard.

![奎克质造设备安装程序](img/qmdev_mac_install.gif)

## Installation Instructions

### Installing on MacOS

#### **MacOS Installation Steps**
1. Unzip installer_6_8_mac.zip
2. Open "Terminal" and execute the following command to allow developers who haven't paid Apple:
    ```bash
    xattr -cr installer_6_8_mac.app
    ```
3. Run installer_6_8_mac.app

### Installing on Linux

#### **Ubuntu 18.04 Installation Steps**
1. Run installer_6_8_lin

#### **Manual Configuration if Linux Device is Not Found**

You need to edit the access permissions for hidraw devices.
```bash
sudo vim /etc/udev/rules.d/99-joysticks.rules
```
Add the following content to the file:
```
KERNEL=="event*", NAME="input/%k", MODE="0666", GROUP="input"
KERNEL=="hidraw*", SUBSYSTEM=="hidraw", MODE="0666", GROUP="input"
```
Reload device rules
```bash
sudo udevadm control --reload-rules
```

#### **Linux Kernel Contribution**
We fixed the Linux kernel's limitation on the maximum number of joystick buttons, see details here:
[Linux Kernel Patch](https://patchwork.kernel.org/patch/11657985/)

## Screenshots

![轻松调试](img/menu_reload.png)
![零性能影响](img/nocost.jpg)

## Major Version Information

### **V6.3**

*   **Core Changes**:
    *   Fixed a core bug with incorrect DataRef value readings.
    *   Updated to X-Plane SDK 4.0.1.
    *   Fixed a USB log error.
*   **Lua Script Changes**:
    *   Added support for the default XP12 A333 for QFCU.
    *   Updated device logic and functional fixes for various aircraft models (Toliss, IXEG, ZIBO, Flightfactor, JarDesign) under XP12.
    *   **Note**: This update requires you to simultaneously update your QFCU firmware: [Firmware Update Address](https://www.quickmadesim.com/?page_id=658&lang=en)

### **V6.1**
*   Added a pop-up prompt when reading Lua files.

### **V6.0**
*   Added native support for MacOS M1 chip.
*   Removed all .cfg configuration files; relevant content has been integrated into Lua scripts.

### **V5.0**
*   Removed reliance on FlyWithLua to resolve its performance overhead issues.
*   Introduced the built-in ulua engine.

### **V2.0**
*   Further optimized performance.
*   Added new keyword `DFKEY` for .cfg files.
*   Added `disfast` dataref to temporarily disable fast keys.
*   Added support for QCDU, QG1K devices.

## For Developers

### **How to Write Your Own .lua Script Files**

We welcome you to write scripts for your favorite aircraft models! For detailed developer documentation, please refer to our Wiki:
[Qmdev .lua File Writing Guide](https://gitee.com/cpuwolf/Quickmadedevice/wiki/Qmdev-.lua-files)

### **More Lua Developer Documentation**

[Visit the Developer Documentation Center](https://gitee.com/cpuwolf/Quickmadedevice/wiki)
