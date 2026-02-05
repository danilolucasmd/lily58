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
- Download the firmware [here](https://github.com/danilolucasmd/lily58-wireless-view-zmk-config/actions).
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

(You need **two** of each component above, one for each haft of the keyboard)

## Layers

### Layer 0 (Base)
<img width="854" height="308" alt="image" src="https://github.com/user-attachments/assets/24d73fe3-b742-41aa-9717-8546eeffbacb" />

### Layer 1 (Arrow keys & Symbols)
<img width="858" height="309" alt="image" src="https://github.com/user-attachments/assets/f4f9e3f1-d87a-4a79-844e-e96ed505f349" />

### Layer 2 (Mouse)
<img width="858" height="307" alt="image" src="https://github.com/user-attachments/assets/f5e2c4ed-e8db-47a6-9a65-606838cb4bc1" />
