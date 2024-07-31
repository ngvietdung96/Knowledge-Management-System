Tag: #SecondBrain 
Status: #open 
Related: [[Single-board computer (SBCs)]], [[Open Source]]

---
# BeagleBone

[[Open Source]] HW and OS base on [[Linux]]

github: https://github.com/beagleboard
forum: https://forum.beagleboard.org/


## BeagleBone Gateway
wiki: https://wiki.seeedstudio.com/BeagleBone-Green-Gateway/
https://www.beagleboard.org/boards/seeedstudio-beaglebone-green-gateway

**Chipset**: [[AM335x| AM3358]] 1GHz ARM® Cortex-A8

### Board Features

**Fully Compatible with BeagleBone® Black and Seeed Studio BeagleBone® Green**
**Connectivity**
- Ethernet 10/100M bit
- WiFi 802.11 b/g/n 2.4GHz
- USB client for power & communications
- USB host
- SD/MMC Connector for microSD
- Bluetooth 4.1 with BLE
- 2x 46 pin headers
- 2x Grove connectors (I2C and UART)
- DC Jack for power, 12V
**Software Compatibility**
- Debian
- Android
- Ubuntu
- Cloud9 IDE on Node.js w/ BoneScript library
- plus much more


|Item|Value|
|---|---|
|Processor|AM3358 1GHz ARMR Cortex-A8|
|RAM|512MB DDR3|
|on-board Flash Storage|4GB eMMC|
|CPU Supports|NEON floating-point & 3D graphics accelerator|
|Micro USB Supports|Powering & Communications|
|USB|USB 2.0 Host x2|
|GPIO|2 x 46 pin headers|
|Ethernet|1|
|Wireless Connectivity|Wi-Fi 802.11b/g/n 2.4GHz and Bluetooth 4.1 LE|
|Grove Connectors|Grove I2C x 1 and Grove UART x 1|
|Operating Temperature|0 ~ 70|
|Buttons|3|

### Boot option

![[BeagleBoneGateway_SYSBOOT0..15_SwitchS2.png]]
![[AM335xBootConfig.png]]



## WiFi Configuration (wpa_supplicant)

```bash
sudo nano /etc/wpa_supplicant/wpa_supplicant-wlan0.conf
```
and then
```bash
sudo wpa_cli -i wlan0 reconfigure
```






---
# Reference
BeagleBone Gateway from SeeedStudio schematic: 
![[SeeedStudio BeagleBone Green Gateway_v1.0_SCH_191203.pdf]]