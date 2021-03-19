---
description: Image Map Data. Provides image map data for this layer. Overrides any data from catalog Map for this layer.
seo-description: Image Map Data. Provides image map data for this layer. Overrides any data from catalog Map for this layer.
seo-title: map
solution: Experience Manager
title: map
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# map{#map}

Image Map Data. Provides image map data for this layer. Overrides any data from catalog::Map for this layer.

 `map=[ *`string`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Image map data for this layer in layer coordinates. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Image map data for this layer in source image coordinates. </p></td> 
 </tr> 
</table>

An empty string indicates that this layer should not provide an image map. The string must be properly HTTP-encoded to avoid parsing issues.

All ampersand (&) characters occurring in *`string`* must be http-encoded.

While `mapA=` and `catalog::Map` specify map data in source image coordinates, `map=` assumes layer coordinates relative to the top, left corner of the layer rectangle (after `rotate=` and `extend=` have been applied).

The output image map is always clipped to the layer rectangle. If the `shape` attribute is omitted or set to `default`, the entire layer rectangle is used as the image map area.

## Properties {#section-a18d9ea95c71414a905a68b8839c0843}

Layer attribute. When applied to `layer=comp`, the specified map data is layered behind all other image maps. Ignored unless `req=map`. Ignored by effect layers. `mapA=` is ignored if `map=` is specified as well.

## Default {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` is used if `map=` is not specified.

## Example {#section-cd7691c94f984222845c86dcb0051ce8}

Define a rectangular image map for a simple text layer:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

An `AREA` element with (mostly) default attributes is used to insert the map area for the entire layer rectangle.

## See also {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Image Maps](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) 
