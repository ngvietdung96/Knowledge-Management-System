
# Resource (Collect all current DIY source)

## **Story inspire to split keyboard:**
https://www.youtube.com/watch?v=Big80AStHSU&list=WL&index=47

[Presentation of modern design of keyboard (evolution to split keyboard)](https://www.youtube.com/watch?v=unMXQTSQEak&list=WL&index=46)
[You need a new Keyboard](https://www.youtube.com/watch?v=76eALNFp3kk)

**List of custom keyboard (link, HW, SW,...):**
[Collection of custom keyboard](https://github.com/help-14/mechanical-keyboard).
[Collection of split keyboard](https://github.com/diimdeep/awesome-split-keyboards).

**Build guide of some keyboard (for reference):**
![](https://www.youtube.com/watch?v=iv__343ZwE0)
![](https://www.youtube.com/watch?v=7azQkSu0m_U)

[Lily58 keyboard Git](https://github.com/kata0510/Lily58), [build clip](https://www.youtube.com/watch?v=YZxqHo3DTFg) ![Lily58](https://user-images.githubusercontent.com/6285554/84393842-13960900-ac37-11ea-811e-65db2948ca73.jpg)

[Urchin keyboard git](https://github.com/duckyb/urchin), [Gerber file](https://github.com/duckyb/urchin/releases/tag/v1.0), [build clip](https://www.youtube.com/watch?v=CHSh1-dJq24)

[Corne keyboard case](https://www.printables.com/model/347524-corne-keyboard-case.  

## **Build guide of some keyboard (for reference):**
[wiki of DIY keyboard (by Xah Lee)](http://xahlee.info/kbd/diy_keyboards_index.html)
[keyboard design book](https://github.com/foostan/keyboard-design-book)

- [Corne keyboard](https://github.com/foostan/crkbd): Contain 4 line up.
	- [Corne-classic](https://github.com/foostan/crkbd/blob/main/corne-classic/doc/buildguide_en.md): Corne for Cherry MX switches.
	- [Corne-cherry](https://github.com/foostan/crkbd/blob/main/corne-cherry/doc/buildguide_en.md)[tilting](https://github.com/foostan/crkbd/blob/main/corne-cherry/doc/v2/buildguide_tilting_tenting_plate_en.md): Hotswappable Corne for Cherry MX switches by kailh PCB sockets. ![Corne-cherry](https://user-images.githubusercontent.com/736191/53021667-13e81f00-349d-11e9-9bc8-051e68fde6eb.JPG)

	- [Corne-chocolate](https://github.com/foostan/crkbd/blob/main/corne-chocolate/doc/buildguide_en.md): Hotswappable Corne for Chocolate switches using Kailh PCB hot-swap sockets. ![Corne-chocolate](https://user-images.githubusercontent.com/736191/52534969-be6c8d80-2d8b-11e9-82ac-a2cd09ab96d1.png)
	- [Corne-light](https://github.com/foostan/crkbd/blob/main/corne-light/doc/buildguide_en.md): Light-weight Corne (Easy build with a simple PCB).
- [Corne keyboard case](https://github.com/Lenbok/scad-keyboard-cases/tree/master/crkbd).

- [Jorne keyboard](https://github.com/joric/jorne/wiki) is an extended Corne with extra key.
- [Nijuni keyboard](https://github.com/krikun98/nijuni) is a 44-key split keyboard inspired by the [Jian](https://github.com/KGOH/Jian-Info) (stagger, pinky and controller footprint) and the [Jorne](https://github.com/joric/jorne) (thumb cluster and wiring).
- [SofleKeyboard](https://josefadamcik.github.io/SofleKeyboard/) is split keyboard base on Lily58, Crkbd and Hexlix keyboard

[Crazy ideal module keyboard](https://www.youtube.com/watch?v=mGShD9ZER1c&t=619s)

Guide to design a Custom keyboard: USB connector and protection, Battery management, MCU, Switch matrix, Voltage measure, Underglow RGB.
- [ZMK design guide](https://github.com/ebastler/zmk-designguide#Table-of-contents)

# Expectation and Rqmt

- [ ] Spilt keyboard.
- [ ] Portable keyboard.
	- [ ] Chargeable battery.
	- [ ] OLED support to present status.
	- [ ] Track point on right hand.
	- [ ] Mouse wheel.
	- [ ] Small and compact for travel.
- [ ] Connection:
	- [ ] Support bluetooth connection.
	- [ ] Multiple device support for bluetooth connection.
	- [ ] Wireless bootloader (OTA).
	- [ ] Wire connection support.
		ZMK only support wireless connection ???, QMK only support wire connection.
		--> For both support, need to check again.
- [ ] Functional
	- [ ] Wireless update configuration.
	- [ ] Reset button to reset device.
	- [ ] Sleep time is adjustable.

- [ ] Optional rqmt:
	- [ ] low profile?
	- [ ] Hot swap.
	- [ ] RGB led.
	- [ ] Adjustable foot for ergonomic.


# Layout
https://bit.ly/keyboard-layouts-doc
![](https://www.youtube.com/watch?v=8wZ8FRwOzhU&t=343s)
# Hardware

## MICRO CONTROLLER

### Wire uController
TBD.

### Bluetooth uController
[nRFMicro doumentation](https://github.com/joric/nrfmicro/wiki) nRFMicro is DIY for board nRF52840 (bluetooth uC of Nordic).
- DIY [alternative uC](https://github.com/joric/nrfmicro/wiki/Alternatives) to replace current Preassembled board.
- [PCBA (Printed Circuit Board Assembly)](https://github.com/joric/nrfmicro/wiki/PCBA) for some open source nRF board (document contain some information of manufacture production for board).
- Guide to DIY split 40 keyboard same guide use to test this nRFMicro [Jorne keyboard](https://github.com/joric/jorne/wiki) 

#### nRF52840 board

##### Seeed XIAOs BLE:
[Wiki for SeeedStudio XIAO](https://wiki.seeedstudio.com/XIAO_BLE/)
[Split Keyboard guide](https://www.hackster.io/geist/totem-a-tiny-splitkeyboard-with-splay-cb2e43)

##### nRFMicro:
[nRFMicro Release](https://github.com/joric/nrfmicro/releases), [iBoom](https://htmlpreview.github.io/?https://github.com/joric/nrfmicro/blob/main/hardware/ibom/ibom.html)
[E73 module aliexpress](https://vi.aliexpress.com/item/4000511833415.html?spm=a2g0o.detail.1000014.10.297c7774fYUfS4&gps-id=pcDetailBottomMoreOtherSeller&scm=1007.14452.335519.0&scm_id=1007.14452.335519.0&scm-url=1007.14452.335519.0&pvid=9a970c24-cd2c-4497-9156-7b86bc38badd&_t=gps-id:pcDetailBottomMoreOtherSeller,scm-url:1007.14452.335519.0,pvid:9a970c24-cd2c-4497-9156-7b86bc38badd,tpp_buckets:668%232846%238108%231977&pdp_npi=3%40dis%21VND%21188444.0%21152595.0%21%21%21%21%21%40210318ef16883092252431963e9485%2110000002492860862%21rec%21VN%21874204888&search_p4p_id=202307020747052714645698123367311940_1)

## INTEGRATED MOUSE

[Github: Jorne wiki for trackpad, trackball](https://github.com/joric/jorne/wiki/Trackpoint)
### Joystick
[Aliexpress: 3D Analog joystick for Nitendo Switch controller (20x23x15mm)](https://vi.aliexpress.com/item/1005005686915736.html?spm=a2g0o.productlist.main.1.fe3f5ca6asStzc&algo_pvid=23ff6383-84e7-4887-a3cf-4b09cf82b434&algo_exp_id=23ff6383-84e7-4887-a3cf-4b09cf82b434-0&pdp_npi=4%40dis%21VND%2145942%2122014.0%21%21%211.92%21%21%402101f49516921996186411718e6d72%2112000034010514075%21sea%21VN%210%21A&curPageLogUid=ejKiEFQYRU7v)
[Aliexpress: Connector for NS joystick](https://vi.aliexpress.com/item/4000264102443.html?spm=a2g0o.detail.0.0.2afeByfDByfDAs&gps-id=pcDetailTopMoreOtherSeller&scm=1007.40050.281175.0&scm_id=1007.40050.281175.0&scm-url=1007.40050.281175.0&pvid=6f9635cc-5bed-4421-a635-15dbfdb03067&_t=gps-id:pcDetailTopMoreOtherSeller,scm-url:1007.40050.281175.0,pvid:6f9635cc-5bed-4421-a635-15dbfdb03067,tpp_buckets:668%232846%238115%232000&pdp_npi=4%40dis%21VND%214764%213811.0%21%21%210.20%21%21%402103209b16925750870584306e3ad2%2110000001070316883%21rec%21VN%21%21A)


### Encoder
Panasonic barrel encoder, EVQWGD001, pretty popular lately, sells on Aliexpres:
- [https://www.aliexpress.com/item/32990950196.html](https://www.aliexpress.com/item/32990950196.html)
- https://github.com/plut0nium/0xLib/tree/main/Encoder.pretty
Examples:
- [https://kbd.news/A-low-profile-portable-BLE-design-564.html](https://kbd.news/A-low-profile-portable-BLE-design-564.html)
- [https://kbd.news/Rollow-with-thumb-encoders-627.html](https://kbd.news/Rollow-with-thumb-encoders-627.html)

### Trackball
[Github: trackball Blackberry for Corne kbd](https://github.com/vlukash/corne-trackpad)
[Trakcball/trackpad of Blackberry pinout](https://hackaday.io/project/167075-thumbmouse/log/166999-of-trackballs-and-trackpads)


### TrackPoint
[Github: Keyboard with track point (in thinkpad laptop)](https://github.com/crehmann/Buzzard/wiki/Build-Guide-(Wired))

## OLED
tbd


## BATTERY
[Battery type and Measuring battery capacity](https://github.com/joric/nrfmicro/wiki/Batteries.)
[Li-Po Rechargeable battery 110mAh (Aliexpress)](https://vi.aliexpress.com/item/32831998939.html?gatewayAdapt=glo2vnm)


## Switches
https://github.com/siderakb/key-switches.pretty
https://vi.aliexpress.com/item/1005002083363380.html?gatewayAdapt=glo2vnm


## KEYCAP
[Nuphy Air 60](https://nuphy.com/products/air60) keycap (60 keys), low profile keycap (Sponsor by my lover).
- Support [Gateron Low-profile 2.0](https://www.keychron.com/products/low-profile-gateron-mechanical-switch-set?variant=40122792575065) (Linear/Tactile/Clicky).


## Mod
https://www.youtube.com/shorts/XHD3xfWHdEo


## CASE

[case 3D print](https://www.printables.com/model/347524-corne-keyboard-case)
# Firmware
## BlueMicro
[Official document](https://bluemicro.jpconstantineau.com/docs/):BlueMicro is an easy to setup firmware for nRF52 chips utilizing Arduino. 
[Channel youtube for Bluetooth nrf52840](https://www.youtube.com/@BlueMicroWirelessKeyboards)


## QMK (Quantum Mechanical Keyboard)
[Official website](https://qmk.fm/) and [Official document](https://docs.qmk.fm/#/).
QMK is keyboard firmware base on the [tmk_keyboard](https://github.com/tmk/tmk_keyboard) firmware with some useful features for AVR and ARM processor.

**How to contribute to QMK firmware:**
- [Best Git practice for working with QMK](https://docs.qmk.fm/#/newbs_git_best_practices).

**Understand architect and how to use:**
[QMK Configurator](https://docs.qmk.fm/#/newbs_building_firmware_configurator): online graphical user interface that generate QMK Firmware `.hex` or `.bin` files (only for supported board).
[Understand QMK's Code](https://docs.qmk.fm/#/understanding_qmk).

**Con:**
Bluetooth support is limited in QMK. Note (3rd July 2023): for bluetooth 2.1 QMK has support for RN-42 modules and [Bluefruit LE SPI Friend (nRF51822)](https://www.adafruit.com/product/2633).
Other new bluetooth board may can be work but require Custom build firmware. 


## ZMK (Zephyr Mechanical Keyboard)
[Official website](https://zmk.dev/docs), [FAQ](https://zmk.dev/docs/faq).
- [Supported Hardware](https://zmk.dev/docs/hardware): ZMK only support for **32-bit** and **64-bit** platform.
- Build base on [[Zephyr Project]] as best-in-class RTOS.
- ZMK is design for the future base on wireless, so power efficiency play a critical role in every design decision, just like in Zephyr.
- Latency of ZMK. [This video](https://www.youtube.com/watch?v=jWL4nU-vtWs) show latency comparation ZMK and other keyboard firmware.


# Wireless Security

[Xah Lee Wiki for wireless security topic](http://xahlee.info/kbd/Microsoft_wireless_keyboard_key_sniffer.html)
