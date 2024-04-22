# RGBDS Basic Template

This repository provides a basic template for Gameboy development using RGBDS. The `game.asm` file is the starting point for your Gameboy project.

This template is based on the example provided at [gbdev.io](https://gbdev.io/gb-asm-tutorial/part1/hello_world.html).

## Development Environment

The recommended development environment for this project is [Visual Studio Code](https://code.visualstudio.com/). This repository includes a preconfigured VSCode setup in the `.vscode` directory.

The following VSCode extensions are recommended for this project:

* [RGBDS Z80 Extension](https://marketplace.visualstudio.com/items?itemName=donaldhays.rgbds-z80): Provides support for `*.asm` files.
* [Emulicious Debugger](https://marketplace.visualstudio.com/items?itemName=emulicious.emulicious-debugger): Enables debugging of Gameboy games.

## Build Toolchain

The [RGBDS](https://rgbds.gbdev.io/) toolchain, which has been used for building Gameboy games in Assembly since 1996, is required for this project. You can install it using the following command (Mac users):

```shell
brew install rgbds
```

Additional installation information for other OSes can be found [here](https://rgbds.gbdev.io/install).

## Emulator

This project uses the [Emulicious](https://emulicious.net/) emulator. The emulator is included in this repository, so there is no need for additional downloads. However, you will need to install [JAVA](https://www.java.com/en/download/) to run it.

To enable remote debugging in Emulicious, navigate to `Tools` > `Remote Debugging` and enable it.

## Additional Files

This project includes the [hardware.inc](https://raw.githubusercontent.com/gbdev/hardware.inc/v4.0/hardware.inc) file, which serves as the standard library for Gameboy ASM.

You are not supposed to modify this file, but just import it in your code.

## Building the ROM

To build the project, press `Shift + Cmd + B`. This will execute the commands defined in the `.vscode/tasks.json` file.

This will create a `build` directory and place the ROM, named `game.gb`, inside it.

Please note that the build process expects a `game.asm` file as your source code.

## Debugging the ROM

To start debugging, press `Shift + CMD + D` and click the Play button for `Launch in Emulicious`.

## Playing the Game

To run the game, either manually run the ROM via an emulator or press `Ctrl + F5`.