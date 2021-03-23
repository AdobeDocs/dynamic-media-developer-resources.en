---
description: Request type. Specifies the type of data requested.


solution: Experience Manager
title: req

feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# req{#req}

Request type. Specifies the type of data requested.

 `req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> debug </span> </p> </td> 
  <td class="stentry"> <p>Run commands in debug mode. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> contents </span> </p> </td> 
  <td class="stentry"> <p>Return information about the objects in the vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>Run commands and return the rendered image. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>Return properties of the specified vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> map </span> </p> </td> 
  <td class="stentry"> <p>Returns image map data embedded in the vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> object </span> </p> </td> 
  <td class="stentry"> <p>Run commands and return the rendered image masked to the current object selection. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> props </span> </p> </td> 
  <td class="stentry"> <p>Run commands and return properties of the reply image. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> userdata </span> </p> </td> 
  <td class="stentry"> <p>Returns the contents of <span class="codeph"> vignette::UserData </span>. </p> </td> 
 </tr> 
</table>

Unless otherwise noted in the detailed descriptions, the server returns text responses with MIME type <text/plain>.

`debug`

Executes the specified commands and returns the rendered image. If an error occurs, error and debug information is returned instead of the error image ( `attribute::ErrorImagePath`).

`contents`

Returns an XML representation of the object hierarchy in the vignette, including selected object attributes. Other commands in the request are ignored.

`img`

Executes the specified commands and returns the rendered image. The reply data format and response type is determined by `fmt=`.

`imageprops`

Returns selected properties of the vignette file or catalog entry specified in the URL path. See [Properties](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) for a description of the reply syntax and response MIME type. Other commands in the request are ignored. The following properties are returned:

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Property </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expiration </span> </p> </td> 
   <td colname="col2"> <p>Double </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Expiration </span> or the default time to live. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Full resolution height in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>name/description of the profile associated with this vignette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 if the associated profile is embedded in the vignette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 if the vignette embeds path data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Modifier </span> or empty if not a catalog entry. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>Pixel type of the response image; may be 'CMYK', 'RGB' or 'BW' (for grayscale images). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Default print resolution in dpi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>Modification date/time (from <span class="codeph"> catalog::TimeStamp </span> or the vignette file). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Full resolution width in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>String </p> </td> 
   <td colname="col3"> <p>Vignette name (name string of the root vignette object). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Maximum object resolution in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> material resolution </a> units (typically pixels/inch). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Average object resolution in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> material resolution </a> units (typically pixels/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> material resolution </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Minimum object resolution in <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> material resolution </a> units (typically pixels/inch). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>Integer </p> </td> 
   <td colname="col3"> <p>Vignette file version number. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Returns image map data included in the vignette. By default, the map data for all outermost groups is returned. The map data for all innermost groups can be obtained with

`req=map&groupLevel=-1`

The map data is not scaled to `wid=` or `hei=` or otherwise modified. The response MIME type is `<text/xml>`.

The response data consists of a `<map>` element containing a set of `<area>` elements, similar to the HTML `<AREA>` tag.

Each `<area>` element includes the standard `type=` and `coord=` attributes, as well as a `name=` attribute, specifying the vignette group name or name path. Multiple `<area>` elements with the same name will be present if the masks of the corresponding object group has discontinuous regions.

In addition to the default attributes, vignettes can define additional attributes if so authored. Such custom attributes are defined as object group attributes. The names of custom attributes must begin with `map`. to be included in the `<area>` elements. For example, if the group attributes include `map.href=http://www.scene7.com`, the corresponding `<area>` element will include `href="http://www.scene7.com"`.

An XML document with an empty `<map>` element is returned if the vignette does not include map data.

`object`

Executes the specified commands and returns the rendered image masked by the residual object selection (the group or object selected with the last `sel=` or `obj=` command in the request). Typically used in conjunction with an image format which supports alpha (see [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). If an image format is used which does not support alpha, the areas outside the mask are black.

`props`

Executes the specified commands and returns vignette properties and group or object properties, rather than the rendered image. See [Properties](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) for a description of the reply syntax and the response MIME type. The default selection applies unless `obj=` or `sel=` is specified as well (see [ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

The following properties may be included in the response:

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Property </p> </th> 
   <th class="entry"> <p> Type </p> </th> 
   <th class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Reply image background color. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>Integer </p> </td> 
   <td> <p> Reply image height in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p>True if the ICC profile will be embedded in the reply image (see <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Shortcut name of the profile associated with the reply image (see <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> True if the reply image includes alpha. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> True if the reply image includes path data (see <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Reply image type, may be 'CMYK', 'RGB' or 'BW' (for grayscale images) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> Real </p> </td> 
   <td> <p> Print resolution (dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>Integer, boolean </p> </td> 
   <td> <p> JPEG quality and chroma flag (see <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Mime type for the reply image (see <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Reply image width in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Attributes string for the current selection. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Number of objects in the current selection. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Indent value of the current selection. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> String </p> </td> 
   <td> <p> Full name path of the current object selection. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> number of overlap objects in the current selection. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p>Number of renderable objects in the current selection. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Number of texturable objects in the current selection. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Current show/hide status of the current selection. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> Integer </p> </td> 
   <td> <p> Z-order value of the first overlap object in the current selection. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Returns the contents of `vignette::UserData`. The server will replace all occurrences of `'??'` in `vignette::UserData` with line terminators ( `<cr><lf>`). The reply is formatted as text data with the response MIME type set to <text/plain>.

If the object specified in the URL path does not resolve to a valid vignette map entry, or if the `vignette::UserData` is empty, the reply will only contain a line terminator ( `CR/LF`).

Any other commands in the request string are ignored.

## Properties {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Request command. May occur anywhere in the request string.

## Default {#section-00c593cbf1af4364b6b78812e6b93c64}

If the URL does not include an image path or modifiers, then:

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Otherwise, `req=img`

## See also {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) , [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0), [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85), [Properties](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 
