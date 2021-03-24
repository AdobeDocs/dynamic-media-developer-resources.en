---
description: Response image format.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# fmt{#fmt}

Response image format.

 `fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> format</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Specifies the image encoding format for image data sent to the client and the corresponding response MIME type for the HTTP reply header. </p> <p> <span class="codeph">  jpeg </span>: lossy JPEG </p> <p> <span class="codeph"> png </span>: loss-less PNG </p> <p> <span class="codeph"> png-alpha </span>: loss-less PNG with alpha channel </p> <p> <span class="codeph">  tif </span>: TIFF </p> <p> <span class="codeph"> tif-alpha </span>: TIFF with alpha channel </p> <p> <span class="codeph">  swf </span>: lossy JPEG embedded into an Adobe swf file </p> <p> <span class="codeph"> pdf </span>: image embedded in PDF </p> <p> <span class="codeph"> gif </span>: GIF with 2 to 256 colors </p> <p> <span class="codeph"> gif-alpha </span>: GIF with 2 to 255 colors plus key-color transparency </p> <p> <span class="codeph"> fxg </span>: FXG with variables and DOM manipulation applied </p> <p> <span class="codeph">  fxgraw </span>: original FXG stored on server </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | gray | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Can be used to effect output color space. </p> <p> <span class="codeph">  rgb </span>: return RGB image data </p> <p> <span class="codeph"> gray </span>: return gray-scale image data </p> <p> <span class="codeph"> cmyk </span>: return CMYK image data </p> </td> 
 </tr> 
</table>

`tiffCompression` is permitted only if tif, tif-alpha is specified as the format. Refer to the table below for the compression options supported for these image formats.

`qlt=` can be used to set the JPEG encoding options for these formats: JPEG, TIFF with JPEG compression. quantize= can be used if fmt=gif or fmt=gif-alpha. Refer to the command descriptions for details. The other formats do not have settable options.

8-bits per pixel component are returned for all formats and `pixelTypes[7]`.

The following table lists the valid combinations of format and `pixelType`, the corresponding HTTP response MIME types.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> format</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Response MIME type </p> </th> 
   <th colname="col4" class="entry"> <p>Embed ICC profile </p> </th> 
   <th colname="col5" class="entry"> <p>Options </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, gray, cmyk </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>rgb, gray </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb, gray, cmyk </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( none | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application/x-shockwave-flash&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb, gray, cmyk </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rgb, gray </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> quantize=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf] 
