---
description: The following options control the processing of vignette files. They are ignored if sourceFile is not a vignette.
solution: Experience Manager
title: Options for vignettes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
---
# Options for vignettes{#options-for-vignettes}

The following options control the processing of vignette files. They are ignored if sourceFile is not a vignette.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contents</span> </p></td> 
  <td class="stentry"> <p>Creates an XML file representing the object hierarchy, and including selected object attributes. The contents of the file is the same as returned by the <span class="codeph"> req=contents</span> command. The file has the same name as the source file, but with an <span class="filepath"> .xml</span> suffix. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Crop the vignette before scaling. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> is the top let corner of the crop rectangle, and <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> is the size of the crop rectangle. Values are pixel coordinates relative to the full-resolution view image of the source vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>Crop the vignette before scaling. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> is the top let corner of the crop rectangle, and <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> hein</span></span> is the size of the crop rectangle. Values are normalized relative to the view image of the source vignette and must be between 0.0…1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> and <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> must be no larger than 1.0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedmaterials</span> </p></td> 
  <td class="stentry"> <p>Keep embedded materials in the output vignette. By default materials are removed from the output vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>One or more output vignette heights in pixels. Ignored if -info is specified. <span class="varname"> ival</span> may be 0, which denotes the width of the input vignette. See <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignette Scaling</a> for detailed information. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Enable extraction of the image map file from the vignette. The map data is written to a HTML file containing only a <span class="codeph"> &lt;map&gt;</span> element. The output file is named the same as the output image file, but with an <span class="filepath"> .htm</span> suffix. A warning message is generated and no file is created if the command is specified but no map data is present in the vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>Saves a copy of the ICC profile embedded in the vignette to a file. A warning message is generated and no ICC profile file is created if the command is specified but no ICC profile is present in the vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pyramid</span> </p></td> 
  <td class="stentry"> <p>Creates a pyramid vignette. Required when rendered images are to be displayed with Dynamic Media zoom viewers. See <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignette Scaling</a> for additional information. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Pixel width and height constraint for the thumbnail image. If specified, a JPEG image which is no wider and no taller than <span class="varname"> ival</span> is generated from the vignette view image, a panel image of the cabinet style file, or the illumination map of the first style in the window coverings style file. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>One or more output vignette widths in pixels. Ignored if <span class="codeph"> -info</span> is specified. <span class="varname"> ival</span> may be 0, which denotes the height of the input vignette. See <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignette Scaling</a> for detailed information. </p></td> 
 </tr> 
</table>
