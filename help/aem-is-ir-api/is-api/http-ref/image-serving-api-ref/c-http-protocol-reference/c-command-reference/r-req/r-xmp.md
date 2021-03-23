---
description: XMP metadata. Returns the XMP metadata associated with the image specified in the request path.
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# xmp{#xmp}

XMP metadata. Returns the XMP metadata associated with the image specified in the request path.

 `req=xmp`

Other commands are ignored. UTF-8 encoding applies. The response is formatted as XML with MIME type `text/xml`.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

## Properties {#section-0d26b6a56c844153ae5cea4880370d00}

Request attribute. Applies regardless of current layer setting.

## Default {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

If the URL does not include an image path or modifiers, then:

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Otherwise, `req=img`

## Examples {#section-34213692deab4a0f9037d5844132ee14}

Query image file properties.

` http:// *`server`*/myPath/myImage.tif?req=imageprops`

Query image catalog properties:

` http:// *`server`*/myRootId?req=catalogprops`

Access the properties of an image catalog entry from client-side JavaScript embedded in an HTML file:

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

Retrieve the mask image for a particular catalog entry, scaled to 25% of the original size:

` http:// *`server`*/myRootId/myImageId?req=mask&scale=0.25`

Request an image at one-eighth size:

` http:// *`server`*/myRootId/myImageId?scl=8`

This is the same as:

` http:// *`server`*/myRootId/myImageId?req=img&scl=8`

Request a thumbnail of an image, relying on the thumbnail attributes specified in the image catalog:

` http:// *`server`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

Send a text message to the server logs:

` http:// *`server`*/myRootId?req=message&message=This%20is%20the%20message`

## See also {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md), [Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f), [Properties](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9), [Image Maps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab) 
