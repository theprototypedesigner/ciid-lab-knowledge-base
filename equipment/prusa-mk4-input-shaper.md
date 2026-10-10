# Prusa MK4 Input Shaper

[← Back to the knowledge base](../README.md)

## Technical specifications

The Original Prusa MK4 is the successor of the Original Prusa i3 MK3S+. It introduces the Nextruder, a new direct drive extruder with a loadcell sensor that makes first layer calibration fully automatic: the nozzle itself works as the sensor, so there is no need to adjust the Z height by hand anymore. Since firmware 5.0.0 the MK4 supports **Input Shaper** and **Pressure Advance**, two features that make the printer roughly twice as fast as before while keeping the print quality.

- Build volume: 25 x 21 x 22 cm (9,84 x 8,3 x 8,6 in)
- 0,4 mm nozzle (easily changeable) for 1,75 mm filament
- Layer height from 0,05 mm to 0,30 mm
- Max nozzle temperature: 290 °C
- Max heatbed temperature: 120 °C
- Nextruder: direct drive extruder with a 10:1 planetary gearbox
- Loadcell sensor for fully automatic first layer calibration
- Automatic mesh bed levelling (only on the area where you print)
- Magnetic heatbed with removable PEI spring steel print sheets
- Filament sensor, power panic (resumes the print after a power outage)
- Connectivity: USB drive, Ethernet, Wi-Fi and NFC
- 3,5" colour screen

### What is Input Shaper?

When a printer moves fast, the frame and the print head vibrate. These vibrations show up on your prints as "ringing" or "ghosting": little waves repeated next to sharp corners or holes. Input Shaper measures at which frequencies the printer vibrates and adjusts the movements of the motors to cancel those vibrations out. Pressure Advance does something similar with the plastic: it compensates for the pressure inside the nozzle, so the printer extrudes the right amount of material when it speeds up or slows down.

In practice, this means you can print faster without the print looking worse.

## Software

[PrusaSlicer - Prusa3d.com - 3D printers by Josef Prusa](https://www.prusa3d.com/prusaslicer/)

## How to use the Prusa MK4 Input Shaper

1. Open PrusaSlicer and go to **Configuration > Configuration Wizard**.
2. In the list of printers, select the **Original Prusa MK4** with the **Input Shaper** profile and the nozzle size installed in the printer (normally 0,4 mm).
3. In the print settings menu you will see new profile names: **Speed** (fastest), **Structural** (stronger parts) and **Fast detail** (smallest layer height for the 0,4 mm nozzle).
4. Slice your model, save the `.bgcode` file on a USB drive and plug it into the printer.

A few things to keep in mind:

- Always slice with the **Input Shaper** profile of the MK4. A file sliced for another printer (for example the MK3S) will not print correctly, and the printer will warn you.
- Do not forget to choose the right filament profile, the speed and temperature settings depend on it.
- The printer calibrates the first layer by itself, so there is no "Live Adjust Z" step like on the MK3S.

## Other resources

- <https://help.prusa3d.com/tag/mk4>
- <https://help.prusa3d.com/article/input-shaper-core-one-mk4-s-mk3-9-s-mk3-5-s-xl-mini_451816>
- <https://help.prusa3d.com/article/printer-handbooks_125045>
- <https://help.prusa3d.com/downloads/mk4-family/firmware>
- <https://www.prusa3d.com/product/original-prusa-mk4s-3d-printer-5/>
