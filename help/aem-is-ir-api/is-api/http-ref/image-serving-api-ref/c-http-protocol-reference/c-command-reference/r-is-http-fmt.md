---
description: Response Image Format.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
---
# fmt{#fmt}

Response Image Format.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* &ndash; avif-alpha | avif | eps | f4m | gif-alpha | gif | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

|*`format`*| Description |
|---|---|
| `avif-alpha` | Lossy and lossless AVIF with alpha channel<br><br>*Release timeline for this format:* <br><b>North America</b> - Available now<br><b>Europe, Middle East, Africa</b> - August 13, 2021<br><b>Asia-Pacific</b> - Available now |
| `avif` | Lossy and lossless AVIF<br><br>*Release timeline for this format:*<br><b>North America</b> - Available now<br><b>Europe, Middle East, Africa</b> - August 13, 2021<br><b>Asia-Pacific</b> - Available now |
| `eps` | Uncompressed binary Encapsulated PostScript |
| `f4m` | Flash Streaming Server manifest format |
| `gif-alpha` | GIF with 2 to 255 colors plus key-color transparency |
| `gif` | GIF with 2 to 256 colors |
| `jpeg` | Lossy JPEG |
| `jpeg2000-alpha` | Lossy and lossless JPEG 2000 with alpha channel |
| `jpeg2000` | Lossy and lossless JPEG 2000 |
| `jpegxr-alpha` | Lossy and lossless JPEG XR with alpha channel |
| `jpegxr` | Lossy and lossless JPEG XR |
| `jpg` | Lossy JPG |
| `m3u8` | Apple Streaming Server manifest format |
| `pdf` | Image embedded in PDF |
| `pjpeg` | Progressive JPEG |
| `png-alpha` | 24-bit lossless PNG with alpha channel |
| `png` | 24-bit lossless PNG |
| `png8-alpha` | 8-bit lossless PNG with alpha channel |
| `png8` | 8-bit lossless PNG |
| `swf-alpha` | Lossy JPEG and a deflate-compressed mask embedded into an Adobe AS2 swf file |
| `swf`| Lossy JPEG embedded into an Adobe AS2 swf file |
| `swf3-alpha` | Lossy JPEG and a deflate-compressed mask embedded into an Adobe AS3 swf file. **Note:** swf and swf-alpha formats are best used for ActionScript 2 applications (Flash Player 8 and earlier). The formats swf3 and swf3-alpha are recommended for use for ActionScript3 applications (Flash Player 9 and later) |
| `swf3` | Lossy JPEG embedded into an Adobe AS3 swf file |
| `tif-alpha` | TIFF with alpha channel |
| `tif` | TIFF |
| `webp-alpha` | Lossy and lossless WebP with alpha channel |
| `webp` | Lossy and lossless WebP |

*`pixelType`* &ndash; rgb | gray | cmyk
| *`pixelType`* | Description | 
|---|---|
| `cmyk` | Return CMYK image data. |
| `gray` | Return gray-scale image data. |
| `rgb` | Return RGB image data. |

*`compression`* &ndash; none | lzw | zip | jpeg | lossy | lossless
| *`compression`* | Description | 
|---|---|
| `jpeg` | JPEG compression (lossy) |
| `lossy` | WebP, JPEG 2000, and JPEG XR compression (lossy) |
| `lossless` | WebP, JPEG 2000, and JPEG XR compression (lossless) |
| `lzw` | LZW (Lempel-Ziv-Welch) compression (lossless) |
| `none` | Uncompressed |
| `zip` | "Deflate" compression (lossless) |

* *`format`* specifies the image encoding format for image data sent to the client and the corresponding response MIME type for the HTTP response header. 
* *`pixelType`* can be used to effect output color space conversion when `icc=` is not specified.

  The default color profile corresponding to *`pixelType`* is applied. If color management is disabled, naïve conversion is applied. *`pixelType`* is ignored when `icc=` is specified, which determines the output pixel type. 

* *`compression`* is permitted only if `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr`, or `jpegxr-alpha` is specified as the *`format`*. Refer to the table below for the compression options supported for these image formats.

You can use `qlt=` to set the JPEG encoding options for these formats: JPEG, TIFF with JPEG compression, PDF with JPEG compression, and SWF. WebP, JPEG 2000, and JPEG XR also use `qlt=` but the values result in different qualities for the different formats. Use `quantize=` if `fmt=gif` or `fmt=gif-alpha`. Refer to the command descriptions for details. The other formats do not have settable options.

8 bits per pixel component are returned for all *`formats`* and *`pixelTypes`* (8 bits per pixel for GIF).

The following table lists the valid combinations of *`format`*and *`pixelType`*, the corresponding HTTP response MIME types, whether ICC profiles can be embedded (see [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)), and what format-specific options you can apply. 

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> format</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> Response MIME type</b> </th> 
   <th class="entry"> <b>Embed ICC profile</b> </th> 
   <th class="entry"> <b> Options</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Yes </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>The <span class="codeph"> pscan= </span> parameter applies only to pjpeg format. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gray </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Yes </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Yes </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Yes </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>'tiff' only; 'tiff-alpha' does not support jpeg compression. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> is ignored unless <span class="varname"> compression </span> is set to <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, gray </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> <p> <p>Note:  The Adobe Flash Player ignores embedded ICC profiles. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Yes </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> is ignored unless <span class="codeph"> <span class="varname"> compression </span> </span> is set to <span class="codeph"> jpeg </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Yes </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gray </p> <p>Data is converted to palette after conversion to gray or rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compression </span> </span> ( <span class="codeph"> lossy </span>, <span class="codeph"> lossless </span>) </p> <p> <span class="codeph"> qlt= </span> is ignored for <span class="codeph"> lossless </span>. </p> <p>Because there is no concept of chrominance downsampling with the WebP format, if you use a second value with <span class="codeph"> qlt </span> (for example, <span class="codeph"> qlt=80,1 </span>) the second value ( <span class="codeph"> 1 </span>) is ignored. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, gray </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p>Same as above. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p>Same as above. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p> avif, avif-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p>Same as above. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Request attribute. Applies regardless of current layer setting if `req=img` (default) or `req=mask`; ignored otherwise.

*`type`* is ignored if `iccProfile=` is specified.

## Default {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, where the *`defaultType`* is handled as follows: If `icc=` is specified, *`defaultType`* corresponds to the pixel type of the specified ICC profile. If `icc=` is not specified, *`defaultType`* is `gray` if `req=mask`, otherwise it is `rgb`.

## Examples {#section-b93222e652df404a84c69025247f07df}

**Request a small, low-quality preview image in JPEG format (default):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Request the same image converted to gray-scale:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Request the same image in a loss-less format with alpha channel and at high resolution:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Request the alpha channel for the same image as a gray-scale TIFF image:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Convert the same image to cmyk using the default ICC profiles:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Convert the same image to cmyk using a different ICC profile and embed the profile in the TIFF image:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Deliver this image as a TIF file with JPEG compression without pixel type conversion:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Convert image to a bi-tonal GIF with key-color transparency and force colors to black and white:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Lossy with a quality setting of 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Lossless with alpha:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Lossy with a quality setting of 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Lossless with alpha:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Lossy with a quality setting of 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Lossless with alpha:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## See also {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301), [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
