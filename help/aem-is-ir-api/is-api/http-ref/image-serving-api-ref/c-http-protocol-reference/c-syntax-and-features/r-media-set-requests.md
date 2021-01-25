---
description: Image Serving provides a mechanism for fetching a hierarchial text response (xml or json) which represents all of the resources and metadata associated with catalog ImageSet for a particular record.
seo-description: Image Serving provides a mechanism for fetching a hierarchial text response (xml or json) which represents all of the resources and metadata associated with catalog ImageSet for a particular record.
seo-title: Media set requests
solution: Experience Manager
title: Media set requests
topic: Dynamic Media Image Serving - Image Rendering API
uuid: af9fabcd-531d-43fb-bd97-269923bea5e8
---

# Media set requests{#media-set-requests}

Image Serving provides a mechanism for fetching a hierarchial text response (xml or json) which represents all of the resources and metadata associated with catalog::ImageSet for a particular record.

The viewers can use this mechanism to generate responses to inform the presentation of simple images, videos, video sets, swatch sets, spin sets, page sets (e-catalogs), and media sets.

## Request syntax {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

The set response for a `catalog::ImageSet` can be retrieved by using the `req=set` modifier and referencing the catalog record id in the net path. Alternately, the image set can be specified directly in the URL by using the `imageset=` modifier. If the `imageset=` modifier is used to specify the imageset, the entire value should be enclosed in curly braces in order to escape the image set value and ensure that any included modifiers are not interpreted as being part of the URL query string.

## Types of set responses {#section-93eb0a1f70344da2a888e56372ad3896}

The set mechanism supports the following types of responses:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>simple images </p></td> 
  <td class="stentry"> <p>An image record without <span class="codeph"> catalog::ImageSet</span> defined. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>simple videos </p></td> 
  <td class="stentry"> <p>A video record in the static content catalog. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>swatch sets </p></td> 
  <td class="stentry"> <p>A set of items consisting of a reference to an image record and an optional separate reference to an image record used as a swatch. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>hierarchical swatch sets </p></td> 
  <td class="stentry"> <p>A set of items consisting of a basic swatch item or a reference to a swatch set record. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>spin sets </p></td> 
  <td class="stentry"> <p>A set of items consisting of a simple list of image IDs. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>two-dimensional spin sets </p></td> 
  <td class="stentry"> <p>A set of items consisting of a simple image or a reference to a basic spin set. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page sets </p></td> 
  <td class="stentry"> <p>A set of items consisting of a list of up to three page images </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>media sets </p></td> 
  <td class="stentry"> <p>A set of items consisting of simple images, video sets, swatch sets, hierarchical swatch sets, spin sets, two-dimensional spin sets, page sets, and video assets. Each media set item can also contain an optional swatch. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>video sets </p></td> 
  <td class="stentry"> <p>A set of items consisting of a list of simple videos. </p></td> 
 </tr> 
</table>

## Outer set type detection {#section-3dd6e453528d46898e559d31458a59ba}

When an `req=set` request is received, the type of response to generate is determined by the value of `catalog::AssetType`. If `catalog::AssetType` is not defined, then the response type is determined by the following rules:

* If record is found in the image catalog AND `catalog::ImageSet` is defined

    * Assume e-catalog set if at least one entry in record Imageset field contains a colon 
    * Assume media set if at least one entry in record Imageset field contains two semi-colons. 
    * Assume image set if at least one entry in record Imageset field contains one semi-colon. 
    * Assume spin set if no entry contains colon nor semi-colon but at least one entry contains referenced set or in-line set (this is a 2D spin set). 
    * Assume unknown set if no entry contains colon nor semi-colon nor referenced set nor in-line set (i.e comma separated list of images).

* If record is found in both image AND static content catalogs

    * Assume video if file extension is in following set: mp3, mp4, flv, f4v, swf, xml 
    * Assumage image otherwise

* If record is found in static content catalog but NOT in image catalog

    * Assume video if file extension is in following set: mp3, mp4, flv, f4v, swf, xml 
    * Assume static otherwise

* If record in found in image catalog but NOT in static content catalog

    * Assume image

* If record is NOT found in the image catalog and NOT found in static content catalog

    * Assume file-based video if file extension is in following set: mp3, mp4, flv, f4v, swf, xml 
    * Assume file-based image otherwise

In all cases, the resultant xml response will conform to specified XML document with set root node corresponding to the detected type.

## Inner set type detection {#section-8f46490e467247e69ce284704def06f3}

When the outer set is detected as type media set, the response will contain a set of media set items corresponding to each media set entry in `catalog::ImageSet`. If the optional type parameter is specified for a particular media set entry, it will be mapped to an output type according to the following table:

|  Input type  | Output type  |
|---|---|
|  `img`  | `img`  |
|  `basic`  | `img`  |
|  `advanced_image`  | `img`  |
|  `img_set`  | `img_set`  |
|  `advanced_image_set`  | `img_set`  |
|  `advanced_swatchset`  | `img_set`  |
|  `spin`  | `spin`  |
|  `video`  | `video`  |
|  `video_set`  | `video_set`  |
|  `static`  | `static`  |
|  `ecat`  | `ecat`  |

If the optional type parameter for a particular media set entry is not specified or corresponds to an unsupported type, the media set item type is auto-detected using the same rules as were applied at the outer set level.

## XML specification {#section-c1bd60948ef545759a16885bb6fcc607}

The returned xml response conforms to the following specification:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

The `labelkey=` modifier is used together with the `catalog::UserData`field to generate labels for images and swatches. The `catalog:UserData` field is parsed as a set of key/value pairs and the labelkey indexes in to this set to retrieve the value for the given key. This value is then returned in the *`l`* attribute for the *`s`* and *`i`*.

## Enforced restrictions {#section-b9f042873bee45a5ae11b69fd42f2bca}

In order to limit the size of the response and prevent self-referential issues, the maximum nesting depth is controlled by the server property `PS::fvctx.nestingLimit`. If this limit is exceeded, an error is returned.

In order to limit the size of the xml responses for large e-catalog sets, private metadata is suppressed for brochure set items according to the server property `PS::fvctx.brochureLimit`. All private metadata associated with the brochure will be exported until the brochure limit is reached. Once the limit is exceeded, private maps and userdata will be suppressed and a corresponding flag will be set to indicate which type of data was suppressed.

Nested media sets are not supported. A nested media set is defined as a media set which contains a media set item of type media set. If this condition is detected, an error will be returned.

## Examples {#section-588c9d33aa05482c86cd2b1936887228}

For sample XML responses for `req=set` request, refer to Properties page under HTML Examples header.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## See also {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) 

