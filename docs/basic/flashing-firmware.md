# Flashing firmware

## QMK

- [Setup your QMK environment](https://docs.qmk.fm/#/newbs_getting_started)
  - [QMK Toolbox](https://docs.qmk.fm/#/newbs_flashing?id=flashing-your-keyboard-with-qmk-toolbox) is a helper tool to flash your keyboard with but we've experienced many issues with it such that we **do not recommend it** and **will not provide support** for it. The qmk-cli is the most reliable way to flash a keyboard.
- [Build your firmware](https://docs.qmk.fm/#/newbs_building_firmware)
- [Flash the firmware](https://docs.qmk.fm/#/newbs_building_firmware?id=flash-your-firmware)

See also:

- Join the [QMK Discord server](https://docs.qmk.fm/#/support?id=realtime-chat) to ask specific questions.

## ZMK

Your best resource will be to follow the official ZMK documentation.

- [Setup your ZMK environment](https://zmkfirmware.dev/docs/user-setup#installing-the-firmware) by following the official ZMK documentation.
- [Download the firmware files](https://zmkfirmware.dev/docs/user-setup#download-the-archive)
- [Flash the .uf2 files](https://zmkfirmware.dev/docs/user-setup#flashing-uf2-files)

See also:

- [Setup local development environment](https://zmkfirmware.dev/docs/development/setup)
  - The "VS Code & Docker" setup is the easiest approach, for both beginners and experienced developers.
- [Troubleshooting](https://zmkfirmware.dev/docs/troubleshooting/)
- Join the [ZMK Discord server](https://zmkfirmware.dev/community/discord/invite) to ask specific questions.

# FAQ

## Can I reverse engineer a .hex file?

No. These are compiled binary and there is no way to reverse them back into code. You will need to find the original files that were used to generate the hex file.

## I can't get my controller to be detected. What do I do?

A few possible issues and solutions are:

- Use a different cable.
- Use a different usb port.
- Use a usb port connected directly to the computer rather than a USB hub or dock.
- Be sure you're resetting your controller correctly.
  - Ensure that you're shorting the correct pins on the pro micro or nice!nano.
  - Some variants of the pro micro and the nice!nano require a quick double-tap of the reset pin before it enters bootloader mode.
- If using Windows, its almost always a drivers issue. Read QMK's documentation on [Bootloader Driver Installation with Zadig](https://docs.qmk.fm/#/driver_installation_zadig?id=bootloader-driver-installation-with-zadig).
- Some controllers are simply dead-on-arrival. Try another controller.

## Everything but a key/column/row works.

That sounds more like a hardware issue. See our [hardware troubleshooting documentation](../troubleshooting.md#A-column-or-a-row-of-keys-do-not-respond)
