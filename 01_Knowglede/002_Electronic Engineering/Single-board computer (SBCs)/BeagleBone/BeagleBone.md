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

| Item                   | Value                                                                                                           |                                                                   | Chip              |     |
| ---------------------- | --------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------- | --- |
| Processor              | AM3358 1GHz ARMR Cortex-A8                                                                                      |                                                                   |                   |     |
| RAM                    | 512MB DDR3                                                                                                      |                                                                   |                   |     |
| on-board Flash Storage | 4GB eMMC                                                                                                        | MMC1                                                              | EMMC04G-M627      |     |
| SD card                |                                                                                                                 | MMC0                                                              | EMIF06-MSD02N16   |     |
| CPU Supports           | NEON floating-point & 3D graphics accelerator                                                                   |                                                                   |                   |     |
| Micro USB Supports     | Powering & Communications                                                                                       | USB0                                                              |                   |     |
| Ethernet               | USB to 1 Ethernet and 2 USB, EEPROM<br>nLNKA_LED<br>nSPD_LED                                                    | USB1<br>                                                          | LAN9512-JZX       |     |
| USB                    | USB 2.0 Host x2                                                                                                 | USB1                                                              | LAN9512-JZX       |     |
| EEPROM (Optional)      | 128 * 16 = 2048 bytes                                                                                           |                                                                   | 93LC66AT-I/OT<br> |     |
| Wireless Connectivity  | Wi-Fi 802.11b/g/n 2.4GHz                                                                                        | MMC2                                                              | WL1835MODGBMOC    |     |
|                        | Bluetooth 4.1 LE                                                                                                | UART3                                                             | WL1835MODGBMOC    |     |
| Debug                  |                                                                                                                 | UART0                                                             | SN74LVC2G241DCUR  |     |
| Operating Temperature  | 0 ~ 70                                                                                                          |                                                                   |                   |     |
| Buttons                | S3: RESET <br>S1: POWER <br>S2: BOOT                                                                            | <br><br>LCD_DATA2                                                 | <br><br>SYSBOOT2  |     |
| LED                    | LED4: USR0<br>LED5: USR1<br>LED6: USR2<br>LED7: USR3<br>LED1: 3V3<br>LED2: BT_EN<br>LED3: WLAN_EN<br>LED8: WLAN | GPMC_A5<br>GPMC_A6<br>GPMC_A7<br>GPMC_A8<br><br><br><br>MII1_RXD0 |                   |     |
| GPIO                   | 2 x 46 pin headers                                                                                              |                                                                   |                   |     |
| Operating Temperature  | 0 ~ 70                                                                                                          |                                                                   |                   |     |
|                        |                                                                                                                 |                                                                   |                   |     |
### Boot option

![[BeagleBoneGateway_SYSBOOT0..15_SwitchS2.png]]
![[AM335xBootConfig.png]]

SYSBOOT[4:0] = 11100b - Boot button released (eMMC/SDcard/UART0/microUSB)
SYSBOOT[4:0] = 11000b - Boot button pressed (SPI0/SDcard/microUSB/UART0)


### Boot from mirco SD card (MMC0)


### Boot from microUSB (USB0)



### Boot from UART0 (debug uart port)
![[UART Boot for  AM3358.png]]


### Boot from microUSB (USB0)
https://github.com/ungureanuvladvictor/BBBlfs
https://github.com/ravikp7/node-beagle-boot
https://lumpynose.wordpress.com/2014/02/10/beaglebone-black-usb-hard-drive-boot-setup/

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