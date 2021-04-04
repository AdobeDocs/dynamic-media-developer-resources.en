---
description: Image Serving supports Scalable Vector Graphics (SVG) files as source data. Conformance with SVG 1.1 is required.
solution: Experience Manager
title: SVG support
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
---
# SVG support{#svg-support}

Image Serving supports Scalable Vector Graphics (SVG) files as source data. Conformance with SVG 1.1 is required.

Image Serving only recognizes static SVG contents; animations, scripting, and other interactive contents are not supported.

SVG can be specified wherever image files are permitted (URL path, `src=`, and `mask=`). After the content of the SVG file is rasterized, it is handled just like an image.

Similar to images, SVG files can be specified as image catalog entries or as relative file paths.

## Substitution variables {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` substitution variables may be included in the SVG file in the value strings `<text>` elements and any element attribute.

Important Variables in the query portion of embedded Image Serving requests are not substituted directly. Instead, all available variable definitions are appended to the request, which allows Image Serving to substitute variables when parsing the request.

See [Substitution Variables](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) for additional information.

## Image references {#section-a7680f9e6aca4b1a83560637cc9fac66}

Images may be inserted into SVG using the `<image>` element. Images referenced by the `xlink::href` attribute of the `<image>` element must be valid image serving requests. Foreign URLs are not permitted.

Specify either a complete Image Serving request, starting with `http://`, or a relative url, starting with `/is/image`. If a full HTTP path is specified, the domain name will be removed from the path to convert to the relative format. Using a full HTTP path may be of advantage, as it allows the file to be previewed with a third-party SVG renderer.

>[!NOTE]
>
>Support for rendering images in this release of Image Serving is limited. Referencing images from within SVG should be used only in situations where traditional Image Serving layering and templating mechanisms are insufficient to achieve the desired result. Under no circumstances should SVG be used to generate multi-image composites.

>[!NOTE]
>
>Images embedded in SVG are not resized automatically at this time. Make sure that all image hrefs include the necessary Image Serving commands to set the desired image size (e.g. `wid=`). If the image size is not set explicitly, `attribute::DefaultPix` will be applied.

## Color management {#section-ea76e2bc4e1842638aa97a2d470c8a68}

All color values embedded in SVG files and passed to SVG templates via substitution variables are assumed to exist in the `sRgb` color space.

No color conversion is performed when images are embedded into the SVG. To ensure color fidelity, make sure to specify `icc=sRgb` for all embedded image requests.

After rasterization, the SVG image participates in color management just like any other image.

## Example {#section-036cdd45abd449849ee00a8f21788c28}

The following SVG template illustrates image references and use of variables.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

This SVG template might be used as follows:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrictions {#section-daa5eccd07204aaf993be41e87822d54}

SVG files must be stand-alone and must not reference any secondary files or resources, with the exception of external images referenced with Image Serving or Image Rendering requests (see above).

Only static content is rendered. Animation, interactive features, such as buttons, etc. may be present but may not be rendered as expected.

ICC profile-based color specifications are not supported at this time.

`<script>` elements may be present but are always ignored.

## See also {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG 1.1 Specification](http://www.w3.org/TR/SVG11/)
