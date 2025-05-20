# KBD firmware

## Fix for Alpha Mod animation

This fork fixes alpha mod animation by setting in keyboard.json of standard crkbd changing the flags for the leftmost, rightmost, thumb and extra keys to 1 to set them as modifier. 

After flashing this version of the firmware open vial and select the backlight pane, select "Alphas Mods" from the animation selection menu and change the primary color with the color picker and the Hue of the secondary color with the speed slider.

## How to build

## 1. Setting Up Your QMK Environment

Please see https://docs.qmk.fm/#/newbs_getting_started and set up 1 to 3.

## 2. Getting source files

Please get source files of `qmk/qmk_firmware` and `vial-kb/vial-qmk`
```sh
make git-submodule
```

## 3. Building firmwares

### for VIA

```sh
make qmk-clean
kb=crkbd make qmk-init
kb=crkbd kr=rev4_1/standard km=via make qmk-compile
```
A built data will be stored on `keyboards/crkbd/qmk/qmk_firmware/.build`\
Please change `kb`, `kr` and `km` when build other.

### for Vial
```sh
make vial-qmk-clean
kb=crkbd make vial-qmk-init
kb=crkbd kr=rev4_1/standard km=vial make vial-qmk-compile
```
A built data will be stored on `keyboards/crkbd/vial-kb/vial-qmk/.build`\
Please change `kb`, `kr` and `km` when build other.

### All cleaning and building
```sh
make update-all
```
