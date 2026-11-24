# Computer Controlled Cutting

In this week's assignment, we got introduced to Computer Controlled Cutting.

## Parametric Design

A Parametric design is a really powerfull method in design. You stop working with precise dimension and you introduce parameters. So every time you want to change one dimension you simple chnage the parameter and everything fits accordigly. 

To experiment with parametric design, i designed all of my final project box using parameters. In fushion you can do that by clicking **Change Parameters**

### Costruction Kit

To test the parametric design and the joints I designed a hexagon and a polygon with finger joints. The joints also have camfered edjes. All the dimensions are parameters.
<div>
  <img src="assets/Week03/Construction Kit.png"  style="width: 60%; border-radius: 6px;">
</div>

<div>
  <img src="assets/Week03/Construction Kit Parameters.png"  style="width: 100%; border-radius: 6px;">
</div>

The sketches were exported in .DXF format and imported in Inkscape to be ready to be used in the laser cut.

![Construction Kit Inkscape](assets/Week03/Construction%20Kit%20Inkscape.png){ width="300" }

> **Note on Kerf Compensation:**  
> **Kerf** is the width of material burned away by the laser beam during cutting (typically around `0.12–0.15 mm`). Because this material is removed from both sides of the cut path, a slot drawn at the exact material thickness (`4.00 mm`) will end up slightly wider, resulting in a loose fit. To achieve a tight press-fit joint without glue, the slot width is parametrically defined as `slot_w = t - kerf` (`3.85 mm`), compensating for the laser beam's width.

## Computer Aided Manufacturing(CAM)

CAM Software: Is a software that takes digital design and converts it into machine instructions. You design ypur part, then you go through the software and through this software you generate the job the machine will execyte afterwards.

### Laser Cutting / Vinyl Cutting

Laser Cutting: fast, easy, and accurate way to cut and engrave detailed artwork. To do this, it continuously shoots a powerful laser beam, through series of mirrors and lenses that move laterally and onto a flat bed where sheets of material such as cardboard, MDF and aacrylic are placed

*Generally takes in input 2D files, either vector, raster or both
*Generates 2D toolpaths
*Considers for lasers: power, speed, freq, job position, focus etc
*Considers for Vinyl Cutter: force(downward weight applied to the blade, low for thin material- high for heavy dense materials), speed (how fast the machine moves), cut depth(how much the blade will protrude from the head) , job position etc

!IMPORTANT! You can assign colors to the setting(ex. engrave, cut etc). You cut from **inside out**. First you do the work inside and last the outside.

Dipnest: Software that put the pieces together to save material

Vinly Cytting Softwares: InkCut, Silhouette Studio




