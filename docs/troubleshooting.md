# A column or a row of keys do not respond

Ensure that the controller is soldered and connected completely. Reflow the solder. Replace if necessary.

# A single switch does not respond

Check the following:

- diode is in the correct orientation
- diode is soldered completely
- hot swap socket is completely soldered
- the switch posts are not bent
- verify that the keymap isn't using a special key at that position (firmwares like QMK sometimes use non-standard/custom keycodes that cannot be detected)

# How can I flash my keyboard?

These guides focus on the hardware. Most keyboards sold on KeyHive use QMK firmware and the following resources are the most helpful:

- [QMK Newbs guide](https://docs.qmk.fm/#/newbs?id=the-complete-newbs-guide-to-qmk)
- [QMK testing and debugging](https://docs.qmk.fm/#/newbs_testing_debugging)

# Connecting/disconnecting the TRRS cable causes issues

The TRRS cable **should not be removed while either side is connected to USB**. The reason is that the TRRS wires pass power and data over to the second half, and connecting/disconnecting can potentially apply power to a pin that should not be powered. 

Some sync issues can be resolved easily by [resetting the EEPROM memory](https://docs.qmk.fm/#/ref_functions?id=wiping-the-eeprom-persistent-storage), disconnecting from USB, and then connecting again.
