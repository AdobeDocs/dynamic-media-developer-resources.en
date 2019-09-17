---
description: Sets or updates an XMP metadata packet for an asset.
seo-description: Sets or updates an XMP metadata packet for an asset.
seo-title: updateXMPPacket
solution: Experience Manager
title: updateXMPPacket
topic: Scene7 Image Production System API
uuid: 97a40261-8f85-4e8c-8aa5-ed4fec297f33
---

# updateXMPPacket{#updatexmppacket}

Sets or updates an XMP metadata packet for an asset.

 Syntax 

## Authorized User Types {#section-ee88a759f4774482a4734201a971f610}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalcontribUser`

## Parameters {#section-7a89621d441840faba639746b410a489}

**Input (updateXMPPacketParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | Company handle.  |
|  ` *`assetHandle`*`  | `xsd:string`  | Yes  | Asset handle.  |
|  ` *`compressedPacket`*`  | `xsd:Base 64 binary`  | Yes  | [!DNL zlib-compressed] XMP packet you want to set or update.  |

**Output (updateXMPPacketReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`success`*`  | `xsd:boolean`  | Yes  |Returns `true` if the packet was updated.  |

## Examples {#section-38b556b94e5044bf97a954519ff6c212}

**Request** 

```java
<ns:updateXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
   <ns:compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg
+955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/LrQ5KcAxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzAQZkunymD8cvs5
lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC41IjNF1YlksGV2v2
6mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFglldKO+bn/ZpqrFv+xsS519WKO1mX9yyoHppveRXrgWTlxX9qJk0ojHG9eaBP3PtKnNaNRNJkq6lN
C8bO5sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh3LPyoIWfgNKX1Vz4i
8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7tx+8xdjuhqNPERMBaoBAAA=</ns:compressedPacket>
</ns:updateXMPPacketParam>
```

**Response** 

```java
<updateXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <success>true</success>
</updateXMPPacketReturn>
```

