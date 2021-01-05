# Lily58 Pro Build Guide [WIP]


## Required parts

|Part name | Quantity | Remarks | Photo |
|---------|----------- |---------- |------------|  
| Lily 58 PCB | 2 pieces ||
| Lily 58 case | 1 set 4 pieces ||
| ProMicro | 2 pieces |  ||
| Key switch (CherryMX, kailh choc) | 58 pieces | MX switch and choc switch use either exclusively ||
| Kailh Switch socket| 58 pieces | Necessary for key switch installation ||
| Key Caps | 58 pieces | 1.5U parts can be 1U ||
| Diodes 1N4148W | 58 pieces |||
| Tact switch | 2 pieces |||
| TRRS jacks | 2 pieces ||
| M2 Spacers | 10, 4 | Choc: 4 mm, MX: 7 mm ||
| M2 screw | 28 pieces |||
| TRRS cable | 1 cable | Cable for 3.5 mm audio, also called AUX cable (4-pole cable recommended) ||
| Micro USB Cable | 1 pcs | Magnet type recommended due to the low durability of the connector on the Pro Micro side ||
| OLED module | 2 pieces |||

## Introduction
  
The PCB is reversible with both of the PCBs being exactly the same.
![5](https://user-images.githubusercontent.com/6285554/51967194-0947f480-24b2-11e9-860f-e45197cf0983.jpg)
![unadjustednonraw_thumb_2ccb](https://user-images.githubusercontent.com/6285554/53638905-1d2a7600-3c6b-11e9-9a39-a121c9b407b6.jpg)


## Attach the diodes
The diodes provided are through hole but SMD works better (I didn't realize this until later). If you do SMD, be careful to only use one at a time because they get lost easily
![2019-01-26](https://user-images.githubusercontent.com/6285554/51967206-1238c600-24b2-11e9-9617-01d8755c5b7f.jpg)

All of the components are soldered to the **back/bottom side**.  

Solder with the diode wire always pointing in the direction of the triangle bar on the board display as shown in the following figure. If the direction is incorrect, the key will not respond.
![2019-02-28](https://user-images.githubusercontent.com/6285554/53542561-53300300-3b62-11e9-8b83-5758ce400491.png)

Apply preliminary solder (melt the solder a little on the substrate) on one pad of the PCB diode.
![2019-01-26](https://user-images.githubusercontent.com/6285554/51965724-cbe16800-24ad-11e9-8afc-17c5b8eebda8.jpg)

Then use tweezers to solder one side of the diode using pre-soldering to secure the diode.
![2019-01-26](https://user-images.githubusercontent.com/6285554/51967222-1cf35b00-24b2-11e9-9624-26ff45f7bc9b.jpg)
Then the other one is also soldered.  
  
When all diodes have been soldered, check for missing spots.
![2019-01-26](https://user-images.githubusercontent.com/6285554/51967226-1f55b500-24b2-11e9-93f5-2802156a4d10.jpg)

## Solder the sockets
The socket is mounted on the back side which is the same side as the diode.

As in the case of the diode, pre-solder on one side of the socket pad, place the socket, and hold it in place with tweezers and hand soldering. (Please be careful not to burn yourself when holding down by hand.)  
As the picture is MX socket, please install Choc socket on the lower side.
![socket](https://user-images.githubusercontent.com/6285554/57197682-3de1b580-6fa5-11e9-90b1-fca894e1e7d2.png)

For parts that require force, firmly solder both and check for freeness.  
![2019-01-26000000000](https://user-images.githubusercontent.com/6285554/5196230-2250a580-24b2-11e9-94ce-591746c49f50.jpg)


## Soldering the TRRS jacks and reset switches
Mount on the surface (the one with the sticker on the mark).  
Attach the parts and fix them temporarily with masking tape. Turn over the board, solder it by making sure that the TRRS jack and reset switch do not float from the board.
![2019-01-2600000](https://user-images.githubusercontent.com/6285554/5196762-2c26d880-24b3-11e9-9764-aa51975c1eef.jpg)
![2019-01-26000000000000](https://user-images.githubusercontent.com/6285554/51967628-2cbf6f00-24b3-11e9-96e6-8f003c53d57b.jpg)


## Attach the OLED
Solder and jumper the four jumper terminals in the ProMicro section of the surface.
Attach the connector for OLED. Do not pour a lot of solder, as it is easy for solder to flow into the connector.
![unadjustednonraw_thumb_2db2](https://user-images.githubusercontent.com/6285554/53293031-d45c6280-380f-11e9-8f1c-1c167b27cfd3.jpg)

Insert the OLED pin into the socket, place the OLED module on it, and solder four places.

## Install Pro Micro  
The pin header enclosed in the bag of ProMicro is not used. In the case of a kit purchased at a playhouse studio, a spring pin header is included, so use that.  
![IMG_2662](https://user-images.githubusercontent.com/6285554/57210525-f5171480-7017-11e9-9d92-3a345d53db94.jpg)  
When attaching with a spring pin header (con-through), solder it according to the method described in the [Helix build guide](https://github.com/MakotoKurauchi/helix/blob/master/Doc/buildguide_jp.md#pro-micro) and then attach it to the Lily 58 PCB.

**Check the lines marked on the PCB and insert it into the PCB**. Please be careful as the place to insert the ProMicro is different for the left and right PCBs.

![ProMicro_PCB](https://user-images.githubusercontent.com/6285554/4891967-6a599a80-ed94-11e8-8e5d-6a6abca326a7.png)


## Attach the spacers
Attach four 10 mm round spacers to the holes near ProMicro.  
It is easy to insert a screw from the back of the board and attach the spacer from the top.
![2019-01-26000](https://user-images.githubusercontent.com/6285554/51967859-c0913b00-24b3-11e9-966c-f3621ed398e5.jpg)

The masking tape for the front and back identification applied first is peeled off here.

## Attach the key switches
Attach the top plate spacer for alignment. (MX: 7 mm Choc: 4 mm)
![2019-01-260](https://user-images.githubusercontent.com/6285554/51967395-912dfe80-24b2-11e9-9cc7-b4520063f36c.jpg)
![2019-01-2600](https://user-images.githubusercontent.com/6285554/51967376-83787900-24b2-11e9-82a0-850556daccfc.jpg)  

Attach four key switches to the top plate. (In the case of Choc, 2 places may be easier to install)
![2019-01-26 14 58 48] https://user-images.githubusercontent.com/6285554/5196380-87a49680-24b2-11e9-80b9-a45564afc8cf.jpg)

  
Insert the switch into the board for alignment, and align it.  
![2019-01-26 15 01 12](https://user-images.githubusercontent.com/6285554/51967478-c3d7f700-24b2-11e9-9f2f-4e75efc215a1.jpg)


After confirming that there are no bends in the switch pins or other issues, you can attach it firmly starting in the middle row then attach it outward.
  
**Be careful because the Kailh BOX switcs and Choc switchs require a bit of force for installation**.  
After installation, push the switch again to make sure that the keys are fully seated and the switches operate correctly.

![2019-01-26 15 10 06](https://user-images.githubusercontent.com/6285554/51967840-b66f3c80-24b3-11e9-8f50-6d8d31fe85e5.jpg)

## ProMicro Protective Acrylic Installation
Peel off the acrylic protective paper for ProMicro upper part and attach it.  
**Mount with the wider side outwards, towards the edge of the PCB**. Screw in the top plate
![top plate](https://user-images.githubusercontent.com/6285554/48837829-c4288780-edc9-11e8-8efb-6714d8e68e92.png)

![2019-01-26 15 21 15](https://user-images.githubusercontent.com/6285554/51968422-b8d19680-24b3-11e9-8402-85180ce10403.jpg)

## Write a key map
You need to be ready to write a keymap. The steps assume that you have been introduced to the process. [Please refer to the official page of QMK](https://docs.qmk.fm/#/getting_started_build_tools) if you are unfamilliar 
Required tools:
* **Windows**: [MSYS2](https://www.msys2.org)
* **Mac, Linux**: [avrdude](https://www.nongnu.org/avrdude)

By using QMK Toolbox, there is no need to build an environment, and writing the keymap can be performed using a GUI. (It is recommended to build the above writing environment when customizing)
[qmk / qmk_toolbox](https://github.com/qmk/qmk_toolbox/releases)  

 
Execute the following in the folder hierarchy of qmk_firmware to write the default key map of Lily 58

```bash
sudo make lily58:default:avrdude  
```

When `Detecting USB port, reset your controller now ...` is displayed, press the reset button on the keyboard to start writing.  
Please write to the other keyboard in the same way as above. 

The Default key map is as follows.  
Since the key map layout is made on the assumption that it is used in the macOS / US keyboard environment, try creating a key map that matches the user, such as adding a key map such as changing to the JIS array or switching between English and Kana. The best of my own keyboard.  
![lily58_default](https://user-images.githubusercontent.com/6285554/47273241-38ee8300-d5cc-11e8-9099-10c1b35e24fc.png)

## Operation check
Connect the left and right with a TRRS cable, connect the MicroUSB cable to ProMicro on the left side (in the case of the default key map), and check if the key responds.  
It is completed by attaching four rubber feet to the back. Thank you for your hard work.
![2019-01-26 15 24 52](https://user-images.githubusercontent.com/6285554/51967992-24b3ff00-24b4-11e9-8cd3-1e679094682f.jpg)
![unadjustednonraw_thumb_2ddc](https://user-images.githubusercontent.com/6285554/53640050-6203dc00-3c6e-11e9-9434-5591ed3e414f.jpg)


## Troubleshooting
### Q: One column (multiple columns) or one row (multiple rows) key switch does not respond
A:ProMicro may not be soldered and attached firmly. Check again, and re-solder and install if necessary.

### Q: The key switch does not respond alone
A. There may be a problem with the key switch insertion, socket or diode soldering. Inspect the switch, diode, and socket to determine which is causing the problem.

In the case of key switch insertion, after removing the key switch once make sure that there is no bending of the pin and then push it in again to install it.

In the case of socket soldering, re-solder the soldering point of the problem socket and pour the solder if necessary.  
  
In the case of diode soldering, check the direction of the diode in question. If it is wrong, remove it and re-solder it.
If the contacts are not fully soldered, please re-solder.

### Q. A symbol different from the symbol input by "@" or "[" etc. is input (Windows etc.)
Since recognition of keyboard is recognized as JIS keyboard on OS, another symbol will be input when inputting with Lily 58 (treated as US keyboard).  
Please set Lily 58 as a US keyboard in the keyboard setting of OS. After switching, switching to Japanese input becomes the switching key for the US keyboard, and it differs from the JIS keyboard, so please be careful (it can be customized with the key map etc.).


**If you have any problems, please feel free to send a message to the "# Lily58" channel on Discord ("Self-Made Keyboards in Japan" (https://discordapp.com/invite/NM7XtDW)) or Twitter: @F_YUUCHI**

## Change the key map
The self-made keyboard is operating using QMK firmware used above.  
The QMK firmware is highly customizable, and you can customize it with very high functionality simply by editing the key map.
### Edit keymap.c and customize
When customizing key map, copy the folder `qmk_firmware/keyboards/lily58/keymaps/default` to any new name. Here we use `my_keymap` for example:
```bash
cd qmk_firmware/keyboards/lily58/keymaps
cp default my_keymap
```
Modify the internal keymap.c accordingly.  
Please refer to the following [official QMK documentation](https://docs.qmk.fm/#/keycodes) for the key codes.

After changing the key map, re-compile KMK using the new keymap:

```bash
sudo make lily58:my_keymap:avrdude  
```
If you get an error, please check the [KMK firmware tutorial](https://docs.qmk.fm/#/newbs).  
  
### How to customize using QMK Configurator (deprecated)
If you use [QMK Configurator](https://config.qmk.fm/#/lily58/rev1/LAYOUT), you can create an original keymap on the browser without editing the keymap.c file.  
Load the downloaded json file into the QMK Toolbox and write it.
