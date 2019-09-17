---
description: Image map data. None or more complete HTML <AREA> elements, sorted front-to-back.
seo-description: Image map data. None or more complete HTML <AREA> elements, sorted front-to-back.
seo-title: Map
solution: Experience Manager
title: Map
topic: Scene7 Image Serving - Image Rendering API
uuid: 674a7a74-91bf-41c4-ab74-a5cb4f8abe1d
---

# Map{#map}

Image map data. None or more complete HTML <AREA> elements, sorted front-to-back.

The server will interpret and may change the SHAPE and COORDS attributes. (SHAPE=CIRCLE is not supported in this release.) All other attributes of `<AREA>` are passed through without modification. Coordinate values specified with the COORDS attribute must be pixel offsets from the top-left corner of the unmodified source image. (% coordinates are not supported in this release and may not be processed correctly.)

## Properties {#section-f52d89fd399b4356ac05277e6c12f956}

Text string value. If specified, it must be one or more complete HTML `<AREA>` elements.

This field participates in text string localization. Refer to [Text String Localization](r_text_string_localization.md#reference_CAE5F6CEA4764762852ACAAB3B7B3527) in the *HTTP Protocol Reference* for details.

## Default {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

None.

## See also {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](r_map.md#reference_8F96545F196B4B7CAA616E15C2363F06) , [req=map](r_req.md#reference_907CDB4A97034DB7AD94695F25552E76), [Text String Localization](r_text_string_localization.md#reference_CAE5F6CEA4764762852ACAAB3B7B3527) 
