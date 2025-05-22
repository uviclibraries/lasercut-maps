---
layout: default
title: 3-Contour Extraction
nav_order: 4
parent: Workshop Activities
---

## Contour Extraction
With the merged raster appropriately coloured, we can generate elevation contours from it. This will be the basis for the laser cut .SVG files. From the Raster menu, navigate to *‘Extraction’* then *‘Contour’*. <br>
<br><img src="images/contour.png" style="width:450px;" alt="QGIS generate contour"><br>
<br> Keep all default parameters in the window and ensure the input layer is your merged raster. Click *‘Run’*.<br>
<br><img src="images/contour2.png" style="width:450px;" alt="QGIS contour inputs"><br>
<br>Uncheck the merged raster layer in the layers pane to view only the line contours.<br>
<br><img src="images/contour3.png" style="width:550px;" alt="contours"><br>
- >Before making any other edits, right-click the contour layer you generated in the layers menu and save it to your project files
  >**(Export -> Save Features As)**.
- It should default to saving as an ESRI shapefile (.shp)
- >As we are focusing on bathymetry, we need to remove all contour lines above 0m.
  >To do so, **right-click** the *‘contours’* layer in the contents pane.
  >From the menu, select *‘open attribute table’*. <br>
<br><img src="images/attribute.png" style="width:450px;" alt="QGIS open attribute table"><br>
<br> With the attribute table open, navigate to the *‘Select feature by expression’* tool at the top of the page.<br>
<br><img src="images/select.png" style="width:450px;" alt="QGIS select features by expression"><br>
<br> The expression editor will open. Type or copy **“ELEV” > 0** into the window. Click *‘select features’* at the bottom of the window to complete the process.<br>
<br><img src="images/expression.png" style="width:450px;" alt="QGIS input expression"><br>
<br>You will see that all contour lines with values greater than zero are now highlighted in yellow on the map.<br>
<br><img src="images/selected.png" style="width:550px;" alt="contours selected"><br>
<br>Right-click the contour layer in the contents pane. Click *‘toggle editing*’. <br>
<br><img src="images/editing.png" style="width:450px;" alt="QGIS toggle editing"><br>
<br>From the toolbar at the top of the window, click *‘delete selected’*. Confirm your selection in the pop-up. If your file contains outlying squares like these:<br>
<br><img src="images/outliers.png" style="width:550px;" alt="QGIS delete selected features"><br>
<br>They will need to be removed, as they will complicate the rest of the data editing process. If there are no outliers, proceed to the *‘saving edits’* step. If your dataset contains outliers,  keep layer editing enabled, open the ‘select features’ menu, and open the ‘select by freehand’ tool.<br>
<br><img src="images/freehand.png" style="width:450px;" alt="QGIS select by freehand"><br>
<br>Work slowly to ensure necessary features are not selected accidentally. If that happens, click the *‘Remove selection’* tool to clear all features from selection. <br>
<br><img src="images/remove.png" style="width:450px;" alt="QGIS remove selection"><br>
<br>Unnecessary features can be deleted the same way the elevation lines above 0m were deleted (Toggle editing > Delete Selected) When you have all extraneous features removed, save all edits to the layer and switch editing off (the single pencil icon next to the save tool).<br>
<br><img src="images/layer_save.png" style="width:450px;" alt="QGIS end editing"><br>
<br>Now is a good time to save your project. <br>
<br>Reopen the contour layer’s attribute table. Open the *‘select by attribute’* tool. Input **“ELEV” = 0**.<br>
<br><img src="images/select.png" style="width:350px;" alt="QGIS select tool"><br>

- With the selection made, right-click the layer and navigate to ‘save selected features as’.
- Change the format from an ESRI shapefile to an AutoCAD DXF.
- Open your project folder and add a new subfolder. Title it 'design_finals'. Save the DXF layer here.
- A popup will appear after saving the file, asking if the DXF should be added to your QGIS project. Click ‘Add Layer’ to proceed.
- These layers are being added to the project file only for visualization purposes and will not need to be manipulated further.<br>
<br><img src="images/dxf_save.png" style="width:450px;" alt="contours selected"><br>
<br>Repeat this process for **“ELEV” = -50, -100, and -150**, remembering to clear the selection between groups. ***Name each file as the depth it shows (for example, 0m.dxf, 50m.dxf). Failure to do so will make subsequent instructions harder to understand.*** <br>
<br><img src="images/deselect_att.png" style="width:450px;" alt="contours selected"><br>
- If there are no features available for a depth of -150, work backwards by 10m increments until features are selected successfully.
- If you would like to experiment with selecting different depth measurements, you are welcome to. Ideally, limit it to three or four layers plus the 0m layer.
-  Deselect the original contours from the layers menu to see what the extracted layers look like on their own. Here is my example. <br>
<br><img src="images/contours_final.png" style="width:550px;" alt="contours selected"><br>
<br>Now is a good time to save your project. 

[NEXT STEP: Add Details for Engraving](engraving.html){: .btn .btn-blue }
