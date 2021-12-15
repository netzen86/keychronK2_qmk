# Installing QMK on Keyhcron K2 V2 RGB Hot-swappable (C3H) on MAC OS

Based on this aticle https://github.com/CanUnesi/QMK-on-K6

![](https://raw.githubusercontent.com/netzen86/keychronK2_qmk/main/img/chip.jpg)

On my version board MCU is blank no serial number. Flashing keyboard on your risk.

## 1. Clone the SonixQMK repository 
git clone https://github.com/SonixQMK/qmk_firmware.git

## 2. Change directory to qmk_firmware
cd qmk_firmware

## 3. Pull the submodules
make git-submodule

## 4. Install utilities
util/qmk_install.sh

## 5. Install gcc 
brew install --cask gcc-arm-embedded 

## 5. Make default firmware
make keychron/k2:default

Compiled firmware in *qmk_firmware* directory  

## 6. Get Sonix Flasher
https://github.com/SonixQMK/sonix-flasher/releases

download flasher-mac.dmg

## 7. Use the 2-position switch to put the keyboard into wired mode

## 8. Enter Boot Mode

Remove the spacebar. Using a conductor, such as a control pen or a tweezer or clip, touch the two boot pins in the image below. While shorting the pins, plug in the keyboard.

![](https://raw.githubusercontent.com/netzen86/keychronK2_qmk/main/img/boot_pins.jpg)

## 9. Run "Sonix Keyboard Flasher"
![](https://raw.githubusercontent.com/netzen86/keychronK2_qmk/main/img/sonixflash2.jpg)
Radio button "qmk offset" did not fit, increase the size of the window.
![](https://raw.githubusercontent.com/netzen86/keychronK2_qmk/main/img/sonixflash1.jpg)

## 10. Plug bord on mac book
Press refresh buttton. Make sure you have picked SN32F24x for the device and 0x00 for qmk offset.

## 11. This is the point of no return, click “Flash QMK…” and choose the .bin file you created in *qmk_firmware* directory. It will flash as soon as you choose the file.

## 12. Change keymap in key board directory 
qmk_firmware/keyboards/keychron/k2/keymaps

Copy defaul folder for new name and make keychron/k2:(yourname)

https://docs.qmk.fm/#/keycodes_basic
