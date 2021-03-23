---
description: The following options can be applied regardless of the type of sourceFile.


solution: Experience Manager
title: Common options

feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Common options{#common-options}

The following options can be applied regardless of the type of sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> string </span> </span> </p> </td> 
  <td class="stentry"> <p>Folder in which output files are to be placed (including the log file, if <span class="codeph"> -log </span> is specified). May be an absolute path or relative to the current working directory. The folder hierarchy will be created if it does not exist. Does not apply to the file specified with <span class="codeph"> -log </span>. If not specified, output files are written to the folder in which <span class="varname"> sourceFile </span> is located. If <span class="varname"> destFile </span> is specified, it will always be written to that location, and <span class="codeph"> -destpath </span> only applies to the secondary output files. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image </span> </p> </td> 
  <td class="stentry"> <p>If specified, the (first) view image is extracted from the vignette, a suitable panel image from a cabinet style, or the first illumination image of a window covering style. The extracted image is saved as a full-resolution TIFF file. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Prevents generation of target files. Useful to quickly extract attributes from <span class="varname"> sourceFile </span>. Only the optional thumbnail ( <span class="codeph"> -thumbwidth </span>), image ( <span class="codeph"> -image </span>) and log files ( <span class="codeph"> -log </span>) are generated. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Selects lossy JPEG encoding for RGB and gray-scale image data embedded in the output file, instead of lossless PNG. Images with alpha (RGBA) are always saved using PNG encoding. <span class="varname"> ival </span> specifies the JPEG quality (1...100); 85 or higher is recommended. Default is <span class="codeph"> -jpegquality 0 </span>, which selects PNG encoding. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> path </span> </span> </p> </td> 
  <td class="stentry"> <p>Creates a log file with the specified path/name The full paths of all output files written to the destination folder are written to the log file, as well as some additional settings, such as version info and any warnings or errors encountered (see <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Output </a> for details). No log file is created if <span class="codeph"> -log </span> is not specified; in this case, all text output is written to <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Lower the priority of the <span class="filepath"> vntc </span> process. This can be used so that <span class="filepath"> vntc </span> won't take over an entire CPU while processing a vignette. It allows the operating system to give more time to other, more important, processes. <span class="varname"> ival </span> specifies the lower priority percentage (0..100). Default is <span class="codeph"> -lowerpriority 0 </span>, which does not lower the priority of the <span class="filepath"> vntc </span> process. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Specify the maximum amount of memory that <span class="filepath"> vntc </span> is allowed to use in bytes. When <span class="filepath"> vntc </span> reaches the maximum memory limit, it stops processing and produces an error. <span class="varname"> ival </span> specifies the maximum memory limit in bytes (0.. 3,758,096,384 (3.5GB)). When <span class="varname"> ival </span> is 0, the maximum memory limit is turned off. Default is <span class="codeph"> -maxmem 3221225472 </span>, which means a maximum memory limit of 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> string </span>" </span> </p> </td> 
  <td class="stentry"> <p>Specifies the separator placed between the filename and the size/resolution suffix for auto-generated output file names. Defaults to "-" if not specified. Ignored if <span class="varname"> destFile </span> or <span class="codeph"> -info </span> is specified. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Enables sharpening of images resampled (scaled) during processing. Only applies to thumbnail sharpening in case of cabinet style files. </p> <p>Specify 0 to disable sharpening (default), 1 to enable normal sharpening, 2 to enable unsharp-masking for brightness only, or 3 to enable unsharp-masking for each color component. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>Sets the log level. Default is 1, which outputs all informational, warning, and error messages. Set to 0 to disable all but error messages. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> amount </span> <span class="varname"> radius </span> <span class="varname"> threshold </span> </span> </p> </td> 
  <td class="stentry"> <p>Sets the unsharp-masking parameters. Ignored if <span class="codeph"> -sharpen </span> is set to 0 or 1; required if <span class="codeph"> -sharpen </span> is set to 2 or 3. <span class="varname"> amount </span> is a real value in the range 0.0...500.0, <span class="varname"> radius </span> is a real value in the range 0.0…10.0, and <span class="varname"> threshold </span> is an integer between 0 and 255. Refer to the description of <span class="codeph"> op_usm= </span> in the Image Serving Protocol Reference for additional information. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Validate that the given vignette is a proper production vignette. <span class="varname"> ival </span> represents the minimum file version of the vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>File version for the output file. If specified, must be 0 or a valid vignette file version (no larger than the default file version). If set to 0 or not specified, the output file is created using the most current file version. Ignored if <span class="codeph"> -info </span> is specified. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Returns version information for this utility. Specify without filename and other options. </p> </td> 
 </tr> 
</table>

