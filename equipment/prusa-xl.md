# Prusa XL

[← Back to the knowledge base](../README.md)

## Technical specifications

The Original Prusa XL is a large format CoreXY 3D printer. It can have from 1 up to 5 independent toolheads that the printer swaps automatically during a print, which means you can print with up to 5 different colours or materials (for example a model in PLA with soluble supports) without wasting much filament on purges. It uses the same Nextruder as the MK4, with a loadcell sensor for fully automatic first layer calibration.

- Build volume: 36 x 36 x 36 cm (14,17 x 14,17 x 14,17 in)
- 1 to 5 toolheads with automatic tool changing
- Quick-swap nozzles (0,4 mm by default, also 0,25, 0,6 and 0,8 mm) for 1,75 mm filament
- Max nozzle temperature: 290 °C
- Segmented heatbed: 16 tiles that only heat the area under your print, saving time and energy
- Removable double-sided satin print sheet
- Loadcell sensor for fully automatic first layer calibration
- Automatic tool offset calibration (the printer checks the position of each toolhead by itself)
- Input Shaper with a built-in accelerometer, calibrated at the factory
- Filament runout sensors and a nozzle wiper
- Connectivity: USB drive, Ethernet and Wi-Fi

### What is a toolchanger?

On most printers there is one nozzle, so to change colour the printer has to unload one filament and load another, throwing away plastic every time. The XL instead has several complete print heads parked at the back of the printer. When the print needs another colour or material, the printer leaves the current head in its dock and picks up the next one. Each head always keeps its own filament loaded, so changes are fast and clean.

## Software

[PrusaSlicer - Prusa3d.com - 3D printers by Josef Prusa](https://www.prusa3d.com/prusaslicer/)

## How to use the Prusa XL

1. Open PrusaSlicer and go to **Configuration > Configuration Wizard**.
2. Select the **Original Prusa XL** profile that matches the number of toolheads in the printer (for example the 5 toolhead version) and the nozzle size.
3. Load your model. If it has several parts, right click on each part and assign it an **extruder** (1, 2, 3...). Each extruder number is one toolhead of the printer.
4. Pick the filament profile for each extruder in the right panel.
5. Slice, save the `.bgcode` file on a USB drive and plug it into the printer.
6. Before printing, the printer shows a **tools mapping** screen: check that each colour in your file is assigned to the toolhead that actually has that filament loaded.

A few things to keep in mind:

- Multi-material prints use a **wipe tower**, a small tower printed next to your model to clean the nozzle after each tool change. Leave space for it on the bed.
- Big prints take a long time. Check the estimated print time in PrusaSlicer before you start, and ask if you are not sure about printing overnight.
- Make sure the print sheet is clean and correctly placed before starting, the bed is big and the first layer needs good adhesion everywhere.

## Other resources

- <https://help.prusa3d.com/product/xl>
- <https://help.prusa3d.com/tag/xl>
- <https://help.prusa3d.com/article/tools-mapping-xl_668277>
- <https://help.prusa3d.com/article/input-shaper-core-one-mk4-s-mk3-9-s-mk3-5-s-xl-mini_451816>
- <https://help.prusa3d.com/article/printer-handbooks_125045>
- <https://help.prusa3d.com/downloads/xl-family/firmware>
- <https://www.prusa3d.com/product/original-prusa-xl-assembled-single-toolhead-3d-printer/>
