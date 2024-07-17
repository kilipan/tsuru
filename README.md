![tsuru](https://github.com/kilipan/tsuru/blob/main/img/tsuru_photo.jpg?raw=true)

# 鶴の恩返し (Tsuru No Ongaeshi)
A cute lil 3-row, katana-staggered keyboard with ISO-Enter compat :)

## Versions
As of now there exist two confirmed versions in this repo:
- SAMD21 version (wired, ZMK only, you will have to flash a bootloader!)
- CH552T version (wired, FAK only)

An untested wireless version can be found in the ble branch.

An STM32F072 mod of the original SAMD21 version is available [here](https://github.com/calvin-mcd/tsuru-STM).

## Layout Options
Note: The CH552T version does not support the encoder!

![KLE](https://github.com/kilipan/tsuru/blob/main/img/tsuru_KLE.png?raw=true)

## Firmware
Firmware can be found in my respective repos:
- [FAK config](https://github.com/kilipan/fak-config/tree/main/keyboards/tsuru)
- [ZMK config](https://github.com/kilipan/zmk-config-tsuru)

## Cases
A beatiful wedge case (**NOT** pictured above) was made by DizzySkizzo (`dizzyskizzo1337` on Discord), who graciously allowed me to make it available under the same license. See the `case` directory.

A super fun case with a key strap and transport shell made by krisenplan is available [on printables](https://www.printables.com/de/model/946165-tsuru-travel-keyboard-case)!

Two great cases made by [Seirin-Blu](https://github.com/seirin-blu) are available here:
- [Tsuru MFR2](https://github.com/seirin-blu/Tsuru-MFR2)
- [SK-Tsuru](https://github.com/seirin-blu/SK-Tsuru)

## Availability
All files are provided under CERN-OHL-S license. Feel free to build your own!

## Thanks
Thank you Pete Johanson for letting me use the SAMD21 schematic and zmk config from the [samd21pad](https://github.com/petejohanson/samd21pad/) and for all the help getting the bootloader onto the chip!
This would've never gotten anywhere without your help <3
