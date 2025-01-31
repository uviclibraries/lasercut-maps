---
layout: default
title: 5-Contour Extraction
nav_order: 6
parent: Workshop Activities
---
## Inkscape contour formatting 
Open the Inkscape program and select ‘new document’ from the startup menu. From the document’s file menu, import your -150m DXF file.<br>
<img src="images/is_open.png" style="width:250px;" alt="Inkscape file open">
<br>Ensure that scaling is set to ‘automatic to A4’ and character encoding is UTF-8.<br>
<img src="images/is_input.png" style="width:250px;" alt="Inkscape file parameters">
<br>A warning will appear. Click OK to load the file into the document. Move it so that the edges of the layer align with the edges of the document. Refer to your QGIS window for the correct scaling.<br> 
<br>From the menus at the right of the screen, open the ‘fill and stroke’ options. Set fill to null (the X), the stroke to flat colour, with 100% opacity and a red value of 255. Under stroke style, set the width to 0.1mm. This allows the lasercut program to read these designs as cut lines, rather than as shapes to be engraved. Repeat this process with the rest of your files, opening them in new Inkscape windows. Ensure the fill and stroke values are all set to the above parameters. <br>
<img src="images/is_colours.png" style="width:250px;" alt="Inkscape line colour settings">
<br>When you have opened and formatted all your contour files in different Inkscape windows, look through them. At least one of your layers should have cut-off lines indicating the upper boundaries of the project file, like the example below. We will use these boundaries to define a consistent area for each layer of the project.<br>
<img src="images/is_upper.png" style="width:250px;" alt="Project upper boundaries">
<br>Navigate to the rectangle tool in Inkscape’s left-hand menu and use it to draw a rectangle around the edges of your project. Use the cut-off lines as a guide for the top border. Ensure the rectangle’s fill and stroke settings are the same as the contour lines (0 fill, solid stroke, red value 255, line width 0.1 mm).<br>
<img src="images/is_rect.png" style="width:250px;" alt="Inkscape rectangle tool">
<br>Select the rectangle in the layers pane and copy it to your clipboard.<br>
<img src="images/is_copy.png" style="width:250px;" alt="Inkscape copy tool">
<br> Go into your other Inkscape windows and paste the rectangle into each of the files. Line up the bottom corners with the edges of the page. Now the layers are all the same size. When all layers include the border rectangle, open the File menu from the top left of the Inkscape window. Select ‘Save As’ and save your layer as an .SVG file (the default file type for Inkscape). <br> 
<img src="images/is_save.png" style="width:250px;" alt="Inkscape save file as"> <br>
## Inkscape placename formatting
<br>With the 0m contour file open, use the Import tool to bring in the screenshot of the place names if you used them. If you used street data to create features for engraving, skip these steps. Ensure the image render mode is set to Smooth.<br>
<img src="images/is_png.png" style="width:250px;" alt="Inkscape open PNG">
<br>In the Layers pane, turn off visibility for the contour line layer, leaving the placenames visible.<br> 
<img src="images/layers.png" style="width:250px;" alt="Inkscape hide layer">
<br>From the upper menu, open the Path tab and select Trace Bitmap. <br>
<img src="images/trace.png" style="width:250px;" alt="Inkscape trace bitmap tool">
<br>The tool will open in the right-side panel. Ensure the label layer is selected in the Objects menu. Bitmap trace should default to single scan mode. A brightness cutoff of around 0.66 should be effective. When the preview looks good, click ‘Apply’. <br>
<img src="images/trace2.png" style="width:250px;" alt="Inkscape trace bitmap tool">
This converts the .png image of labels into a path format suitable for laser engraving. Navigate back to the layers tab and turn visibility off for the original screenshot, while turning it on for the 0m contour layer. Position the labels accurately on the 0m layer, using the QGIS project for reference. With this complete, set the fill of the label layer to solid, the stroke to none, and the colour to 0 in R, G, and B with 100% opacity. Do not edit the line weight.



