---
description: Layer size. Specifies the size or maximum layer size for a layer, before rotate=, perspective=, and extend= are applied to the layer.
seo-description: Layer size. Specifies the size or maximum layer size for a layer, before rotate=, perspective=, and extend= are applied to the layer.
seo-title: size
solution: Experience Manager
title: size
topic: Scene7 Image Serving - Image Rendering API
uuid: c9c13062-7974-4dd9-aff4-f9502bcf442e
---

# size{#size}

Layer size. Specifies the size or maximum layer size for a layer, before rotate=, perspective=, and extend= are applied to the layer.

 ` size= *`width`*, *`height`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span>, <span class="varname"> height </span> </span> </p> </td> 
  <td class="stentry"> <p>Layer size constraint in pixels (int, int, 0 or greater). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>Layer size constraint normalized relative to the layer 0 size (real, real, 0.0…1.0). </p> </td> 
 </tr> 
</table>

When specified for an image layer, size= constrains the layer image's width, or height, or both. The image will be scaled to be no larger than `size=`. If a normalized size is specified, it is relative to the size of layer 0. If both *`width`* and *`height`* are specified, the source image is scaled (after `crop=` is applied) so that neither dimension exceeds the specified size. The aspect ratio of the source rectangle is maintained in all cases. Either *`width`* or *`height`* may be set to 0; in this case the value is calculated by the server based on the aspect ratio of the image.

When specified for a text layer, `size=` specifies the text box size. *`width`* is required; *`height`* may be set to 0, in which case the height of the laid out text is used as the layer height. By default, the text layout engines insert line breaks to ensure that text always fits horizontally into the available space. If *`height`* is specified, lines which do not fit into the available space will be clipped ( `text=`) or omitted ( `textPs=`). `text=` supports additional fit modes; refer to `textAttr=` for details.

When specified for a solid color layer, `size=` defines the exact layer size; both values must be specified (unless a mask is provided). If `mask=` is also specified, the mask image will be sized to fit `size=` the same way images are scaled in image layers.

## Properties {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Layer attribute. Applies to layer 0 if `layer=comp`. `sizeN=` is not permitted for `layer=0` or `layer=comp`. `sizeN=` is permitted for `layer=0` and `layer=comp` only in catalog records which define watermark images. In this case, `sizeN` defines the scaling of the watermark image relative to the composite image to which the watermark is being applied. If `size=` is specified, `res=` and `scale=` are ignored for this layer. Ignored by effect layers.

## Default {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`, the layer size is unconstrained. For image layers, the layer size is then determined based on the layer image size after any `crop=`, `scale=`, or `res=` operations have been applied. For text layers, if `size=` is not specified, the layer will be sized automatically to fit the rendered text.

Solid color layers require either a fully specified `size=`, a `mask=`, or `clipPath=`.

## Example {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

See [Example A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## See also {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f) 
