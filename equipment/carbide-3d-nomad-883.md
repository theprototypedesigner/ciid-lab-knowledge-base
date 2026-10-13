# Carbide 3D Nomad

[← Back to the knowledge base](../README.md)

## Technical specifications

The Nomad 3 is a desktop CNC milling machine made by Carbide 3D. A CNC mill works the opposite way to a 3D printer: instead of adding material layer by layer, it starts from a solid block and removes material with a spinning cutting tool (called an **end mill**). It is fully enclosed, so it is quieter and cleaner than most CNC machines, and small enough to fit on a table.

- Work area: 20,3 x 20,3 x 7,6 cm (8 x 8 x 3 in)
- 130 W brushless spindle, up to 24.000 RPM
- ER-11 collet for end mills with a 1/8" (3,175 mm) shank
- Fully enclosed, with a door interlock: if you open the door, the job pauses and the spindle stops
- BitSetter: built-in sensor that measures the length of each tool automatically, so you don't need to set the Z zero again after a tool change
- BitZero V2: touch probe to find the corner (X, Y and Z zero) of your material
- Weight: about 32 kg (70 lb)

It can cut:

- Hardwoods and softwoods
- Plastics like acrylic, Delrin (POM), polycarbonate, nylon, HDPE and PVC
- Modelling materials like Renshape, machinable wax and foams
- Soft metals like aluminium, brass and copper
- PCBs (the material must be very flat)

## Software

- [Carbide Create](https://carbide3d.com/carbidecreate/): design your part in 2D / 2.5D and create the **toolpaths** (the paths the end mill will follow). It exports a G-code file.
- [Carbide Motion](https://carbide3d.com/carbidemotion/): controls the machine. You use it to home the machine, change tools, set the zero point on your material and run the G-code file.
- [MeshCAM](https://www.meshcam.com/): creates toolpaths from 3D models (STL files), for shapes that are not flat, like a relief or a mould.

## How to use the Carbide 3D Nomad 3

Always wear safety glasses, and never leave the machine alone while it is cutting.

1. **Design and create toolpaths** in Carbide Create: set the size of your material, draw your shapes, choose the end mill and generate the toolpaths. Use the simulation to check the result, then save the G-code file.
2. **Connect and home**: turn on the machine, open Carbide Motion and click **Connect to Cutter**. With the door closed, click **Initialize Machine**. The machine moves to its home position (back right corner).
3. **Fix your material** to the wasteboard with double-sided tape, clamps or a vise. If the material moves while cutting, the job is ruined (and the end mill can break).
4. **Set the zero**: Carbide Motion will ask you to install the probing pin (a metal pin that goes in the collet instead of an end mill). Then place the BitZero probe on a corner of your material, attach its clip to the pin and run the probe in Carbide Motion. This tells the machine where your material is.
5. **Install the end mill** when Carbide Motion asks for it. Insert it at least 2 cm (0,75 in) into the collet and tighten the nut firmly. The BitSetter will measure it automatically.
6. **Run the job**: load your G-code file, close the door and click **Start**. Stay next to the machine and watch.
7. **Clean up**: when the job finishes, remove your part, vacuum the chips and dust inside the machine and put the tools back in their place.

A few things to keep in mind:

- Never tighten the collet nut without a tool inside, the collet can break.
- End mills are very hard but also brittle, handle them with care.
- If something sounds or looks wrong, open the door (the job pauses) or use the power switch to stop the machine.
- Wood dust and chips can catch fire, keep the machine clean.

When you are ready to start milling, these video tutorials will get you started with Carbide Create and Carbide Motion:

- [Design with Carbide Create (video course)](https://guides.carbide3d.com/create/)
- [Running a Shapeoko (video course)](https://guides.carbide3d.com/running-shapeoko/): made for another Carbide 3D machine, but Carbide Motion works the same way on the Nomad.

You can find more CNC learning resources on the [Maker resources](maker-resources.md#cnc-milling) page.

## Other resources

- <https://my.carbide3d.com/gettingstarted/nomad3/>
- <https://guides.carbide3d.com/files/pdf/Nomad3_Getting_Started_Guide_12_22_2020_v1_smaller.pdf>
- <https://guides.carbide3d.com/files/pdf/BitZero_V2_Nomad.pdf>
- <https://shop.carbide3d.com/products/nomad-3/>
- <https://community.carbide3d.com/>
