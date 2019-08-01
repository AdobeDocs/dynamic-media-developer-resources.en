---
description: There are some restrictions and known issues that should be considered when using Scene7 Image Serving.
seo-description: There are some restrictions and known issues that should be considered when using Scene7 Image Serving.
seo-title: Restrictions and known issues
solution: Experience Manager
title: Restrictions and known issues
topic: Scene7 Image Serving - Image Rendering API
uuid: 58ba48c0-d51c-40bc-b054-8fd21a9cc7d8
index: y
internal: n
snippet: y
---

# Restrictions and known issues{#restrictions-and-known-issues}

There are some restrictions and known issues that should be considered when using Scene7 Image Serving.

## Documentation errata {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* The number of lines will not exceed the maximum of the `\copyfitmaxlines` setting and the number of explicit lines in the text input. 
* Matching curly brackets and parenthesis are required in image sets. If curly brackets and parenthesis are not matched, they need to be URL encoded. 
* Server-side global response time alert includes error responses. 
* The `id=` command is currently required when using the `rect=` command with an image or mask request.

## Known differences textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Synthetic italic are rendered less slanted than when using `text=`. 
* Underlining is a little lower and thinner than when using `text=`. 
* `\expnd` and `\expndtw` used with high negative values cause characters to be placed in front of each other when using `text=`. 

* `\charscaley` scales differently than when using `text=` but does not affect the line height. 

* If the last line of text does not fit, the entire line is dropped instead of appearing as cutoff. 
* `\slmult` and `\sl` behave differently from MS Word and `text=`, they simply take effect for the current and subsequent paragraphs. 

* `\sb` applies to the first paragraph for both MS Word and `text=`, Adobe InDesign and Photoshop do not do this. 

* `\sa` applies to the last paragraph for both MS Word and `text=`, Adobe InDesign and Photoshop do not do this.

## Backwards compatibility {#section-a76842f751944f4fb664af296d064122}

* Escaping the underscore character ( `\_`) in an RTF string does not work with all fonts using `textPs=` 

* Supporting not case sensitive macro handling. 
* Catalog cache has been reduced from 60 seconds to 10 seconds. 
* The error redirect feature now only redirects requests referencing corrupt images, fonts, color profiles, and images that are published in a catalog, but not found on disk. 
* `posN=`, `anchor=`, `anchorN=`, `origin=`, and `originN=` now return a parsing error if any of the modifier values are greater than 2147483648. 

* Encoding of nested requests is not supported. Transition to the new behavior and unencode any nested request values found in URL requests on your site and in your company catalogs. 
* DefaultImage now applies thumbnail attributes when using `req=tmb`. 
* In previous versions using `flip=`, the image was never repositioned regardless of what the anchor point was.

## Restrictions applicable to third-party libraries {#section-79768b96bf634e44ab672c5b893f343d}

The Digimarc library refuses to apply a Digimarc watermark to an image if one is already detected. If enough editing is done to a master image, the Digimarc library may still be able to recognize that the watermark was applied. However, it may not be able to read that information. This results in a new image where the original Digimarc information that was applied to the original image cannot be obtained. Image Serving can now apply the Digimarc watermark defined in the company catalog.

## Restrictions applicable to both Image Serving and Image Rendering {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Image Serving and Image Rendering may not take full advantage of all CPUs when more than 4 CPUs are available. Simulate your traffic on these machines to see how advantageous it is with more than 4 CPUs. 
* Remote URLs returning a redirect (HTTP statuses 301, 302, or 303) are rejected. 
* When configuring `errorRedirect.rootUrl` the IP address defined in this property needs to be included in the ruleset `<addressfilter>` tag value on that server.

  *Example*:

  Server A has defined `errorRedirect.rootUrl=10.10.10.10` .

  Server B, that has the IP address of 10.10.10.10, sets the `<addressfilter>` tag value in the ruleset file to include its IP address (10.10.10.10). 

* Point text and text path with positioning may exhibit clipping. 
* `text=` only applies `\sa` and `\sb` to the entire text block and not per paragraph. 

* When using one company defined in the URL and another company defined for the `src=` or `mask=` modifier, you must prefix a forward slash to the company defined for `src=` or `mask=` for this form of request to work.

  *Example*:

  `/is/image/MyCompany?src=/YourCompany/MyImage` .

  Instead of: `/is/image/MyCompany?src=YourCompany/MyImage` . 

* Non-Pyramided Tiff or vignette requests produce a similar error message to

  *"Image C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt has no valid DSF, and area of 2.25MPixel exceeds max of 2MPixel"* .

  Best practice is to use pyramided Tiffs and vignettes. If you have a need to use non-pyramided tiffs or vignettes, follow the instructions below to increase the size limit.

  *Work around*:

  For Image Rendering non-pyramided vignettes, increase the property value for IrMaxNonPyrVignetteSize in the [!DNL  *[!DNL install_root]*/ImageServing/bin/ ImageServerRegistry.xml] configuration file.

  For Image Serving non-pyramided TIFFs, increase the property value for `MaxNonDsfSize` in the [!DNL  *[!DNL install_root]* /ImageServing/bin/ ImageServerRegistry.xml] configuration file. 

* Adobe Photoshop CS3 does not save layered PSD files by default a composite image.

  *Symptoms*:

  The Adobe Photoshop CS3 layered PSD file displays as black with text stating, "This layered Photoshop file was not saved with a composite image." for the Image Serving reply image or in IPS.

  *Workaround*:

  Save the Adobe Photoshop CS3 file with maximize compatibility turned on. 

* Assigning ICC Profile to a CMYK/JPEG reply image causes colors to be inverted in some browsers.*Work around*:

  Change reply image format by using `fmt=` 

* The size of HTTP response image data-after compression, including file header-is limited to 16 MB. 
* " .." is not permitted in any path element in HTTP requests. 
* Uninstall may remove user-created or modified file from *[!DNL install_root]* or any sub folder. Copy such files to a different location before uninstalling.

## Restrictions applicable only to Image Serving {#section-b08ad535e4454265b8157dec244c4faf}

* Foreground colors in the RTF ( `\cf`) command are not supported for PhotoFont text. 
* Synthesizing bold, italic, and bold/italic will be rejected as an error for PhotoFont text. 
* Vertical text flow is not supported for PhotoFont text. 
* 16bpc PNG images are not supported for PhotoFont text. 
* Color corrections for PNG images with embedded color profiles use hard-coded options. Render intent is relative colorimetric and Blackpoint compensation is turned on for PhotoFont text. 
* File-based lookup is not supported when locale translation is enabled in company [!DNL ini] file. 
* Image Serving does not write non-closed Photoshop paths correctly. 
* Image Serving does not currently support processing of TIFF files exported using Adobe Media Encoder 4.0.1 or earlier. Adobe Media Encoder is included with Premiere Pro CS4, After Effects CS4 and Creative Suite 4 Production Premium. 
* Using `text=` with self-sizing layers does not support RTF strings that use more than one setting for line justification.

  *Example*

  RTF string cannot use both left and right line justification for a self-sizing text layer. 

* SVG has its own property for the font lookup path of referenced fonts that are not embedded in the SVG file.

  *Symptoms*

  Rendered SVG images that contain font definitions are using the incorrect font.

  *Workaround*

  Set the property `svgProvider.fontRoot=` in [!DNL  *[!DNL install_root]* /ImageServing/conf/PlatformServer.conf] . 

* Crop is currently using `bgColor=` instead of `color=` to fill any newly extended area. 

* Color conversion may not be correct when `bgColor=` does not match the base color space involving color profiles. 
* Outer layer effects are not rendered if the layer does not have a mask or alpha data.

## Restrictions applicable only to Image Rendering {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Decals and wall materials are not removable. 
* The size of textures is limited relative to the size of the vignette view. In rare circumstances, the default limit of 425% of the view size may interfere with an application using very large non-repeatable textures. If it is not possible to change the application or contents to work within the pre-defined limitations, the percentage can be increased as follows. Using a text editor, open [!DNL  *[!DNL install_root]*/ImageServing/conf/ImageServerRegistry.xml], locate `IrMaxTextureSizeFactor` and enter a new percentage value. The change takes effect immediately without restarting the Image Server. 

* The JavaScript engines in Netscape and Opera cache response data even if the nocache header is set. This interferes with proper functioning of stateful requests.

  *Workaround*

  Append a timestamp or other unique identifier to the request string, such as `"&.ts=currentTime`.

## Restrictions applicable only to utilities {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`sometimes crashes with a segmentation fault when stopped with a `control-c`. 
