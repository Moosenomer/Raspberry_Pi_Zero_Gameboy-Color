# Gameboy-Color-Raspberry-Pi-Mod

# Description & Background Information
A github page to highlight the Raspberry Pi Zero W portable emulator in a Gameboy color shell.
This project has been in the works for years, and the final result is a functional portable emulator and computer! 

Instead of this being a step by step guide I have designed this document to provide you with most of the required documentation and guides so that you can complete the project yourself and helpfully learn a lot too. My best advice is to throw yourself into something, set a ridged completion date and work towards it. That way a project (like this one) one take you 4 years (like it took me) and you'll finish the project no matter if its your best work or not.
# Features of the Project
- Full support for GameBoy, Gameboy Color, NES, SUPER-NES and other retro game consoles with RetroPi
- 2.2 inch TFT display overclocked and tweaked for 60fps gameplay
- Original Gameboy Shell
- 2500 mA battery 
- Replica Gameboy controller PCB for use with original GameBoy buttons
- Adafruit 2.5W Mono amp paired with headphone jack and 1W Speaker
- Project Cost was ~135 Canadian Dollars (100 USD)

# Acquiring Hardware
### Crucial Components
1. Buy a Gameboy Color Shell. There are plenty of broken Gameboys available on ebay that ship internationally, and plenty of shells that are inexpensive on Aliexpress. Please don't break a perfectly operational Gameboy, that would break my heart.
2. Source a Raspberry Pi Zero W. Best sites are smaller electronics retailers, especially in Canada. I used PiShop to purchase mine.
3. The 2.2 Inch ili9341 TFT display was sourced from Aliexpress, non touch versions of these boards are ideal since they have better colors. They can be found on similar sites as well, buy at own risk!
4. Adafruit PowerBoost 1000. Check website for availability, we will be likely drawing close to 500mA at max load so its worth purchasing this over the PowerBoost 500.
5. Adafruit D class 2.5W Mono Amp. Any mono amp works, this is just what was easy to source (and had documentation).
6. SD card, 32GB or larger. The Pi zero is only capable of emulating NES, Gameboy and GBA titles well which don't have large file sizes so don't worry too much. Larger is better, and a good quality card should be used for longevity and performance.
7. Battery, 2500mAH 3.7V LiPo. The larger the battery the better, in this build I 3D printed a custom cartridge to put the battery inside, this is not necessary however I can only guarantee this will work. The size I used is roughly (4.6cm x 5.8cm x 0.5cm).
8. 1W, 8ohm Speaker, Headphone Jack, USB-C Breakout Board, LED. Source from wherever, a local retailer is always the best!
9. Capacitors (33nF, 10uF), Resistors (270ohm, 150ohm x2, ~420ohm). Since these are used to create a filter, use good quality components if possible, I didn't because of interesting life choices.

### Not So Obvious Components
1. Wire. Lots of it. I used 22 AWG wire however it was not solidcore. This made assembly a royal pain in the ass as every connection need the stranded wire to be compromised in order to create reliable solder joints. Also two different colours really help with assembly, and personally I believe the aesthetic is nice.
2. Heat-shrink tubing, while not required it comes in handy during final assembly when some wires need to be shorter or longer in some sections.

## Tools
- Multimeter: Verify continuity and troubleshoot circuits.
- Soldering Iron with a Fine tip: I did not have this prior to doing some of the assembly, it improved my solder joints significantly. 
- Wire Strippers: Useful since you'll be manipulating many wires.
- Fine tip Needle Nose Pliers or Tweezers: You will drop things, or need to adjust very small things especially come final assembly
- Dremel Tool with Varying Bits: To remove the parts of the original shell that interfere with the installation of other components.
- Utility knife: Cutting small PCB boards 
- Screwdriver (Tri-wing Y Tip, Very small slotted screwdriver)
- Micro USB Power adaptor: For testing the pi and its functionality before the battery or charging system is installed.
- Helping Hands: More hands = Better

That should be all the tools I deemed useful while finishing this project. How well talk about the prep work that should be done before final assembly.
# PREP WORK
## Raspberry Pi Zero Setup
After flashing Retropie to the SD card, create the ==wpa_su== file in the root of the SD Card and add a network so that the pie can be managed remotely Via SSH Client.

Now its time to install dependencies and libraries, at this point you should have a Pi running headless, and accessing it over SSH. 
## ILI-9341 Driver Build
In order for the Raspberry Pi to function as expected with the TFT display there are some software tweaks that need to be preformed. In Resources used section there is a fantastic video by EmulatedBen.

In summary after cloning the ili-9341 driver files, you need to build it with custom commands that suit your specific needs. In my build the command that I used to build the driver is listed, the main things are that it has are optimizations for the pi-zero and 60fps capability.

## Adafruit Retrogame
Adafruit Retrogame is a great utility to help you manage keyboard inputs using GPIO pins. It works great with Retropie and the availably documentation is tailored to this use case. After installing make sure you have an idea how your going to wire the button controls, it technically wont matter since you will be mapping all the keys in emulation station anyways. 
The guide on the Adafruit website should be all you need to get going!
[Installing Retrogame | Retro Gaming with Raspberry Pi | Adafruit Learning System](https://learn.adafruit.com/retro-gaming-with-raspberry-pi/adding-controls-software)

## GPIO Pins
In order to change the default pin modes, were going to utilize __

## ALSA Mixer settings and configuration tweaks
In order to get the raspberry pi zero to output over pins __ and, you need to add some text to config.txt and alter some settings in the raspberry pi configuration. 

## Test Drive
Before even thinking about installing everything into the shell, we need to make sure that mostly all the major components work as expected and that crucial software features also work.
In this test I will be using all these components simultaneously:
- Raspberry Pi Zero
- Controller Board
- PowerBoost 1000
- Battery
- TFT Display

I bought these components with pins pre soldered or I soldered them myself to use on a modular breadboard. All the components were connected using jumper wires, and the Pi was powered using a USB-A to USB-Micro B cable. 

[picture here?]

# Assembly
........ Documentation is a work in progress, were getting there




# Resources Used
Please Take some time to visit these amazing sites that I used to learn & troubleshoot issues as I completed this project, some great guides and some things that you might find useful as well.


Important Guides
[Retropie SPI ili-9341 screen 30 fps+ tutorial - YouTube](https://www.youtube.com/watch?v=6C1kVnGUAY0&ab_channel=EmulatedBen)
[Raspberry Pi Zero Sound Output – Bytes N Bits](https://bytesnbits.co.uk/raspberry-pi-zero-analog-sound/)
[(697) cheap 2.8 inch ili-9341 SPI screen retropie 60 FPS Juj method tutorial - YouTube](https://www.youtube.com/watch?v=r1J0Hd-abVA&t=490s)
[ili9341 tft screen guide - RetroPie Forum](https://retropie.org.uk/forum/topic/7464/ili9341-tft-screen-guide)
[juj/fbcp-ili9341: A blazing fast display driver for SPI-based LCD displays for Raspberry Pi A, B, 2, 3, 4 and Zero (github.com)](https://github.com/juj/fbcp-ili9341)
[NeonHorizon/lipopi: Guide to setting up LiPo batteries on the Raspberry Pi (github.com)](https://github.com/NeonHorizon/lipopi)
[Installing Retrogame | Retro Gaming with Raspberry Pi | Adafruit Learning System](https://learn.adafruit.com/retro-gaming-with-raspberry-pi/adding-controls-software)

Custom Controller Guide
[(701) retropie - how to connect and configure GPIO buttons to raspberry Pi 3 using GPIOnext - YouTube](https://www.youtube.com/watch?v=R-wAcP6wVTc)

Guides
[How to Add a Power Button to Your Raspberry Pi - Howchoo](https://howchoo.com/pi/how-to-add-a-power-button-to-your-raspberry-pi/)
[How to Transfer Files to the Raspberry Pi - Howchoo](https://howchoo.com/pi/how-to-transfer-files-to-the-raspberry-pi/)
[Circuit Diagram | Mini Raspberry Pi Handheld Notebook | Adafruit Learning System](https://learn.adafruit.com/mini-raspberry-pi-handheld-notebook-palmtop/circuit-diagram)
[Overview | Adding Basic Audio Ouput to Raspberry Pi Zero | Adafruit Learning System](https://learn.adafruit.com/adding-basic-audio-ouput-to-raspberry-pi-zero/overview)
[How to Clone Your Raspberry Pi SD Card for Foolproof Backup (howtogeek.com)](https://www.howtogeek.com/341944/how-to-clone-your-raspberry-pi-sd-card-for-foolproof-backup/)
[gpio - Automatic shutdown of Pi Zero on low battery - Raspberry Pi Stack Exchange](https://raspberrypi.stackexchange.com/questions/42946/automatic-shutdown-of-pi-zero-on-low-battery)
[Audio Output from a Raspberry Pi Zero (Shallow Thoughts) (shallowsky.com)](https://shallowsky.com/blog/hardware/pi-zero-audio.html)
[raspberry-gpio-python / Wiki / BasicUsage (sourceforge.net)](https://sourceforge.net/p/raspberry-gpio-python/wiki/BasicUsage/)
[(697) RetroPie 3.5 inch SPI display HIGH FPS (FBCP - iLi9341) - YouTube](https://www.youtube.com/watch?v=xOPVlq4kM9c)
[Adding a Shutdown Button to the Raspberry Pi B+ - element14 Community](https://community.element14.com/products/raspberry-pi/raspberrypi_projects/w/documents/856/adding-a-shutdown-button-to-the-raspberry-pi-b)

KICAD Guides
[Getting Started in KiCad | 6.0 | English | Documentation | KiCad](https://docs.kicad.org/6.0/en/getting_started_in_kicad/getting_started_in_kicad.html#tutorial_part_4_custom_symbols_and_footprints)
[Tutorial: How to make a symbol -FAQ - KiCad.info Forums](https://forum.kicad.info/t/tutorial-how-to-make-a-symbol-kicad-v5-1-x/13336/3)
[Kicad 6 missing symbols/footprints - Electrical Engineering Stack Exchange](https://electronics.stackexchange.com/questions/650961/kicad-6-missing-symbols-footprints)

Generally Useful
[Raspberry Pi GPIO Pinout- pinout.xyz](https://pinout.xyz/pinout/ground)

Relevant Troubleshooting Forums
[No soundcards found on Pi Zero - Raspberry Pi Forums](https://forums.raspberrypi.com/viewtopic.php?t=294710)
[alsa sound and alsamixer - Raspberry Pi Forums](https://forums.raspberrypi.com/viewtopic.php?t=7663)
[failed to find mixer elements - RetroPie Forum](https://retropie.org.uk/forum/topic/11256/failed-to-find-mixer-elements/22)
[Resetting controller configuration - RetroPie Forum](https://retropie.org.uk/forum/topic/5069/resetting-controller-configuration/2)

Overclocking Guide (not recommended)
[raspi-documentation/configuration/config-txt/overclocking.md at master · RealVNC/raspi-documentation (github.com)](https://github.com/RealVNC/raspi-documentation/blob/master/configuration/config-txt/overclocking.md)
[RetroPie: Improving Emulator Performance | Retro Gaming with Raspberry Pi | Adafruit Learning System](https://learn.adafruit.com/retro-gaming-with-raspberry-pi/retropie-improving-emulator-performance)


# Thanks
If you've made it this far, thank you. A lot went into this project, and I'm hoping that what I have been able to provide in this document is enough to get you started making something awesome.

Cheers!