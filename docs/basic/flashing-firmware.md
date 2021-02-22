# Flashing firmware

## QMK

QMK is a very popular keyboard firmware that is widely supported and has many great features. This is the recommended firmware for controllers that are not wireless. Your best resource will be to follow the official QMK documentation and we've included links below for convenience.

- [Setup your QMK environment](https://docs.qmk.fm/#/newbs_getting_started)
  - [QMK Toolbox](https://docs.qmk.fm/#/newbs_flashing?id=flashing-your-keyboard-with-qmk-toolbox) is a helper tool to flash your keyboard with but we've experienced many issues with it such that we **do not recommend it** and **will not provide support** for it. The qmk-cli is the most reliable way to flash a keyboard.
- [Build your firmware](https://docs.qmk.fm/#/newbs_building_firmware)
- [Flash the firmware](https://docs.qmk.fm/#/newbs_building_firmware?id=flash-your-firmware)

See also:

- Join the [QMK Discord server](https://docs.qmk.fm/#/support?id=realtime-chat) to ask specific questions.

## ZMK

ZMK is a nacient keyboard firmware that aims to reach feature parity with QMK while also supporting Bluetooth enabled controllers. It should be noted that the firmware is under active development and might change drastically in the future. Your best resource will be to follow the official ZMK documentation and we've included links below for convenience.

- [Setup your ZMK environment](https://zmkfirmware.dev/docs/user-setup#installing-the-firmware) by following the official ZMK documentation.
- [Download the firmware files](https://zmkfirmware.dev/docs/user-setup#download-the-archive)
- [Flash the .uf2 files](https://zmkfirmware.dev/docs/user-setup#flashing-uf2-files)

Helpful resources:

- [Workaround for MacOS BLE stack problems](https://github.com/zmkfirmware/zmk/issues/278)
- LEDs cause battery drain even if not enabled (known as "LED leak") causing poor battery life
    - This is a known issue in ZMK which should be resolved once [zmkfirmware/zmk#156](https://github.com/zmkfirmware/zmk/pull/516) is merged
    - Another solution is to add a hardware on/off switch connected to the battery wires to manually cut power
        - We do not currently provide instructions on how to do this but may in the future; you will have better luck asking in the ZMK Discord for assistance
        - Those who have achieved this have used:
          - Slide toggle switch ([Digikey](https://www.digikey.com/en/products/detail/e-switch/EG1201A/101723?utm_adgroup=Slide%20Switches&utm_source=google&utm_medium=cpc&utm_campaign=Shopping_Product_Switches_NEW&utm_term=&utm_content=Slide%20Switches&gclid=CjwKCAiAyc2BBhAaEiwA44-wW1u_PQGDGa_oh8w2mr0ynfvmBrpdQYzDDGVepTo7V-kk-DTQPDkUxxoCWQIQAvD_BwE), [AliExpress](aliexpress.com/item/32848360942.html))   
          - AS11AH ([Mouser](https://www.mouser.com/ProductDetail/NKK-Switches/AS11AH/?qs=MODAV37v1mDLjalye5Scdw%3D%3D), [Digikey](https://www.digikey.com/en/products/detail/nkk-switches/AS11AH/2103411), ~$4/switch)
          - MSK12C02-HB ([LCSC](https://lcsc.com/product-detail/Toggle-Switches_SHOU-HAN-MSK12C02-HB_C431541.html))
          - [Switched JST Breakout Board](https://www.adafruit.com/product/1863) from Adafruit
        - This is also useful for those who travel and store their keyboards where the keys might get activated
- Toggling certain behaviors such as RGB only works on one side
    - [Open PR to invoke behaviors with different locality](https://github.com/zmkfirmware/zmk/pull/547). Once merged, this behavior should work as expected
    - A simple workaround is to add the keycode to both sides to toggle RGB
- OLEDs and RGB together have some known issues. 
    - We've enabled them by default to verify that the hardware works but you might consider disabling them in whatever combination suits your needs
    - ["I don't recommend using RGB and OLED together w/ ZMK at all yet." as of 01/29/2021](https://discord.com/channels/719497620560543766/781271311455748136/804791061641035834)
 - [nicekeyboards also recommends BlueMicro firmware](https://docs.nicekeyboards.com/#/wireless_firmware/) if you would like to try a different option. Note that there are some trade-offs between the two firmwares!

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
