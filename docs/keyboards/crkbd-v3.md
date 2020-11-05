# Crkbd v3

Available at: https://keyhive.xyz/shop/corne-v3

1. Solder
   - [diodes](#solder-diodes)
   - [hot swap sockets](#solder-hot-swap-sockets)
1. [Flash controller](#flash-controller)
1. Solder controller
   - [with headers](#with-headers)
   - [with sockets](#with-sockets)
1. [Test the keyboard](#test-the-keyboard)
1. Solder remaining components
   - [Underglow LEDs](#solder-underglow-leds)
   - [per-key LEDs](#solder-per-key-leds)
   - [OLEDs](#Solder-OLEDs)
   - [TRRS jacks](#Solder-TRRS-jacks)
   - [Reset button](#Solder-reset-button)

## Solder diodes

Diodes are fairly robust and they have polarity, which means that the orientation matters. The stripe on the diode should match the silkscreen on the PCB, like so: ![insert image]()

The simplest approach is to add a little bit of solder to one pad, place the diode and solder to one pad, make adjustments, and then solder the other pad.

## Solder hot swap sockets

Place the hot swap socket into the holes of the PCB. Solder one side, and then the other.

## Flash controller

Flash the controller (pro micro, Elite C, nice!nano, etc) with the firmware. This ensures that the controller works completely before soldering it permanently to the board.

The default crkbd firmware does not have LEDs enabled so if you plan on having LEDs this would be the time to modify the firmware to have it.

## Solder controller

Solder the controller to the PCB. Unlike previous versions, there is only one set of holes for the controllers to be soldered to.

### with headers

Insert the headers. Solder in place.

### with sockets

Insert the sockets. Solder in place. Cover with kapton or electrical tape. Poke holes in sockets using an LED leg, pick tool, or needle. Lay controller over sockets. Insert diode or LED legs in place, starting with just the 4 corner sockets. Clip to height. Solder in place. Insert remaining pins, clip, and solder.

## Test the keyboard

At this point it should function as a keyboard. When you plug it in, the on-board LEDs should turn on. Insert a switch into a hot swap socket and [test that a keycode is pressed](https://www.keyboardtester.com/tester.html). You might consider testing every key in case there are problems with the diodes or hot swap sockets.

After this, solder remaining components.

## Solder underglow LEDs

> (!) LEDs can be very temperature sensitive. Be careful. Consider setting your soldering to a low temp (about 200C), using a fine tip, adding flux, or using a hot air station.

Tin all the pads with a small bubble of solder, not too much. Place the 5050 LED on top and center. With some light pressure, hold the led in place while you flow the solder bubbles. I use an aluminum screwdriver which also acts as a heat sink to protect the LED. Test each LED as you go.

### Troubleshooting

If an LED pixel does not turn on, there are a few points of failure to verify:

1. Are all 4 pads properly soldered?
   - Reflow the solder, careful when applying heat
   - Add more solder
1. Is the LED damaged?
   - Replace the LED
1. Is the PCB damaged?
   - Review the WS2812B wiring, and create a jump that completes the circuit per the schematic

## Solder per-key LEDs

> (!) LEDs can be very temperature sensitive. Be careful. Consider setting your soldering to a low temp (about 200C), using a fine tip, adding flux, or using a hot air station.

Tin two pads on one side. Place the LED. Flow the solder on the tinned pads. Add solder to pads on other side. Test each LED as you go.

## Solder OLEDs

Insert into holes. Consider using electrical tap to secure in place while you solder the holes on the bottom side of the PCB.

## Solder TRRS jacks

Insert into holes. Solder in place on the bottom side of the pcb.

## Solder reset button

Insert into holes. Solder in place on the bottom side of the pcb.
