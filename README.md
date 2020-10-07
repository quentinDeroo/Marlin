# Mks-Robin-Nano-Marlin2.0-Firmware-for-Sapphire-pro

My version of MKS Marlin 2.0.7 for Sapphire Pro.
I updated the whole UI/UX with new icons and menus so it looks more modern. The interface is also faster which is especially important for tuning during printing.
It's configured for my modified version of Sapphire pro with an E3D V6 but it will work just fine with the stock hotend, just do a PID tuning.
Also it fixes the bed dimensions compared to the original Marlin 2.0 fork for Sapphire Pro (https://github.com/inib/Marlin/tree/2.0.X-SapphirePro-3.5TFT). Now it matches the Cura profile you can find here : https://github.com/Anisotropic/sapphire_pro_cura_profile

I tested it on tens of prints, no real issues so far. Please let me know if you find any.

Note that I removed the multi language so it's only available in english.

## Features
The firmware of Mks Robin Nano, based on [Marlin2.0.x](https://github.com/MarlinFirmware/Marlin)(The based version is based on Marlin2.0.7).

![Main menu](https://github.com/quentinDeroo/Marlin/tree/2.0.x/Images/main.jpg)
![Tools menu](https://github.com/quentinDeroo/Marlin/tree/2.0.x/Images/tools.jpg)
![Printing screen](https://github.com/quentinDeroo/Marlin/tree/2.0.x/Images/printing.jpg)

## Update firmware
Download the release and put the `Robin_nano35.bin` and the `assets` folder at the root of the SD card. 
When you boot the printer, it will update automatically.

## Build
As the firmware is based on Marlin2.0.x which is built on the core of PlatformIO, the buid compiling steps are the same as Marlin2.0.x. You can directly using [PlatformIO Shell Commands](https://docs.platformio.org/en/latest/core/installation.html#piocore-install-shell-commands), or using IDEs contain built-in PlatformIO Core(CLI), for example, [VSCode](https://docs.platformio.org/en/latest/integration/ide/vscode.html#ide-vscode) and [Atom](https://docs.platformio.org/en/latest/integration/ide/atom.html). VSCode is recommended.

The build results are in the `.pio\build\mks_robin_nano35` directory.

## About the gcode file preview
The images should be added to gcode file when slicing, and MKS has developed the [plugin for Cura](https://github.com/makerbase-mks/mks-wifi-plugin) to make it.

## About the image conversion
- Open [LVGL online image converter tool](https://lvgl.io/tools/imageconverter). 
- Open png or bmp images. (make sure it's 32 bits color depth)
- Enter the saved file name.
- Choose color format:True color.
- Choose file output format:Binary RGB565.
- Start conversion.
- Save bin file.
- Copy the converted bin file to the mks_pic folder.
- Copy the mks_pic folder to the SD card.
- SD card is connected to the motherboard, and you can see the update interface after powering on.

In the png_assets folder, I've put all the icons in png format, as well as the pdn (for paint.net) files containing all layers so you can modify them easily.


## Others functional configuration
Please refer to [MKS-Robin-Nano-V2 wiki](https://github.com/makerbase-mks/MKS-Robin-Nano-V2/wiki/Marlin_firmware).

## More information about the Robin Nano
Please refer to [MKS Robin Nano github](https://github.com/makerbase-mks/MKS-Robin-Nano).

