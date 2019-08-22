---
description: Image location coordinates returned by the getPhotoshopPath operation.
seo-description: Image location coordinates returned by the getPhotoshopPath operation.
seo-title: PerspectiveQuad
solution: Experience Manager
title: PerspectiveQuad
topic: Scene7 Image Production System API
uuid: caff3596-ba19-4c09-8d34-27d7bf9590d7
index: y
internal: n
snippet: y
---

# PerspectiveQuad{#perspectivequad}

Image location coordinates returned by the getPhotoshopPath operation.

 Syntax 

## Parameters {#section-59792c446366456d90de7f5875bad1b0}

|  Name  | Type  | Description  |
|---|---|---|
|  ` *`x0`*`  | `xsd:double`  | Upper left x-axis coordinate.  |
|  ` *`y0`*`  | `xsd:double`  | Upper left y-axis coordinate.  |
|  ` *`x1`*`  | `xsd:double`  | Upper right x-axis coordinate.  |
|  ` *`y1`*`  | `xsd:double`  | Upper right y-axis coordinate.  |
|  ` *`x2`*`  | `xsd:double`  | Lower right x-axis coordinate.  |
|  ` *`y2`*`  | `xsd:double`  | Lower right y-axis coordinate.  |
|  ` *`x3`*`  | `xsd:double`  | Lower left x-axis cooridnate.  |
|  ` *`y3`*`  | `xsd:double`  | Lower left y-axis coordinate.  |

## Example {#section-19ed4409ff3a41c9b52a9c9424612927}

The `PerspectiveQuad` type returns data in this order: 

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORE_LIKE_THIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)
