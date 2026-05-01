---
description: Multi-bit rate data.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
TQID: https://experienceleague.adobe.com/AkZw3S6R4uagF0TydQlTDTHZm9B3PYppv0g-pDFKhlQ
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# mbrSet{#mbrset}

Multi-bit rate data.

 `req=mbrSet[,text|xml[, *`encoding`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

Returns a text or xml response which contains a list of URLs (and corresponding bit rates) which correspond to valid video entries in video set associated with net path id.

The previous requirement that a valid video entry contain a value for `catalog::VideoBitRate` has now been relaxed. The entry can containing a value for `catalog::VideoBitRate`*or* `catalog::AudioBitRate`*or* `catalog::TotalStreamBitRate`. Only one of these needs to be defined for the video entry to be valid. Note that the requirements for `catalog::Path` and a valid video file extension have not changed.

Responses are intended for consumption by Apple and Flash Streaming Servers and thus structurally conform to those specifications. URLs are generated using prefixes `attribute::HttpAppleStreamingContext` and `attribute::HttpFlashStreamingContext`.

m3u8 responses only contain mp4 files if any are present in the video set. If no mp4 files are present, then these responses only contain f4v files. If no mp4 files nor f4v files are present, then the response is empty.

f4m responses only contain f4v files if any are present in the video set. If no f4v files are present, then these responses only contain mp4 files. If no f4v files nor mp4 files are present, then the response is empty.

Bit rates that appear in f4m/m3u8 responses correspond to the values in `catalog::TotalStreamBitRate` (converted to appropriate units). If `catalog::TotalStreamBitRate` is not defined, the summation of `catalog::VideoBitRate` and `catalog::AudioBitRate` is used.

The HTTP response is cacheable with the TTL based on `catalog::NonImgExpiration`.
