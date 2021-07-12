---
description: Request type. Specifies the type of request.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
---
# req{#req}

Request type. Specifies the type of request.

 `req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`options`*]`

* [catalogprops](r-catalogprops.md)
* [exists](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [map](r-map-req.md)
* [mask](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [message](r-message.md)
* [props](r-props.md)
* [resolve](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [set](r-set.md)
* [targets](r-targets.md)
* [tmb](r-tmb.md)
* [userdata](r-userdata.md)
* [validate](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

Unless otherwise noted in the detailed descriptions, the server returns `text` responses with MIME type `text/plain`. Many request types let you specify a response type, such as `text`, that is typically the default, `javascript`, `xml`, or `json`. The associated response MIME types are `text/plain`, `text/javascript`, `text/xml`, and `text/javascript`, respectively.

Unless otherwise noted, responses format the response as a set of `name=value` pairs.

See [Properties](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
