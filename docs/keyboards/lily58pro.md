# Lily58 Pro

Available at: https://keyhive.xyz/shop/lily58

![Lily58 PCBs](https://user-images.githubusercontent.com/6285554/51967194-0947f480-24b2-11e9-860f-e45197cf0983.jpg)

## Required parts

| Part                  | Qty | Description                                                              |
| --------------------- | --- | ------------------------------------------------------------------------ |
| Lily 58 PCB           | 2   | PCBs are reversible                                                      |
| Lily 58 plates        | 1   | 2 switch plates, 2 bottom plates                                         |
| Pro micro             | 2   |                                                                          |
| Switches              | 58  | Either MX or choc switch                                                 |
| Kailh hot swap socket | 58  |                                                                          |
| Diodes 1N4148W        | 58  | throughhole diodes are not recommended due to a footprint error          |
| Tactile switch        | 2   | 6x3x2 right angle tactile switch                                         |
| TRRS jacks            | 2   |                                                                          |
| M2 Standoffs          | 10  | Choc: 4 mm, MX: 7 mm. Also known as spacers                              |
| M2 screw              | 28  | 6mm is ideal                                                             |
| TRRS cable            | 1   | Cable for 3.5 mm audio, also called AUX cable (4-pole cable recommended) |
| Micro USB Cable       | 1   |                                                                          |
| OLED module           | 2   |                                                                          |
| Keycaps               | 58  | 56 1u keys, 2 1.5u keys for the thumb keys                               |

## Instructions

1. Solder
   - [diodes](#solder-diodes)
   - [hot swap sockets](#solder-hot-swap-sockets)
1. [Flash controller](#flash-controller)
1. [Solder controller](#solder-controller)
1. [Solder the reset button](#Solder-reset-button)
1. [Test the keyboard](#test-the-keyboard)
1. [Solder OLEDs](#solder-oleds)
1. [Solder TRRS jacks](#solder-trrs-jacks)
1. [Install OLED cover](#install-oled-cover)
1. [Install switches](#install-switches)

## Solder diodes

Soldering diodes is relatively straightforward. Refer to [Soldering diodes](../basic/soldering-diodes.md) if you need further guidance.

![2019-01-26](https://user-images.githubusercontent.com/6285554/51967206-1238c600-24b2-11e9-9617-01d8755c5b7f.jpg)

## Solder Kailh hot swap sockets

Refer to [Soldering Kailh hot swap sockets](.../basic/soldering-diodes.md) if you need further guidance.

![Kailh hot swap sockets orientation](https://user-images.githubusercontent.com/6285554/57197682-3de1b580-6fa5-11e9-90b1-fca894e1e7d2.png)

## Flash controller

Flash the controller (pro micro, Elite C, nice!nano, etc) with the firmware. This ensures that the controller works completely **before** soldering it permanently to the board.

The default crkbd firmware does not have LEDs enabled so if you plan on having LEDs this would be the time to modify the firmware to enable it.

## Solder controller

Refer to [Soldering the controller](../basic/soldering-the-controller.md) if you need further guidance.

## Solder reset button

Insert into holes. Solder in place on the bottom side of the pcb.

## Test the keyboard

At this point it should function as a keyboard. When you plug it in, the on-board LEDs should turn on. Insert a switch into a hot swap socket and [test that a keycode is pressed](https://www.keyboardtester.com/tester.html). You might consider testing every key in case there are problems with the diodes or hot swap sockets.

After this, solder remaining components.

## Solder OLEDs

> If you've socketed the controller, also consider socketing the OLEDs else the controller will be trapped underneath it.

Solder the 4 jumper pads on the same side that the pro micro will be mounted on. DO NOT FORGET THESE; they will be very difficult to access after the pro micro is soldered into place.

![Image showing the 4 jumper pads bridged with solder](https://user-images.githubusercontent.com/6285554/53293031-d45c6280-380f-11e9-8f1c-1c167b27cfd3.jpg)

Insert headers into holes. Use electrical tape to secure in place while you solder the holes on the bottom side of the PCB.

> ⚠︎ The OLED is not required but **if you omit it, you must disable it in the firmware**. If you do not, you will experience "jittery" keystrokes as if some keys were lost while in transit. Disabling it in the firmware will fix this behavior.

## Solder TRRS jacks

Insert into holes. Solder in place on the bottom side of the pcb

![Image showing TRRS jacks held in place with tape](https://user-images.githubusercontent.com/6285554/51967628-2cbf6f00-24b3-11e9-96e6-8f003c53d57b.jpg)

## Install OLED cover

Install the 4 spacers into the holes just below the pro micro, screw from the bottom.

![](https://user-images.githubusercontent.com/6285554/51967859-c0913b00-24b3-11e9-966c-f3621ed398e5.jpg)

![](https://user-images.githubusercontent.com/6285554/48837829-c4288780-edc9-11e8-8efb-6714d8e68e92.png)

## Install switches

Install the standoffs onto the switch plates.

![](https://user-images.githubusercontent.com/6285554/51967395-912dfe80-24b2-11e9-9cc7-b4520063f36c.jpg)

![](https://user-images.githubusercontent.com/6285554/51967376-83787900-24b2-11e9-82a0-850556daccfc.jpg)

Insert switches into the plate. Begin by placing one on each of the corners of the PCB to give you some stability. Be cautious of bent pins when pushing the switch down. **Kailh Box and choc switches require a bit of force for installation**.

![](https://user-images.githubusercontent.com/6285554/51967840-b66f3c80-24b3-11e9-8f50-6d8d31fe85e5.jpg)
