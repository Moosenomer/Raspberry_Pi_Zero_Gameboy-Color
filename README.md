# Gameboy-Color-Raspberry-Pi-Mod

## Description & Background Info
A github page to highlight the Raspberry Pi Zero W portable emulator in a Gameboy color shell.
This project has been in the works for years, and the final result is a functional portable emulator and computer!

## Features of the Project
- Full support for GameBoy, Gameboy Color, NES, SUPER-NES and other retro game consoles with RetroPi
- 2.2 inch TFT display overclocked and tweaked for 60fps gameplay
- Original Gameboy Shell
- 2500 mA battery 
- Replica Gameboy controller PCB for use with original GameBoy buttons
- Adafruit 2.5W Mono amp paired with headphone jack and 1W Speaker
- Project Cost was ~135 Canadian Dollars (100USD)

## Be Warned...
This guide includes general assembly tips, but is not a full guide as I don't have the resources to effectively guide someone through ever step of construction (due to lack of foresight and time constraints). Believe in yourself, accept you will make mistakes and it turn out just fine!

## Acquiring Hardware
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
In order for the Raspberry Pi to function as expected with the TFT display there are some software tweaks that need to be preformed after installing RetroPie (can be found here).


## "Dry" Test
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