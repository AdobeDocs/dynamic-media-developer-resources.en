---
description: Image Conversion utility.
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
---
# ic {#ic}

Image Conversion utility.

 `ic` is a command line tool that converts image files to the optimized Pyramid TIFF format (PTIFF). While Image Serving can process images without conversion, we recommend that you convert all images larger than 512x512 pixels to PTIFF. This conversion ensures optimal server performance and resource usage and minimizes response times.

It is recommended that PTIFF files that contain photographic content be JPEG-encoded (specify `-jpegcompress`). Computer-generated contents can benefit from lossless compression (either `-deflatecompress` or `-lzwcompress`). Unless a color conversion or pixel type conversion is required, JPEG source image data is transferred to the PTIFF without decoding, to avoid quality degradation. In this case, the specified compression options apply only to the lower resolution pyramid levels.

If you are not converting large images you do not have to set the parameters that control how much memory to use. However, if you are, give `ic` more memory by using the `-maxmem` setting described below. A good rule of thumb for computing the amount of memory required is to multiply the width of the image times the height of the image times the number of channels. For example, four for an RGB image with alpha times three. In addition, if the channels are 16-bits per component instead of 8 double the final result.

## Usage {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>options</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Command options (see below). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Single input image file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Single output PTIFF file (not valid if used with SourceDirectory). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Folder containing input images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Folder to which output PTIFF files are written. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-36a2dcfa39824d29b69547c432366219}

0 if successful. If an error occurs, a nonzero value is returned and error details are sent to `stderr`.

## Options {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -uncompressed </span> </p> </td> 
   <td colname="col2"> <p>Do not compress the output image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>Use deflate (zip) compression (default). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Use Lempel-Ziv-Welch (LZW) compression. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>Use JPEG encoding. Ignored if <span class="codeph"> <span class="varname"> sourceFile </span> </span> includes alpha data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> quality </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG quality (0-100; default is 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>Disable JPEG chroma-downsampling (can improve quality of color text and graphics). This has no effect on output images that are CMYK or grayscale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> amount </span>&gt; &lt; <span class="varname"> radius </span>&gt; &lt; <span class="varname"> threshold </span>&gt; &lt; <span class="varname"> monochrome </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Apply unsharp-masking to subsampled pyramid levels. See <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> for details. (Not applied to the full resolution image.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>Use the clip path in the source file, if any, to create associated alpha data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Print resolution (dpi) for <span class="codeph"> <span class="varname"> destFile </span> </span>; if not specified, the print resolution of <span class="codeph"> srcFile </span> is copied to <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> mode </span>&gt; &lt; <span class="varname"> tolerance </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Calculate a crop rectangle to minimize a solid color background. No crop info is output if the auto-crop algorithm would result in the entire image being cropped. </p> <p>To calculate the crop rectangle without converting the image, specify <span class="codeph"> -autocrop </span> without <span class="codeph"> -convert </span> and without <span class="codeph"> <span class="varname"> destFile.</span> </span></p>
   
   <p><i><b>corner</b></i> &ndash; ul | ur | ll | lr </p>
   <p> Specifies which corner of the image to use a seed point. Ignored if mode is 1.</p>
   <p><i><b>mode</b></i> &ndash; 0 | 1</p>
   <p>Set to 0 to crop based on the color of the specified corner pixel; works on premultiplied color data if alpha data is associated with the source image.</p>
   <p>Set to 1 to crop based on alpha data; corner is ignored and 0 is always the seed value; no crop is applied if no alpha data is associated with the source image.</p> 
   <p><i><b>tolerance</b></i> &ndash; Match tolerance. Real value 0.0 to 1.0. Specifies the tolerance for matching pixel component values. Set to 0 for exact matches.</p>
   <p><i><b>infoFile</b></i> &ndash; Path and name of the XML output file to which crop info data is written.</p>
   
   <p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>Copy XMP metadata, if available, from <span class="codeph"> <span class="varname"> sourceFile </span> </span> to <span class="codeph"> <span class="varname"> destFile </span> </span> without modification. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> Embed the ICC color profile in <span class="codeph"> <span class="varname"> destFile </span> </span>, if available (no profile is embedded by default). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Path and name of an ICC profile file. Defines the color space of <span class="codeph"> <span class="varname"> sourceFile </span> </span> and must match its pixel type. Should be specified only if no profile is embedded in <span class="codeph"> <span class="varname"> sourceFile </span> </span>, as this overrides the embedded profile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Path and name of an ICC profile file. Defines the pixel type and color space of <span class="codeph"> <span class="varname"> destFile </span> </span>. IC converts to this profile if <span class="codeph"> <span class="varname"> sourceFile </span> </span> has an embedded profile or if <span class="codeph"> -imageprofile </span> is specified as well. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>Perceptual render intent for color space conversions. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> Relative Colorimetric render intent for color space conversions (default). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>Absolute Colorimetric render intent for color space conversions. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>Saturation render Intent for color space conversions. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>Disable blackpoint compensation for certain color conversions </p> <p>Enabled by default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>Disable dithering (error diffusion) when color-converting. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> Disable automatic conversion from CMYK to RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>Force decoding and re-encoding of JPEG input images. </p> <p> <b>Caution:</b> Applying this option may reduce image quality. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>Use standard quality (bi-linear) resampling filter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>Use higher quality (Lanczos window) resampling filter (default). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>Use higher quality (FlashPix) resampling filter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Downsample with Photoshop style 8x8 bicubic-sharp filter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> When specified as the first option, suppresses output of usage info when invalid options are encountered. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -overwrite </span> </p> </td> 
   <td colname="col2"> <p>Allow overwriting an existing <span class="codeph"> <span class="varname"> destFile </span> </span>. By default, a numeric suffix is appended to the file name to prevent overwriting. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>Ignore hidden source files. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>Do not stop processing when an error occurs. Only has an effect when processing multiple files. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Path and name for the log file (defaults to <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> level </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Log level. </p> 
   <p>< 0 &ndash; Logging disabled.</p>
   <p>0 &ndash; List files to be processed.</p>
   <p>1 &ndash; Add reporting for unneeded files.</p>
   <p>2 &ndash; Add progress reporting.</p>
   <p>3 &ndash; Add reporting on every file encountered.</p>
   <p>4 &ndash; Add progress reporting at the file level.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>Append to log file (default). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>Overwrite log file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Logging interval in msec for loglevel 2 and higher (default is 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> bytes </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Memory usage limit. Must be at least 10 MB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Memory usage limit. Default is 25% of physical memory. If neither <span class="codeph"> maxmem </span> nor <span class="codeph"> maxmempercent </span> are explicitly set uses maxmempercent default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version </span> </p> </td> 
   <td colname="col2"> <p> Return version info for this utility. Specify with no other options. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Supported Input Image Formats {#section-ab13d941d6724e65b9f84b62d949d31c}

The following table lists the image file formats and format options which are supported by IC. 

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Format</b> </p> </th> 
   <th class="entry"> <p> <b> Pixel Type</b> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Compression</b> </p> </th> 
   <th class="entry"> <p> <b> Notes</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Windows Bitmap) </p> </td> 
   <td> <p> RGB | indexed </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> uncompressed | RLE </p> </td> 
   <td> <p> 5/6 bits/channel indicates support for 16-bit RGB (5-5-5 and 5-6-5 bits/channel). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated Postscript) </p> </td> 
   <td> <p> CMYK | RGB | gray </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | Binary | JPEG </p> </td> 
   <td> <p> Only EPS files generated by Photoshop are supported. </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> indexed </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> If present, the transparency value in the palette is converted to alpha. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB | gray </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | gray | grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> uncompressed | compressed </p> </td> 
   <td> <p> Merged image only; layers and extra channels are ignored. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> Bitmap data only; vector data is ignored. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | gray | grayA | indexed </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> compressed </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | gray | grayA | indexed </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> uncompressed | ZIP | LZW | JPEG | CCITT RLE | CCITT G3 | CCITT G4 | Packbits </p> </td> 
   <td> <p> With the exception of the first associated alpha channel, extra channels are ignored. </p> </td> 
  </tr> 
 </tbody> 
</table>

Embedded ICC profiles are recognized in EPS, JPG, PSD, PNG, and TIFF files.

Embedded paths and XMP metadata are recognized in EPS, JPG, PSD, and TIFF files.

## Examples {#section-3c1986b30315431989bd76b1ee5bef6d}

Convert a single image at best quality and keep it in the same folder:

`ic -convert src/myFile.png src/myFile.tif`

Convert all images in *`srcFolder`* to JPEG-encoded pyramid TIFFs and place in *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Convert all images in *`srcFolder`*. The encoded image data of JPG files is used for the full-resolution level, loss-less LZW compression for the remainder of the image pyramid of these images as well as for the entire output image of all non-JPG input files. The pixel types, embedded color profiles, XMP metadata, etc. are maintained.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
