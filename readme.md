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
The device will use an STM32 microcontroller, I2S DAC for audio output, 
and microSD card interface. The USB interface will be built in to the STM 
chip. A general layout is shown below:

![Hardware layout](./hardware/design/Hardware%20Diagram.svg)

## License
Hardware - CERN OHL v1.2
Software - MIT

