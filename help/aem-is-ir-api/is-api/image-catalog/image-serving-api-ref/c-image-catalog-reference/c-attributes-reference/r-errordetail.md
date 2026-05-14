---
description: Error message detail. Specifies the level of detail for error messages returned by way of HTTP as the error.message value.
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
TQID: 'https://experienceleague.adobe.com/CZ2k-H1kZI3t3ZAtgm7qj8eo97u4NPmumdErNU--uvU'
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
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
---
# ErrorDetail{#errordetail}

Error message detail. Specifies the level of detail for error messages returned by way of HTTP as the error.message value.

 The following values are permitted:

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Title only. Returns a short general description of the error. Recommended for live servers that can be accessed publicly. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Brief message. Reserved for future use. Currently returns the same info as 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Detailed message. Provides user-level details about the error. May include sensitive information, such as file paths. Recommended for staging, quality assurance, and application development servers. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Full debug info. Adds Java stack traces when applicable. Error images never include stack traces and instead return level 2 information in <span class="codeph"> $error.message</span>. This information can be useful when reporting problems to Dynamic Media technical support. </p></td> 
 </tr> 
</table>

## Properties {#section-e167895723ca4ad4ba283d3d7b4324de}

Enumerated value, must be 0, 1, 2, or 3.

## Default {#section-8f27098e509945a18676aca0675c8f41}

Inherited from `default::ErrorDetail` if not specified or if empty.

## See also {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
