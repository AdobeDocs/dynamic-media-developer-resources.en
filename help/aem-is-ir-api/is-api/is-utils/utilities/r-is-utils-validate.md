---
description: Image validation utility. This command-line utility verifies image files to make sure that they are valid and Image Serving can read them without difficulty.
solution: Experience Manager
title: validate
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
TQID: 'https://experienceleague.adobe.com/gWtVDo3ounZMncdhwLMJsoRaPyZP3E1Fi98L8fX6XFA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# validate{#validate}

Image validation utility. This command-line utility verifies image files to make sure they are valid and can be read by Image Serving without difficulty.

All non-PTIFF image files must pass validation before the file is made available to Image Serving as a source image. PTIFF images should be validated after potentially unreliable copy operations.

## Usage {#usage}

` validate *`fileType`* [ *`options`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>Source file type; at least one must be specified (-any allows the same image file types supported by IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> options </span> </span> </p> </td> 
  <td class="stentry"> <p>Other command options (see below). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> Image file. None or more, separated by spaces. </p> </td> 
 </tr> 
</table>

## Returns {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 if successful. If an error occurs, a non-zero value is returned and error details are sent to `stderr`.

## Options {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>Specifies a separate text file containing the list of image files. One record per file. If <span class="codeph"> -fileList </span> is included, <span class="varname"> sourceFile </span> must not be specified. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>Enables verification of the entire image file. By default, only the image header is validated. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>Verifies the embedded color profile for validity. By default, the body profile is not checked. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> Rejects images with 16 bits per image component. Always specified by the Image Server when it validates remote source images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> Prints more information if the image is invalid. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>Disables <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span> output. Only a status is returned. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>Terminates processing when a file validation failure occurs, even if additional files are yet to be validated. By default, processing continues when a validation error occurs </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version </span> </p> </td> 
  <td class="stentry"> <p>Returns version info for this utility. Specify with no other options. </p> </td> 
 </tr> 
</table>
