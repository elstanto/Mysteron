# Mysteron - Scheduled radio playback device (WIP)
Useful for amateur radio foxhunts and numbers stations, among other nefarious 
uses, this device will connect to standard VHF/UHF radios and generate audio 
according to a schedule or other triggers.

## Features
* It will playback samples from a microSD card, and generate tones.
* It will read a script file from the microSD and load all triggers from it.
* It will have a USB COM interface to edit the script and live trigger.
* The USB COM interface will be tested on an Android phone as well as PC.
* A real-time clock will be used for accurate time triggers.
* An LED or two will show power and audio output status.

## Hardware
The device will use an STM32 microcontroller, built-in DAC for audio output, 
and microSD card interface. The USB interface will be built in to the STM 
chip. A general layout is shown below:

![Hardware layout](./hardware/design/Hardware%20Diagram.svg)

An Adafruit STM32F405 Feather has been purchased for testing, as it appears 
this board has all of the requirements in a compact and cheap form factor.

## Firmware
The Mysteron firmware will ideally be written in Arduino, as it is most 
portable and wasy to understand due to abstraction through standard libs.
stm32duino will be used to try and implement this. It supports the high 
speed SDIO SD card interface.

## Software

Ideally the firmware will present a complete interface over serial port, 
so software is not required. However, to avoid typing in the field, an 
Android app may be developed to act as a GUI for the serial commands.

## License
Hardware - CERN OHL v1.2
Software - MIT

