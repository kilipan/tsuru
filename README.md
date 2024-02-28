![tsuru](https://github.com/kilipan/tsuru/blob/main/img/tsuru_photo.jpg?raw=true)

# 鶴の恩返し (Tsuru No Ongaeshi)
A cute lil 3-row, katana-staggered keyboard with ISO-Enter compat :)

## Layout Options
![KLE](https://github.com/kilipan/tsuru/blob/main/img/tsuru_KLE.png?raw=true)

## BOM
| Amount | Part | LCSC part number | Schematic Designator |
|-------:|:-----|:-----------------|:---------------------|
|      1 | Tsuru PCB |             |                      | 
|      1 | Tsuru Plate |           |                      | 
|      1 | ATSAMDE18A-AF | C618770 | U1                   |
|      1 | SOT-23-5 Linear Voltage Regulator | C3021085 | U2 |
|      1 | Top-Mount USB-C Receptacle | C3001293 | J1     |
|      1 | SKQGAKE Button | C388858 | SW2                 |
|     15 | BAV70 Diodes | C5184417 | D1, ..., D15         |
|      2 | 0805 1nF Capacitors | C129637 | C1, C3         |
|      1 | 0805 100nF Capacitor | C2169363 | C2           |
|      2 | 0805 5.1kΩ Resistors | C118848 | R1, R2        |
|      1 | 0805 1kΩ Resistor | C140870 | R3               |
|  30-31 | Kailh MX Hot Swap Sockets | C5184526 | MX1, ..., MX32|

## Bootloader
Since the SAMD21 doesn't come pre-flashed with a bootloader, you will have to flash one yourself.
The tested and confirmed working `.elf` file is available [right here](https://github.com/kilipan/tsuru/blob/main/bootloader-tsuru.elf).
You may flash it using `arm-none-eabi-gdb` with your favorite hardware debugger, using the following commands:
```sh
sudo -E arm-none-eabi-gdb path/to/bootloader-tsuru.elf
(gdb) target extended-remote /dev/ttyACM0
(gdb) mon swd_scan
(gdb) att 1
(gdb) mon erase
(gdb) load
(gdb) run
```
Depending on your setup and operating system, the name and number of your serial device may vary.

## Firmware
Tested and working [ZMK firmware](https://github.com/kilipan/zmk-config-tsuru) is available.

## Availability
All files are provided under CERN-OHL-S license. Feel free to build your own!

## Thanks
Thank you Pete Johanson for letting me use the SAMD21 schematic and zmk config from the [samd21pad](https://github.com/petejohanson/samd21pad/) and for all the help getting the bootloader onto the chip!
This would've never gotten anywhere without your help <3
