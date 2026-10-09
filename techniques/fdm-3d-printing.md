# FDM 3D printing

[← Back to the knowledge base](../README.md)

Fused Deposition Modeling (FDM), is an additive manufacturing process that belongs to the material extrusion family. In FDM, an object is built by selectively depositing melted material in a pre-determined path layer-by-layer. The materials used are thermoplastic polymers and come in a filament form.

FDM is the most widely used 3D Printing technology, it represents the largest installed base of 3D printers globally and is often the first technology people are exposed to.

When designing parts that's going to be printed using FDM keeping in mind the capabilities and limitations of the technology will help you achieve the best result

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/intro-fdm-3d-printing/2-fdm-steps.png)

# How does FDM work?

Here is how the FDM fabrication process works:

1. A spool of thermoplastic filament is first loaded into the printer. Once the nozzle has reached the desired temperature, the filament is fed to the extrusion head and in the nozzle where it melts.
2. The extrusion head is attached to a 3-axis system that allows it to move in the X, Y and Z directions. The melted material is extruded in thin strands and is deposited layer-by-layer in predetermined locations, where it cools and solidifies. Sometimes the cooling of the material is accelerated through the use of cooling fans attached on the extrusion head.
3. To fill an area, multiple passes are required, similar to coloring a rectangle with a marker. When a layer is finished, the build platform moves down (or in other machine setups, the extrusion head moves up) and a new layer is deposited. This process is repeated until the part is complete.

![](https://f.3dhubs.com/pBf6WNqrpF9eJJgE9wnSYc.png)

# Characteristics of FDM

## Layer Adhesion

Good adhesion between the deposited layers is very important for an FDM part. When the molten thermoplastic is extruded through the nozzle, it is pressed against the previous layer. The high temperature and the pressure re-melts the surface of the previous layer and enables the bonding of the new layer with the previously printed part.

**The bond strength between the different layers is always lower than the base strength of the material.**

This means that FDM parts are inherently anisotropic: their strength in the Z-axis is always smaller than their strength in the XY-plane. For this reason, it is important to keep part orientation mind when designing parts for FDM.

For example, [tensile test pieces](https://www.innofil3d.com/wp-content/uploads/2016/05/TDS-Innofil3D-ABS-160609.pdf) printed horizontally in ABS at 50% infill were compared to test pieces printed vertically and were found to have almost 4 times greater tensile strength in the X,Y print direction compared to the Z direction (17.0 MPa compared to 4.4 Mpa) and elongated almost 10 times more before breaking (4.8% compared to 0.5%).

Moreover, since the molten material is pressed against the previous layer, its shape is deformed to an oval. This means that FDM parts will always have a **wavy surface**, even for low layer height, and that small features, such as small holes or threads may need to be post-processed after printing.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/intro-fdm-3d-printing/7-fdm-side-layers_720.png)

Schematic of the FDM layer-by-layer construction

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/intro-fdm-3d-printing/6-fdm-sample-layers.jpg)

## Layer height

All 3D printing processes build parts layer-by-layer. Due to the additive nature of 3D Printing, the thickness of each layer determines the resolution of a print in a similar way that the number of pixels determines the resolution of a television or computer monitor. Lower layer height typically results in parts with smoother surfaces. The downside is that the lower the layer height the longer it takes to complete a print.

It is important for a designer to determine whether aesthetics (a smoother surface) or time (and cost) savings are more important.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/layer-height/photo5.jpg)

3 FDM parts printed at 50, 200 and 300 microns (left to right).

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/layer-height/photo6.jpg)

A macro view of the FDM prints (50, 200 and 300 microns from left to right) shown at the same scale for comparison.

### Why is layer height important?

Layer height is an important design parameter that impacts the printing time, cost, visual appearance and physical properties of a printed part.

Often the visual difference between parts printed at 100 μm and 200 μm is very small. However, the part at 100 μm will take twice as long to print, the 3D printer will have to trace twice as many cross-sections, and this will have an impact on the cost.

### When to choose a lower layer height?

Before selecting a layer height consider the following question:

- **Part geometry**: Does your 3D model have curved surfaces or holes?
- **Use case & application**: Is functionality or visual appearance the main design consideration?
- **Post processing**: Will the part be finished after 3D printing and before use?

### Curves and angles

The impact of layer height is more noticeable on curves and angles and is less prominent on straight vertical walls, due to the layer-by-layer nature of 3D printing.

For example, in order to print a hole along a horizontal axis, the printer software has to slice the circular hole into multiple layers and then stack them on top of each other, creating a non-smooth edge that looks like a staircase. This is called the stepping effect and becomes more prominent at surfaces with greater curvature.

If a design includes a significant number of curves, angles or hole using a lower layer height will result in a more accurate part.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/layer-height/6-sls-stepping.png)

The stepping effect becomes more prevalent in areas of larger curvature.

## Support Structure

Support structure is essential for creating geomentries with overhangs in FDM. The melted thermoplastic cannot be deposited on thin air. For this reason, some geometries require support structure.

Surfaces printed on support will generally be of lower surface quality than the rest of the part. For this reason, it is recommended that the part is designed in such a way to minimize the need for support.

Support is usually printed in the same material as the part. Support materials that dissolve in liquid also exist but are only available on our Ultimaker. Printing on dissolvable supports improves significantly the surface quality of the part, but increases the overall cost of a print, as specialist machine (with dual extrusion) are required and because the cost of the dissolvable material is relatively high.

### When is support needed in FDM?

With FDM printing, each layer is printed as a set of heated filament threads which adhere to the threads below and around it. Each thread is printed slightly offset from its previous layer. This allows a model to be built up to angles of 45°, allowing prints to expand beyond its previous layer’s width.

When a feature is printed with an overhang beyond 45°, it can sag and requires support material beneath it to hold it up.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/supports-3d-printing-technology-overview/visual1.png)

Depending on the degree of overhang, your FDM print might need support

### Bridging vs support

There is an exception to this rule:

Hot material can be stretched short distances between two points in a method known as bridging. Bridging allows material to be printed without support and with minimal sag. If a bridge is over 5 mm long, generally, support is required to give an accurate surface finish.

### The ABCs (or YHTs) of FDM support

Consider the letters Y, H, and T, and a set of associated 3D models.

- The arms of a model of the letter Y can be printed easily. Even though the arms the of Y are outstretched, because they extend at 45 degrees or less, they do not require support.
- The letter H is a little more complicated but if the center bridge is under 5mm, it can be printed without support or any sagging. Over 5mm and support will be required. For this example, the center bridge is over 5mm and support is needed.
- The letter T requires support for the arms of the letter. There is nothing for the outer arms to be printed on and the material will just fall down without support.

The image below illustrates YHT with the support material shown in light gray.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/supports-3d-printing-technology-overview/visual2.png)

Here is how the YHTs look when printed. The image below now shows the result of the T printed without support. The surface has significant sagging and will require a large amount of post-processing to clean up.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/supports-3d-printing-technology-overview/photo24.jpg)

Y, H, and T printed with FDM with support

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/supports-3d-printing-technology-overview/photo25.jpg)

The letter T fails when printed with FDM without any support structure

### The downside of FDM support material

One of the limitations of using support in FDM printing is that post-processing is always required, resulting in marks or damage to the surface in contact with the support.

Another issue is that layers printed upon support will be less perfect as the support will be slightly less stationary than the solid layers.

Support can also be difficult to remove from small, intricate features without breaking the model.

Furthermore, support requires additional printing material and therefore incurs additional costs. The support also needs removal, creating more work for the 3D printing service provider which can also increase the total cost of the print job.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/supports-3d-printing-technology-overview/photo27.jpg)

### How much support is needed for my FDM print?

The arch example below requires only a limited amount of support placed in the correct location to allow it to be printed accurately.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/supports-3d-printing-technology-overview/photo13.jpg)

## Importance of part orientation

Designers often overlook the importance that part orientation plays in the final quality of a 3D printed part. This article discusses how part orientation impacts the part accuracy, manufacturing time, strength and surface finish of your 3D printed parts and addresses the importance of build orientation by technology.

### Part accuracy

Consider a cylinder with a hole, 10 mm outer diameter, 6 mm inner diameter, 30 mm length, that is printed with FDM with its center axis vertical. The 3D printer would construct this part as a series of concentric circles layered on top of one another. This would produce a final cylinder with a relatively smooth outer surface.

If the same cylinder is reorientated with its center axis horizontally, the part will be built as a series of rectangles (with slightly different width) layered on top of each other. Also, the surface of the cylinder that touches the build platform will be flat, because the material would as the initial first layers were printed.

By orientating the part in different directions, there is a significant difference in the print quality, as can be seen in the photo below.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/print-orientation/photo2.jpg)

Two identical cylinders printed at the same layer height in different orientations — left: vertically, right: horizontally

### Build time

Orientation can also have a significant impact on print time.

Using as an example the cylinder of the previous section, the horizontal orientation will take significantly less time to print than the vertical, as the total number of layers is significantly reduced: at a 100 μm layer height, the horizontal cylinder will be printed with 100 total layers and the vertical with 300 layers. This can add up to significant time differences for large parts.

### Part strength

For functional parts, it is important to consider the application and the direction of the loads. For example, FDM parts are much more likely to delaminate and fracture when placed in tension in the Z direction compared to the XY directions up to 4-5 times difference tensile strength.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/print-orientation/visual2.png)

3D printing technologies generally are much stronger in one direction compared to another

Due to the anisotropic nature of FDM printing, understanding the application of a component and how it is built are critical to the success of a design. FDM components are inherently weaker in one direction due to layer orientation.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/key-design-considerations-fdm-3d-printing/visual13.png)

The lack of continuous material paths and the stress concentration created by each layer joint contribute to this weakness. Since the layers are printed as a round-ended rectangle, the joints between each layer are actually small valleys. This creates a stress concentration where a crack will want to form.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/key-design-considerations-fdm-3d-printing/visual9.png)

## Vertical axis holes

FDM will often print vertical axis holes undersized. The general process for printing a hole diameter and the reason the reduction in diameter occurs is:

- As the nozzle prints the perimeter of a vertical axis hole, it compresses the newly printed layer down onto the existing build layers to help improve adhesion.
- The compressing force from the nozzle deforms the extruded round layer shape from a circle into a wider and flatter shape (see image below).
- This increases the area of contact with the previously printed layer (improving adhesion) but also increases the width of the extruded segment.
- The result of this is a decrease in the diameter of the hole that is being printed.

This can be an issue particularly when printing small diameter holes where the effect is greater due to the ratio of hole diameter to nozzle diameter.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/key-design-considerations-fdm-3d-printing/visual20.png)

The variation in slicer program vs. actual diameter of vertical holes is due to compression of the extruded profile

The amount of undersize will depend on the printer, the slicing software, the size of the hole, and the material. Often, the reduction in diameter of vertical axis holes is accounted for in the slicing program, but accuracy can vary and several test prints may be needed to achieve the desired accuracy. If a high level of accuracy is required, drilling the hole after printing may be required.

**Key design consideration:** If the diameter of your vertical axis hole is critical, printing it undersized and then drilling the hole to the correct diameter is recommended.

Support for holes is best avoided by changing the print orientation. Removal of support in horizontal axis holes can often be difficult, but by rotating the build direction 90 degrees, the need for support is eliminated. For components with multiple holes in different directions, prioritize blind holes, then holes with the smallest to largest diameter, then criticality of hole size.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/key-design-considerations-fdm-3d-printing/visual18.png)

Re-orientation of horizontal axis holes can eliminate the need for support

### Infill & Shell Thickness

FDM parts are usually not printed solid to reduce the print time and save material. Instead, the outer perimeter is traced using several passes, called the shell, and the interior is filled with an internal, low-density structure, called the infill.

Infill and shell thickness affect greatly the strength of a part. A guide for choosing the best shell and infill parameters for FDM 3D Printing can be found [here](https://www.3dhubs.com/knowledge-base/selecting-optimal-shell-and-infill-parameters-fdm-3d-printing/). For desktop FDM printers, the default setting is 25% infill density and 1 mm shell thickness, which is a good compromise between strength and speed for quick prints.

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/intro-fdm-3d-printing/9-fdm-sample-infill.jpg)

## Common FDM Materials

One of the key strengths of FDM is the **wide range of available materials**. These can range from commodity thermoplastics (such as PLA and ABS) to engineering materials (such as PA, TPU, and PETG) and high-performance thermoplastics (such as PEEK and PEI).

![](https://s3-eu-west-1.amazonaws.com/3dhubs-knowledgebase/intro-fdm-3d-printing/10-thermo-pyramid.png)

Thermoplastic materials pyramid available in FDM. As a rule of thumb, the higher a material is the better its mechanical properties.

The material used will affect the mechanical properties and accuracy of the printed part, but also its price. The most common FDM materials are summarized below.

### ABS

- ⊕ Good strength
- ⊕ Good temperature resistance
- ⊖ More susceptible to warping

### PLA

- ⊕ Excellent visual quality
- ⊕ Easy to print with
- ⊖ Low impact strength

### NYLON

- ⊕ High strength
- ⊕ Excellent wear and chemical resistance
- ⊖ Low humidity resistance

### PETG

- ⊕ Food Safe\*
- ⊕ Good strength
- ⊕ Easy to print with

<sub>\* The notches at the layer interface are critical points for bacterial growth, so thorough cleaning after every use is needed.</sub>

### TPU

- ⊕ Very flexible
- ⊖ Difficult to print accurately

### PEI

- ⊕ Excellent strength to weight
- ⊕ Excellent fire and chemical resistance
- ⊖ High cost

## Downloads

If you are interested in reading more about FDM 3D printing or need help troubleshooting why your print isn't working, you can download this booklet.

[The ABC of 3D-P.pdf](https://drive.google.com/file/d/1Em6fTpHhf1DHVCchMBOqeK_PSamBXBv8/view?usp=sharing)
