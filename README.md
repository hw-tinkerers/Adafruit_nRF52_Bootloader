# Adafruit nRF52 Bootloader

[![Build Status](https://github.com/adafruit/Adafruit_nRF52_Bootloader/workflows/Build/badge.svg)](https://github.com/adafruit/Adafruit_nRF52_Bootloader/actions)

A CDC/DFU/UF2 bootloader for Nordic nRF52 microcontroller. UF2 is an easy-to-use bootloader that appears as a flash drive. You can just copy `.uf2`-format application images to the flash drive to load new firmware. See https://github.com/Microsoft/uf2 for more information.

DFU via serial/CDC requires [adafruit-nrfutil](https://github.com/adafruit/Adafruit_nRF52_nrfutil), a modified version of [Nordic nrfutil](https://github.com/NordicSemiconductor/pc-nrfutil). Install `python3` if it is not installed already and run this command to install adafruit-nrfutil from PyPi:

```
$ pip3 install adafruit-nrfutil
```


### Building UF2 for TR60 Keyboard

### Prerequisites
- ARM GCC
- Nordic's [nRF5x Command Line Tools](https://www.nordicsemi.com/Software-and-Tools/Development-Tools/nRF-Command-Line-Tools)
- [Python IntelHex](https://pypi.org/project/IntelHex/)

### Build:

Firstly clone this repo with following commands.
Checkout to the tr60_suppot branch.

```
git clone git@github.com:hw-tinkerers/Adafruit_nRF52_Bootloader.git
cd Adafruit_nRF52_Bootloader
git checkout tr60_support
git submodule update --init
```

Then build it with `make BOARD={board} all`, for example:

```
make BOARD=tr60_keyboard all
```

### Flash
```
make BOARD=tr60_keyboard flash
```




