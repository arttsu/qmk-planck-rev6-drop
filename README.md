# Keymap for my Planck v6

Created via [QMK Configurator](https://config.qmk.fm).

## Usage

### 1. Set up qmk (see below)

### 2. Copy keymap.json

`cp keymap.json $QMK_FIRMWARE_PATH/keyboards/planck/keymaps/arttsu/keymap.json`

### 3. Flash to the keyboard

`qmk flash -kb planck/rev6_drop -km arttsu`

## Setting up QMK on Fedora

### 1. Install pip (if not already installed)

`sudo dnf install python3-pip -y`

### 2. Install qmk

`pip install qmk`

### 3. Install deps

```sh
sudo dnf install -y dfu-util \
                    avr-gcc \
                    arm-none-eabi-gcc-cs \
                    libusb1-devel \ # dep of dfu-programmer
                    avrdude \
                    arm-none-eabi-newlib \
                    avr-libc \
                    avr-binutils
```

### 4. Install [dfu-programmer](https://github.com/dfu-programmer/dfu-programmer)

### 5. Run `qmk setup`

### 6. Copy udev rules

See instructions in `qmk setup` output.

### 7. Reload udev rules

```sh
sudo udevadm control --reload-rules
sudo udevadm trigger
```
