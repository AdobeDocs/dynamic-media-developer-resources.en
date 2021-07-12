---
description: vntc generates text data which is sent either to stderr or the log file.
solution: Experience Manager
title: Output
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
---
# Output{#output}

vntc generates text data which is sent either to stderr or the log file.

The data is formatted as one `name=value` property per text record. String values are not quoted. Warning and error messages are always sent to `stderr`, even if `-log` is specified.

Certain properties can occur multiple times in the same output. A sequence number, starting with 0, is appended to the name of these properties, separated by a period. Such properties are identified below with a `. *`n`*` suffix after the property name.

The following properties are generated:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>The RGB background color of the cabinet style. Cabinet styles only. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>The default output file version. Also the highest file version number this release of <span class="filepath"> vntc</span> can generate. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">error.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Error message. Presence of error messages typically indicate that either no output file(s) are created or that they are not suitable for use by Image Rendering. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">file.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>The fully qualified path/name of all output files, including vignettes, cabinet style files, full resolution images, and thumbnail images. One file attribute is present for each generated file (except the log file). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> is 1 if the cabinet includes glass doors, 0 otherwise. Cabinet styles only. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>The name of the iccProfile embedded in the <span class="varname"> sourceFile</span>. </p> <p>Empty if <span class="varname"> sourceFile</span> is not color-managed. Vignettes only. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Informational message, such as progress information. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> is 1 if <span class="varname"> sourceFile</span> is a master vignette, 0 if it has been processed previously with <span class="filepath"> vnUpdate</span> or <span class="filepath"> vntc</span>. Vignettes only. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> is 0 if <span class="varname"> sourceFile</span> is a cabinet style containing JPEG image data (a warning is also output in this case), 1 otherwise. Cabinet and window covering style files only. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>The maximum memory limit that applies to the running <span class="filepath"> vntc</span> process. <span class="varname"> string</span> is either <span class="varname"> ival</span>, <span class="varname"> ivalK</span>, <span class="varname"> ivalM</span>, <span class="varname"> ivalG</span>, or <span class="codeph"> 0</span> (disabled). Where <span class="varname"> K</span>, <span class="varname"> M</span>, and <span class="varname"> G</span> refer to Kilobytes (1024 bytes), Megabytes (1048576 bytes), and Gigabytes (1073741824 bytes). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Scale of the lowest resolution pyramid level in the output vignette. Only present if <span class="codeph"> -pyramid</span> is specified. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>The number of materials saved in the <span class="varname"> sourceFile</span>. Vignettes only. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>The number of panel images in this cabinet style file. Cabinet styles only. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>The number of pyramid levels in the output vignette. Only present if -pyramid is specified. Vignettes only. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramid=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 if either the source or destination vignette has pyramid structure. Vignettes only. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>For cabinet styles, the object resolution of the<span class="varname"> sourceFile</span>. For vignettes, this is the recommended material resolution for best quality render results when rendering the output vignette. Pixels/inch (ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>The smallest object resolution in the output vignette. Vignettes only. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>The average object resolution in the output vignette. Vignettes only. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>The fully qualified <span class="varname"> sourceFile</span> path. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>The file version of <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>The pixel size of the input vignette, the default panel image in a cabinet style file, or the first opacity image of a window covering style file. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>The type of window covering (window covering styles only): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=horizontal shade or blinds </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=vertical blinds </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=full-width short curtains </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=left/right short drapes </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=full-width full-length curtains </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=left/right full-length drapes </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=café curtain </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> if <span class="varname"> sourceFile</span> is a vignette, <span class="codeph"> vnc</span> if <span class="varname"> sourceFile</span> is a cabinet style, or <span class="codeph"> vnw</span> if <span class="varname"> sourceFile</span> is a window covering style. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>The value specified with <span class="codeph"> -version</span>, or the value of<span class="codeph"> defaultFileVersion</span> if<span class="codeph"> -version</span> was not specified. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Comma-separated list of the pixel sizes of the all views in the output vignette (the full-resolution view for pyramid vignettes), of the default panel image in a cabinet style file, or of the first opacity image of a window covering style file. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> is 1 if the cabinet style is texturable, 0 otherwise. Not present for vignettes and window coverings style files. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">warning.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Warning message (such as when <span class="codeph"> -imagemap</span> is specified but no map data is found in the vignette). </p></td> 
 </tr> 
</table>
