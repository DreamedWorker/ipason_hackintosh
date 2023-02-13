# IPASON SmartBook D1 Hackintosh

As you can see, this repository holds an EFI file that can boot the macOS on this laptop. At first, let me give you a brief introduction to the basic configuration of this laptop.

## About this computer

| Hardware Type    | Name                                        |
| ---------------- | ------------------------------------------- |
| CPU              | Intel® Core™ i3-10110U 2.21GHz              |
| iGPU             | Intel® UHD Graphics 630                     |
| Monitor          | NV133FHM-N62 13.3inch                       |
| Memory           | Samsung DDR4 4GB*2 2400MHz                  |
| Disk             | NVME SSD 256GB                              |
| Network Driver   | Intel® Dual Band Wireless-AC 3165           |
| Bluetooth Driver | Intel® Built-in Bluetooth                   |
| Sound Card       | 瑞昱 High Definition Audio                  |
| Motherboard      | I/O -0284 for Intel 400 Series Chips Family |
| OS Version       | macOS Monterey 12.5.1                       |

## Ports

DC charge port x1

USB Type-A 3.1 ports x2

Type-C Full-function x1

HDMI v1.4 x1

3.5mm Headset port x1

micro-SDCard Reader x1

## What works

1. iGPU: Intel CometLake-U GT2 [UHD Graphics] 2048 MB
2. PS/2 Keyboards(The brightness adjustment shortcut key cannot be used.)
3. USB 2.0 Camera
4. Bluetooth
5. All USB ports and SD Card Reader
6. WiFi
7. Sound Card: Speaker and Microphone works and 3.5mm port also works.

## What does not work

1. Trackpad(I can find this but it has no responsibility.)
2. Sleep and native power management
3. Fingerprint identification drvier

## Tips

This EFI config file can help you boot your macOS 12 system(All versions of the system numbered Monterey will work.), but that doesn't mean you can't use it to boot macOS 11 or lower (higher) systems.

If you need to boot Big Sur or earlier, you need to disable the BlueToolFix kext and enable the IntelBluetoothInjector kext in the **config.plist** file, and you also need to prepare a wireless driver replacement for your target version to drive the wireless driver.

If you need to boot macOS 13, you only need to change the wireless network card driver to the corresponding version.

I don't know if the trackpad of this computer can be driven (after I add drivers and adjust the kext order according to the tutorial, the trackpad can be detected by system preference settings, but the mouse on the screen will not slide when I slide my hand). If you can fix this problem, you are welcome to send your proposal to the repository.

