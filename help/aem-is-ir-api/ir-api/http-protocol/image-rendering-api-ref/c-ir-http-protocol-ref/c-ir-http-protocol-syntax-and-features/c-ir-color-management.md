---
description: Image Rendering supports color space conversions based on color space profiles conforming to the ICC (International Color Consortium) specification.
solution: Experience Manager
title: Image Rendering color management *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
---
# Image Rendering color management *{#image-rendering-color-management}

Image Rendering supports color space conversions based on color space profiles conforming to the ICC (International Color Consortium) specification.

 **Restrictions**

Only CMYK, RGB, and gray-scale color spaces are supported at this time.

Cabinet style files (.vnc) and window coverings style files ( [!DNL .vnw]) are not color-managed and are assumed to exist in the working color space.

**See also**

[International Color Consortium](https://www.color.org/index.xalter) , [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , ICC Profile Maps

## Default color spaces {#section-8ce27edf42e746febe4654f8f19b9c0c}

Each image catalog (and the default catalog) can define a set of ICC profiles. These profiles constitute the default color spaces for this catalog - one input and one output profile each for gray-scale, RGB, and CMYK data ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray`, and `attribute::IccProfileSrcCmyk`).

The default color space for a particular image or other object is selected from the catalog default profiles based on the pixel type of the image.

## Input color space {#section-660f661a7e954df4b451e34134195276}

Material images may embed ICC profiles to define the input color space. If no profile is embedded in a source image, `attribute::IccProfileSrc*` of the applicable image catalog corresponding to the pixel type of the source image is used. If this attribute is not defined in the image catalog, `attribute::IccProfile*` is used. If that catalog attribute is not defined either, the image is not color-managed and only naïve transforms are applied.

## Working color space {#section-645d9cfa5b0347a190a0ece218f5b5e1}

Typically, the working color space is defined by the ICC color profile embedded in the vignette. If the vignette does not include a profile, the default RGB input profile ( `attribute::IccProfileSrcRgb` of the session catalog) is used for the working color space.

All render operations are executed in the working color space.

**Important:** The ICC profile for the working color space must support input and output transformations. If an output-only profile is used as a working color space IR is unable to convert materials to it. Such a color profile may still be used if materials exist in the same working color space. Attempting to apply materials in other color spaces fail.

## Explicit color values {#section-31727bf1b23e477ca92572fbbf422d2f}

RGB color values specified with `color=`, `bgc=`, `catalog::BgColor`, and `catalog::Color` are assumed to exist in the current working color space.

## Material data files {#section-33f7a170a6664c02b8479fb89cc0aea3}

Material image files (texture and decal images) can have RGB, gray-scale, or CMYK pixel type and can embed a color profile. If no color profile is embedded, the default input color space is associated with the image (for example, the color profile from the material catalog which corresponds to the pixel type of the image).

Material images obtained from nested Image Serving or Image Rendering requests typically include a color profile. If this is not the case, the images are associated with the default input color space corresponding to the pixel type.

If the color space of the image file is different from the working color space, accurate color conversion is used to convert to the working color space. Naïve type conversion is used when no profile is embedded and no default input profile is defined.

Other material data files, such as cabinet style files ( [!DNL .vnc]) or window covering files ( [!DNL .vnw]) do not embed color profiles and are always assumed to be in the working color space.

## Output color space {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

All render operations take place in the working color space. If the request specifies a different color profile with the `icc=` command, the data is converted to that color space just before it is encoded and returned to the client. When color management is disabled, naïve conversion is used if necessary to convert to gray-scale or CMYK.

## Embedded color profiles {#section-5ff733832d38429fbe02b3c1e9bb94a9}

The color profile associated with the rendered image can be embedded into the response image by specifying `iccEmbed=` for the request.

If `icc=` is not specified, the ICC profile for the working color space is embedded. No profile is embedded if color management is disabled and no profile was specified with `icc=`.

## ICC profiles {#section-afeb76068b5042adb83261638e450140}

All color profiles used by the server must conform to the ICC specification. ICC profile files typically have an [!DNL .icc] or [!DNL .icm] file suffix and are co-located with material data files.

While output profiles can be specified by file path/name in the `icc=` command, it is recommended to register all profile files in the ICC Profile Map of the default catalog or a specific material catalog and use shortcut identifiers ( `icc::Name`) instead of file paths.

Working profiles must be registered in the ICC Profile Map of the material catalog or the default catalog.
