---
description: Select object by pixel location.
seo-description: Select object by pixel location.
seo-title: sel
solution: Experience Manager
title: sel
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2a679284-9da4-44b6-b495-8e1a47296e7c
---

# sel{#sel}

Select object by pixel location.

 ` sel= *`x`*, *`y`*[, *`level`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>Pick location coordinates in pixels (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> level </span> </p> </td> 
  <td class="stentry"> <p>Group level (int). </p> </td> 
 </tr> 
</table>

Selects the group or object at the pixel coordinates specified by *`x, y`* and starts a new MSS. If no selectable object is at the pick location, or if the pick location is not valid, the action specified by `attribute::OnFailSel` is taken.

*`level`* specifies whether to select the outermost group, or drill-down to a nested group or object. If *`level`* is not specified, the outermost group is selected. Set to 1 to select one group level below the outermost group. Set to a large number (such as 99) to select the innermost selectable object or group.

## Properties {#section-8f27e84d88734a62a5e398e0c9972bdc}

Selection command; MSS delimiter. The object selection is persistent until another object is selected, either with `obj=` or `sel=`.

*`x, y`* must be in the range 0, 0 (top-left corner of the image) to *`wid`*-1, *`hei`*-1 (bottom, right corner of the image), where *`wid`* and *`hei`* is the size of the unscaled vignette view.

If specified, *`level`* must be 0 or larger.

## Default {#section-e13c705a3e76468894b4ec190ed8a893}

None for *`x, y`*. *`level`* defaults to 0.

## See also {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513) 
