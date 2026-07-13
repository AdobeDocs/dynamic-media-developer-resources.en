---
description: Image location coordinates returned by the getPhotoshopPath operation.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
TQID: 'https://experienceleague.adobe.com/jJYhv5-HhU2t1CyVeRVzmIsprZ3xM4ZQtcMDS-Zgt6I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# [!DNL PerspectiveQuad]{#perspectivequad}

Image location coordinates returned by the getPhotoshopPath operation.

 Syntax 

## Parameters {#section-59792c446366456d90de7f5875bad1b0}

|  Name  | Type  | Description  |
|---|---|---|
|  x0  | `xsd:double`  | Upper left x-axis coordinate.  |
|  y0  | `xsd:double`  | Upper left y-axis coordinate.  |
|  x1  | `xsd:double`  | Upper right x-axis coordinate.  |
|  y1  | `xsd:double`  | Upper right y-axis coordinate.  |
|  x2  | `xsd:double`  | Lower right x-axis coordinate.  |
|  y2  | `xsd:double`  | Lower right y-axis coordinate.  |
|  x3  | `xsd:double`  | Lower left x-axis cooridnate.  |
|  y3  | `xsd:double`  | Lower left y-axis coordinate.  |

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

>[!MORELIKETHIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)

