---
description: Property data is returned in response to the following req= types  imageprops and props.
seo-description: Property data is returned in response to the following req= types  imageprops and props.
seo-title: Properties
solution: Experience Manager
title: Properties
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Properties{#properties}

Property data is returned in response to the following req= types: imageprops and props.

The reply data is formatted to be readable as Java properties. A typical text properties response has this general structure:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` can be empty. White space is optional at the beginning and end of each line and before and after the '=' separator. Single or double quotes may be used to enclose string values, but are not required.

String values may contain JAVA-style escape characters, such as `\n`, `\t`, `\:`. or `\\`.

**See also**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb) 
