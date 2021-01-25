---
description: Layer Clip Path. Specifies a clip path for the current layer.
seo-description: Layer Clip Path. Specifies a clip path for the current layer.
seo-title: clipPath
solution: Experience Manager
title: clipPath
topic: Dynamic Media Image Serving - Image Rendering API
uuid: fe84cf7a-63af-47d3-ae4f-2122f2f0a262
---

# clipPath{#clippath}

Layer Clip Path. Specifies a clip path for the current layer.

 `clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Name of path embedded in layer source image (ASCII only). </p></td> 
 </tr> 
</table>

Any parts of the layer that fall outside the area defined by `clipPath=` are rendered transparent.

`*`pathName`*` is the name of a path embedded in the layer source image. The path is automatically transformed to maintain relative alignment with the image contents. If more than one `*`pathName`*` is specified, the server clips the image to the intersection of these paths. Any `*`pathName`*` not found in the source image is ignored.

>[!NOTE]
>
>Only ASCII strings are supported for `*`pathName`*`.

`*`pathDefinition`*` allows specifying explicit path data in layer pixel coordinates.

If `size=` is specified and not 0,0, the layer is presized. In this case, path coordinates are relative to the upper-left corner of the layer rectangle and the layer is positioned based on `origin=` or its default. Any regions of the path outside the layer rectangle remain transparent.

If `size=` is not specified for a solid color or text layer, the layer is considered self-sizing with the extent of the path determining its size. If `origin=` is not specified, it defaults to (0,0) of the path coordinate space. This effectively allows path coordinates to be specified relative to the origin of layer 0.

>[!NOTE]
>
>`scale=`, `rotate=`, and `anchor=` commands are not permitted for self-sizing solid color layers.

`*`pathDefinition`*` accepts a string similar to the value of the `d=` attribute of the SVG `<path>` element, except that commas are used instead of spaces to separate values. `*`pathDefinition`*` can include one or more closed-loop sub-paths.

The following path commands are supported in `*`pathDefinition`*`: 

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Command</b> </th> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> moveto absolute </p> </td> 
   <td> <p> Start a new subpath at x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> moveto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto absolute </p> </td> 
   <td> <p> Draw a line from the current position to x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto absolute </p> </td> 
   <td> <p> Draw a Bezier curve from the current position to x,y. x1,y1 is the control point at the beginning of the curve and x2,y2 is the control point at the end of the curve. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Close the current subpath with a straight line. </p> </td> 
  </tr> 
 </tbody> 
</table>

Uppercase commands indicate that the coordinate values are in absolute pixel positions (relative to the upper-left of the layer rectangle). Pixel offsets follow lowercase commands relative to the current position.

'm' or 'M' always starts a new subpath. Subpaths are closed automatically (with a straight line) if 'Z' or 'z' is not specified at the end.

If a subpath begins with a relative moveto ('m'), it is relative to one of the following:

* The starting point of the previous subpath, if it was closed with 'z' or 'Z'. 
* The end point of the previous subpath, if it was not closed explicitly. 
* 0,0, if this is the first subpath.

## Properties {#section-d4127db0dac54e3cbd44f7ea1e001960}

Layer attribute. Applies to the current layer or to the composite image if `layer=comp`. Effect layers ignore it.

`clipPathE=` is ignored if no path with the specified name is found in the layer source image, or if the layer source is not an image.

## Default {#section-076c35ea37fa4a44ada253b4c2dec1dd}

None, for no additional clipping of the layer.

## See also {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac) 
