---
description: Multi-bit rate data.
seo-description: Multi-bit rate data.
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
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
