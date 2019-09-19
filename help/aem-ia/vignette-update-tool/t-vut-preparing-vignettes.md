---
title: Preparing Vignettes for the Image Rendering System
seo-title: Preparing Vignettes for the Image Rendering System in Dynamic Media (Scene7) Image Authoring Guide
description: Vignettes that you process with the Vignette Update tool are saved in the same folders as their originals.
seo-description: Vignettes that you process with the Vignette Update tool are saved in the same folders as their originals.
---

# Preparing Vignettes for the Image Rendering System

Vignettes that you process with the Vignette Update tool are saved in the same folders as their originals.

Each vignette has its width specification appended to its filename, so you can tell the processed vignettes from the original ones.

**To Prepare Vignettes for the Image Rendering System:**

1. From your computer desktop, click the Start button, then choose Scene7 &gt; Image Authoring > Vignette Update tool.
1. Click [!UICONTROL Select Vignettes].
1. Navigate to the folder containing your vignettes. Select the vignettes to place in the list on the left.

   Placing vignettes in the list makes them available to the Vignette Update tool. You can select multiple vignette files in the dialog box by using the Shift key (to select adjacent files) or the Ctrl key (to add or remove a single file from the selection).

1. Specify the following settings, which will be applied to all the selected vignettes:

   * **Target Vignette Width:** Specifies the width of each resulting vignette view image in pixels.
   * **Thumbnail Width:** Specifies the width of each resulting thumbnail in pixels. This setting is optional.
   * **Zoom Multiplier and Max Zoom Levels:** To create versions of the vignette at different magnifications, specify both the Zoom Multiplier and the Max Zoom Levels settings.

     The Zoom Multiplier indicates how many times to magnify the vignette for each version. For example, a zoom multiplier of 2 doubles the size of the vignette for each saved version.

     The Max Zoom Levels indicates the largest number of magnified versions to create. The number of versions is also limited by the size of the original vignette. The Vignette Update tool determines how close to the next zoom level the original vignette size is. If it is at least half again as large as the last zoom level, it uses the original size as the largest zoom level. If it is closer than that, it does not produce another zoom level. For example, if the original vignette is 700 pixels in either direction, and the target vignette is 400 pixels wide, a zoom factor of 2 produces a maximum of 2 saved vignettes: one at 400 pixels wide and one at 700. The second one is produced because 700 is more than half again as large as 400. The next natural zoom level would be 800, which exceeds the original size.

   * **Size Suffix Separator:** Specifies the character that separates the vignette name and the suffix indicating its size.
   * **Save As Version:** Lets you specify the file format version for the selected vignettes. If you have a new version of Image Authoring and an older version of the Image Rendering server, you must specify a vignette version that your Image Rendering server can read. If you specify a higher version, the Image Rendering system can not read the vignettes.

     By default, the Save As Version is the version supported by Image Authoring (displayed as the VNT Version in the About box, available from the Help menu). In the Vignette Update tool, each vignette in the list displays its file format version in parentheses, but all are output in the format version specified in the Save As Version field.

     Check your Image Rendering system and determine the version number it supports. See the documentation for the Image Rendering system.

   * **Expand Maps:** Converts the UV Data for each object to a UV map. This reduces rendering time, so it's best to leave it checked.
   * **Sharpen Images:** Applies sharpening to the main view image for each vignette. This option is similar to the Photoshop sharpen option. Sharpening can compensate for blurring when vignettes are scaled. It is optional.

1. When you have finished specifying the settings, click Start Processing to process the vignettes.
1. When the vignettes have been processed, click Exit.
