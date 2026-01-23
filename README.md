## Lily58 Keyboard Build

This repository contains everything related to my Lily58 keyboard build. It includes the custom keymap, QMK firmware configuration, build notes, and any additional files or documentation relevant to this setup.

The Lily58 is a column-staggered ortholinear split mechanical keyboard featuring a 6×4 layout per half, plus an additional 4 thumb keys. It is designed with ergonomics in mind, offering a more natural typing position and improved comfort during long typing sessions.

## Firmware flash
- Go to the [QMK configurator](https://config.qmk.fm/), compile the firmware and download it.
- Run the flash command using `avrdude`
```bash
sudo avrdude -v -p atmega32u4 -c avr109 -P /dev/ttyACM0 -b 57600 -D -U flash:w:/home/danilolucasmd/Downloads/lily58_rev1_lily58.hex:i
```

## Layers

### Layer 0 (Normal)
<img width="857" height="309" alt="image" src="https://github.com/user-attachments/assets/db4afab2-16aa-4dfb-87c9-4b26aa4637ea" />

### Layer 1 (Arrow keys & Symbols)
<img width="855" height="307" alt="image" src="https://github.com/user-attachments/assets/a0a56d77-347d-4d10-8dcb-1f6a51137317" />

### Layer 2 (Mouse)
<img width="856" height="308" alt="image" src="https://github.com/user-attachments/assets/3efd1c74-df9e-472f-8505-bc020d822ab1" />
