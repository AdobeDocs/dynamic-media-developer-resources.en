---
description: Property data is returned in response to the following req= types  imageprops and props.
solution: Experience Manager
title: Properties
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
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
