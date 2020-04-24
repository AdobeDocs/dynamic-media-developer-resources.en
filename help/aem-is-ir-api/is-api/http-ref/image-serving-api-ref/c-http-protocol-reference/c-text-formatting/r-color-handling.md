---
description: The RTF specification permits RGB color values specified with &bsol;colortbl. Each component is provided separately with the &bsol;red, &bsol;green, and &bsol;blue commands.
solution: Experience Manager
title: Color handling
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
---

# Color handling{#color-handling}

The RTF specification permits RGB color values specified with `\colortbl`. Each component is provided separately with the `\red`, `\green`, and `\blue` commands.

The proprietary RTF extension command `\cmykcolortbl` allows specifying CMYK colors, with each color component provided with the `\cyan`, `\magenta`, `\yellow`, and `\black` commands.

Color component values for `\colortbl` are in the range 0 to 255. Component values for `\cmykcolortbl` are in the range 0 to 100.

The RTF extension command `\*\iscolortbl`, supported by `textPs=`, provides a way to specify a color table with standard Image Serving color values, with full RGB, gray, CMYK and alpha support. It has the following syntax:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* one or more IS color values, separated with ';'

More than one type of color table may be specified in the same `text=` or `textPs=` RTF string. Each color table can have a different number of entries. Image Serving will attempt to find colors in this order: `\iscolortbl` before `\cmykcolortbl` (only if the pixel type of the text layer is CMYK) before `\colortbl`. For `textPs=` only, colors are accurately converted between CMYK and RGB, if so required (e.g. when RGB colors are specified but CMYK output is required). If no color for a particular index value is found, the default color (black) is used.

Refer to [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) for a description of the syntax of IS color values.

## Restrictions {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` does not support `\*\iscolortbl`. `textPs=` does not support `\cmykcolortbl`.

Color selections are ignored when rendering Photofonts.

## Example {#section-0f166bb72bd44479be01131077851142}

Allow three text colors to be controlled with variables, while still displaying the color default value when the RTF string is opened in a standard RTF text editor.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…` 
