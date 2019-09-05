---
description: Property data is returned in response to the following req= types  imageprops and props.
seo-description: Property data is returned in response to the following req= types  imageprops and props.
seo-title: Properties
solution: Experience Manager
title: Properties
topic: Scene7 Image Serving - Image Rendering API
uuid: 96ac5981-974d-4c1a-b508-19401aea973b
index: y
internal: n
snippet: y
---

# Properties{#properties}

Property data is returned in response to the following req= types: imageprops and props.

The reply data is formatted to be readable as Java properties. A typical text properties response has this general structure:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` can be empty. White space is optional at the beginning and end of each line and before and after the '=' separator. Single or double quotes may be used to enclose string values, but are not required.

String values may contain JAVA-style escape characters, such as \n, \t, \:. or \\.

**See also**

[req=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb) 
