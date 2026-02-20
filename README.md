## Lily58 Keyboard Build

This repository contains everything related to my Lily58 keyboard build. It includes the custom keymap, QMK/ZMK firmware configuration, build notes, and any additional files or documentation relevant to this setup.

The Lily58 is a column-staggered ortholinear split mechanical keyboard featuring a 6×4 layout per half, plus an additional 4 thumb keys. It is designed with ergonomics in mind, offering a more natural typing position and improved comfort during long typing sessions.

![20260204_105359](https://github.com/user-attachments/assets/d0d8aff7-7c34-476c-9130-1e7ceed3ec32)

## Firmware
#### QMK
- Clone the [official qmk firmware](https://github.com/qmk/qmk_firmware), and setup `qmk` cli.
- Override the `keyboards/lily58/keymaps/default` dir with the content of the `keymaps/defualt` of this repo.
- Compile the firmware
```bash
qmk compile -kb lily58 -km default
```
- Flash the firmware (on both sides)
```bash
qmk flash -kb lily58 -km default
```
#### ZMK
- Download the firmware [here](https://github.com/danilolucasmd/lily58/actions).
- Connect the left haft of the keyboard to the computer via the usb-c port.
- Press the rest button twice.
- Copy the the `left` haft of the firmware to the `nicenano` drive.
- Disconnect the usb-c, and repeat for the right haft.
- (Optional) If you want to clear all bt profiles and start fresh. Copy over the `reset` firmware to both halves of the keyboard. Repeat the steps above.

## Hardware
- Wired version (QMK)
  - ProMicro atmega32u4 (Arduino)
  - OLED ssd1306
- Wireless version (ZMK)
  - ProMicro nrf52840 (nice!nano clone)
  - LI-ion battery 301230 (110mah)
- 3D printed case
  - [Gabbajoe printables](https://www.printables.com/model/625411-lily58-keyboard-high-profile-case)
- 3D printed plate (Just got the plate from this project)
  - [kooziecup printables](https://www.printables.com/model/730538-aurora-lily58-mx-style-switch-case)
- 3D printed keycaps (The outer key of the thumb cluster on both halves)
  - [Scottokebs repo](https://github.com/joe-scotto/scottokeeb)

(You need **two** of each component above, one for each haft of the keyboard)

## Layers
### QMK
#### Base (Default)
<img width="857" height="310" alt="image" src="https://github.com/user-attachments/assets/ed76db4e-0ad6-4db0-bf57-080c5ad1c22c" />

#### Lower (Arrow keys & Symbols)
<img width="858" height="309" alt="image" src="https://github.com/user-attachments/assets/f4f9e3f1-d87a-4a79-844e-e96ed505f349" />

#### Raise (Mouse)
<img width="854" height="307" alt="image" src="https://github.com/user-attachments/assets/17bf9ac8-61f7-4b27-8846-27be37aa68cd" />

### ZMK
#### Base (Default)
<img width="1060" height="437" alt="image" src="https://github.com/user-attachments/assets/60e41208-da63-4664-8f5e-10e586d5ab74" />

#### Lower (Arrow keys & Symbols)
<img width="1061" height="438" alt="image" src="https://github.com/user-attachments/assets/0a87061e-6e26-4f43-bf90-16b470e1a9de" />

#### Raise (Mouse)
<img width="1057" height="430" alt="image" src="https://github.com/user-attachments/assets/decd2d82-b504-4767-9bc7-ad3d4d7a5da9" />
