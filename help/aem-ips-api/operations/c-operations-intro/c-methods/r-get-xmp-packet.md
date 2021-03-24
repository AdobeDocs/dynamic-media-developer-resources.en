---
description: Retrieves an XMP Metadata packet for the specified asset.
solution: Experience Manager
title: getXMPPacket
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# getXMPPacket{#getxmppacket}

Retrieves an XMP Metadata packet for the specified asset.

 Syntax 

## Authorized User Types {#section-7cb9c26045214f01b1d6b6948b6c6a18}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-b4075df0e4414b00b961d978d5471db9}

**Input (getXMPPacketParam** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  |The company handle with the packet you want to return (e.g., `c|656`).  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | The asset for which the XMP packet should be retrieved.  |

**Output (getXMPPacketReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`compressedPacket`*`  | `xsd:Base 64 binary`  | Yes  | [!DNL zlib-compressed] XMP packet.  |

## Examples {#section-d681af49122e4ca9bcd04110a2e98e6f}

**Request** 

```java
<ns:getXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
</ns:getXMPPacketParam>
```

**Response** 

```java
<getXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg+
      955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/Lr/AQ5Kc/AxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzA/QZkunymD8
      cvs5lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC4
      1IjNF1YlksGV2v26mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFgllKO+bn/ZpqrFv+xsS519WKO1mX9y/yoHppveRXrgWTlxX9qJk0ojHG9eaBP3
      PtKnNaNRNJ kq6lNC8bO5/sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh
      /3LPyoIWfgNKX1Vz4i8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7t+8xdjuhqNPERMBaoBAAA=
   </compressedPacket>
</getXMPPacketReturn>
```

