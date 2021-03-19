---
description: Error message detail. Specifies the level of detail for error messages returned via HTTP as the error.message value.
seo-description: Error message detail. Specifies the level of detail for error messages returned via HTTP as the error.message value.
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
uuid: aab11640-95d7-427d-b79f-c477b2c9047e
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# ErrorDetail{#errordetail}

Error message detail. Specifies the level of detail for error messages returned via HTTP as the error.message value.

## Title {#section-c10d75d72ee24d16a67cc8d927f1deba}

The following values are permitted:

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Title only. Returns a short general description of the error. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Brief message. Reserved for future use. Currently returns the same info as 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Detailed message. Provides user-level details about the error. May include sensitive information, such as file paths. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Full debug info. Adds Java stack traces when applicable. Error images never include stack traces and instead return level 2 information in <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* Level 0 is recommended for live servers that can be accessed publicly. 
* Level 2 is recommended for staging, quality assurance, and application development servers. 
* Level 3 information may be useful when reporting problems to Dynamic Media technical support.

## Properties {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

Enumerated value, must be 0, 1, 2, or 3.

## Default {#section-5e78d550050840cc9a1de811c581b94f}

Inherited from `default::ErrorDetail` if not specified or if empty.

## See also {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0) 
