---
description: Image Serving supports color space conversions based on color space profiles conforming to the ICC (International Color Consortium) specification.
solution: Experience Manager
title: Image Serving color management
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
---
# Image Serving color management{#image-serving-color-management}

Image Serving supports color space conversions based on color space profiles conforming to the ICC (International Color Consortium) specification.

## Default color spaces {#section-8cfe60808bce49968091995e4e521dba}

Each image catalog (and the default catalog) can define a set of ICC profiles which constitute the default color spaces for this catalog - one input and one output profile each for gray-scale, RGB, and CMYK data. See ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`, and ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## Input color space {#section-9f08e2c1b6aa4fe4815be174972c1944}

Source images may embed ICC profiles to define the input color space. If no profile is embedded in a source image, `attribute::IccProfileSrc*` of the applicable image catalog corresponding to the pixel type of the source image will be used. If this attribute is not defined in the image catalog, `attribute::IccProfile*` is used. If that catalog attribute is not defined either, the image is not color-managed and only naïve transforms will be applied.

## Output color space {#section-b517bca622b64dcfa7defba6035d0716}

The color space of the final image result of a request is defined with the `icc=` command. If `icc=` is not specified, the default output color space (from the request's main catalog) which corresponds to the pixel type of the output image is used as the output color space. If no output profile is defined in the main or default catalog, and if the base layer is an image with an embedded profile matching the output pixel type, then that profile is used for the output color space. Otherwise, the output color space remains undefined -- only naïve color conversions will be applied when converting between pixel types and no color profile can be embedded in the output image.

The output color space of a nested/embedded Image Serving request is always the same as the output color space of the outer, embedding request.

## Solid colors {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Color values specified with `color=`, `bgcolor=`, or the RTF command `\iscolortbl` will be associated with the input color space if the color value includes the suffix 'S', otherwise they are associated with the output color space. Color values specified with `bgc=` or the RTF commands `\colortbl` and `\cmykcolortbl` are always associated with the corresponding default or actual output color space.

>[!NOTE]
>
>At this time, `bgc=` does not fully participate in color management-the 'S' suffix is ignored when specified with `bgc=`, and naïve conversion is applied when the pixel type of the color value specified with `bgc=` differs from the pixel type of the output image. Otherwise, `bgc=` is associated with the actual output color space.

## Nested and embedded requests {#section-bdda638c31504f26a77e51ebb1ea6e3b}

The output color space for nested IS requests and embedded IR requests is automatically set to the output color space of the outermost request, unless the nested request specifies an explicit output color space with `icc=`. In addition, nested/embedded requests also inherit the default output color spaces from the main catalog of the outermost request, to ensure consistent handling of solid color values.

## Color space conversion {#section-ca87b80b8e364ea59d8a92d87121b0fb}

Image Serving generally attempts to delay color conversions during processing. If all layers of an image have the same layer color space, conversion to the output color space is done after merging and final scaling. If multiple layer color spaces are involved, each layer is transformed to the output color space prior to merging.

>[!NOTE]
>
>The commands `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=`, and `op_saturation=` are RGB operations. These operations maintain color fidelity only if the layer color space has RGB pixel type. If other than RGB, the data is converted to RGB using naïve color conversion, and the result will have limited color fidelity. The layer color space for such layers should be considered indeterminate.

Color conversion options are provided with `icc=` or, if `icc=` is not specified, with `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation`, and `attribute::IccDither`.

## Embedding color profiles {#section-261ebbae5ce046589a776ca972380052}

The ICC color profile of the output color space, if available, can be embedded into the response image by specifying `iccEmbed=`.

## Managing ICC profiles {#section-eb210e4b44e64e2c8b80ee59216c5555}

All color profiles used by the server must conform to the ICC specification. ICC profile files typically have an [!DNL .icc] or [!DNL .icm] file suffix and are co-located with image data files.

While output profiles can be specified by file path/name in the `icc=` command, it is recommended to register all profile files in the ICC Profile Map of the default catalog or image catalog and use shortcut identifiers ( `icc::Name`) instead of file paths.

All ICC profiles referenced in `catalog::IccProfile` and in `attribute::IccProfile*` must be registered in the ICC Profile Map of the image or default catalog.

## Restrictions {#section-fb50ede40b124b89b30679da29782ab5}

Only CMYK, RGB, and gray-scale color spaces are supported at this time.

## Included ICC color profiles {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

Image Serving includes most standard Adobe ICC profiles in the default image catalog. These profiles can be accessed by either their common names (e.g. as seen in Photoshop) or with a somewhat shorter identifier. The following table lists all standard ICC profiles. When referencing a profile in the `icc=` command by its common name, spaces must be encoded as `%20`.

Additional profiles may be added to the standard profiles, either to the default catalog or a specific image catalog. Refer to the [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) for details.

>[!NOTE]
>
>The following table applies to *Dynamic Media Hybrid* only (running in `dynamicmedia` run mode).

|Identifier|Common name|File name|
|-- |-- |-- |
|**RGB**|||
|`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB`|CIE RGB|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC (1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto`|ProPhoto RGB|ProPhoto.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm|
|`WideGamutRGB`|Wide Gamut RGB|WideGamutRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`CoatedGraCol`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc|
|`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`NewsprintSNAP2007`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc|
|`PS4Default`|Photoshop 4 Default CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 Default CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|U.S. Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|U.S. Sheetfed Uncoated v2|USSheetfedUncoated.icc|
|`UncoatedFogra29`|Uncoated FOGRA29 (ISO 12647-2:2004)|UncoatedFOGRA29.icc|
|`WebCoated`|U.S. Web Coated (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`WebCoatedGrade3`|Web Coated SWOP 2006 Grade 3 Paper|WebCoatedSWOP2006Grade3.icc|
|`WebCoatedGrade5`|Web Coated SWOP 2006 Grade 5 Paper|WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|U.S. Web Uncoated v2|USWebUncoated.icc|

The following table applies to *Dynamic Media Classic Image Serving* and *Dynamic Media* (running in `dynamicmedia_scene7` run mode).

|Identifier|Common name|File name|
|-- |-- |-- |
|**RGB**|||
|`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB|CIE RGB`|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC (1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm|
|`WideGamutRGB`|Wide Gamut RGB|WideGamutRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc|
|`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`PS4Default`|Photoshop 4 Default CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 Default CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|U.S. Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|U.S. Sheetfed Uncoated v2|USSheetfedUncoated.icc|
|`UncoatedFogra29`|Uncoated FOGRA29 (ISO 12647-2:2004)|UncoatedFOGRA29.icc|
|`US Newsprint (SNAP 2007)`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc|
|`WebCoated`|U.S. Web Coated (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`Web Coated SWOP 2006 Grade 3 Paper`|Web Coated SWOP 2006 Grade 3 Paper|WebCoatedSWOP2006Grade3.icc|
|`Web Coated SWOP Grade 5 Paper`|Web Coated SWOP 2006 Grade 5 Paper|WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|U.S. Web Uncoated v2|USWebUncoated.icc|

## See also {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](http://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
