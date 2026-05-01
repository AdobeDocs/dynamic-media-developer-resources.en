---
description: IS provides mechanisms to simplify use of HTML image maps. The JAVA-based and Flash-based viewers in IS also include limited support for image maps.
solution: Experience Manager
title: Image maps
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
TQID: https://experienceleague.adobe.com/qYmqWMAjzvpjFjsb9hLu-b1DlIdMl-nN9dHCWkqpzw0
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Image maps{#image-maps}

IS provides mechanisms to simplify use of HTML image maps. The JAVA-based and Flash-based viewers in IS also include limited support for image maps.

Source image maps are provided to IS either by way of `catalog::Map` or with the `map=` command, and processed maps are retrieved using the `req=map` command.

An image map consists of one or more HTML AREA elements, properly delimited with '<' and '>'. If provided by way of catalog::Map, all pixel coordinates values are assumed to be in the original image resolution and relative to the top left corner of the (unmodified) source image. When provided by way of a `map=` command, the coordinate values are assumed to be layer coordinates, relative to the top-left corner of the layer (after `rotate=` and `extend=`).

>[!NOTE]
>
>% coordinates are not permitted at this time and may be processed incorrectly.

IS generates a composite image map from the source image maps of each constituent layer by applying the spatial transformations (such as scaling and rotation) to the map coordinates, and then assembling the processed layer maps in the appropriate z-order (front to back) and with the appropriate positioning.

The following commands are considered for image map processing when provided in conjunction with `req=map` (either directly in the request, by way of catalog templates, or in `catalog::Modifier` strings):

* `align=` 
* `wid=` 
* `hei=` 
* `scl=` 
* `crop=` 
* `flip=` 
* `rotate=` 
* `scale=` 
* `layer=` 
* `size=` 
* `extend=` 
* `origin=` 
* `pos=` 
* `anchor=` 
* `src=` 
* `map=`

All other commands are effectively ignored.

The `SHAPE` and `COORDS` attributes of an `AREA` may be modified during processing of a `req=map` request, all other attributes of the `AREA` element are passed without modification. In most cases this involves changing the `SHAPE` value from `DEFAULT` to `RECT` (this would also add the `COORDS` attribute), or changing the `COORDS` values.

Any `AREA` elements which become empty during processing are removed entirely. If a map is associated with `layer=comp` it is placed behind all other maps. The data is returned in text form one as or more HTML `AREA` elements. An empty reply string indicates that no image map exists for the specified object(s).

Layer transparency is not considered for map processing. A fully transparent layer can still have an image map associated with it. The map of a partially transparent layer is not clipped to the transparent regions.

## See also {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01 Specification](https://www.w3.org/TR/html401/)
