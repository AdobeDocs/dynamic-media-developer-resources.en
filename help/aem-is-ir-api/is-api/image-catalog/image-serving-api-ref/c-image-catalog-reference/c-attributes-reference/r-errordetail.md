---
description: Error message detail. Specifies the level of detail for error messages returned via HTTP as the error.message value.
seo-description: Error message detail. Specifies the level of detail for error messages returned via HTTP as the error.message value.
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Scene7 Image Serving - Image Rendering API
uuid: 46ebb8c7-930e-4844-8664-ec6a63691523
index: y
internal: n
snippet: y
---

# ErrorDetail{#errordetail}

Error message detail. Specifies the level of detail for error messages returned via HTTP as the error.message value.

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
  <td class="stentry"> <p>Full debug info. Adds Java stack traces when applicable. Error images never include stack traces and instead return level 2 information in <span class="codeph"> $error.message</span>. This information can be useful when reporting problems to Scene7 Tech Support. </p></td> 
 </tr> 
</table>

## Properties {#section-e167895723ca4ad4ba283d3d7b4324de}

Enumerated value, must be 0, 1, 2, or 3.

## Default {#section-8f27098e509945a18676aca0675c8f41}

Inherited from `default::ErrorDetail` if not specified or if empty.

## See also {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) 
