---
description: You can use Image Serving to manage non-image content in catalogs and serve it via a separate /is/content context.
seo-description: You can use Image Serving to manage non-image content in catalogs and serve it via a separate /is/content context.
seo-title: Serving static (non-image) contents
solution: Experience Manager
title: Serving static (non-image) contents
topic: Scene7 Image Serving - Image Rendering API
uuid: bdb1383a-e02d-499f-be79-4a6dc501705c
index: y
internal: n
snippet: y
---

# Serving static (non-image) contents{#serving-static-non-image-contents}

You can use Image Serving to manage non-image content in catalogs and serve it via a separate /is/content context.

This capability allows for configuring the TTL for each item separately.

Image Serving supports the following commands at [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>Content type filter. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>, and <span class="codeph"> req=exists </span> only. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cache </a> </p> </td> 
  <td class="stentry"> <p>Allows disabling client-side caching. </p> </td> 
 </tr> 
</table>

## Basic syntax {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> request </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> server </span>/is/content[/catalog/ <span class="varname"> item </span>][? <span class="varname"> modifiers </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> port </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalog </span> </span> </p> </td> 
  <td class="stentry"> <p>Catalog identifier. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item </span> </span> </p> </td> 
  <td class="stentry"> <p>Static content item ID. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modifiers </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command </span>*[&amp; <span class="varname"> command </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> value </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>One of the supported command names. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Command value. </p> </td> 
 </tr> 
</table>

## Static content catalogs {#section-91014f17f0d543d7aaf24539b2d7d4b9}

Static content catalogs are similar to image catalogs, but support fewer data fields:

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribute/Data </p> </th> 
   <th colname="col2" class="entry"> <p>Notes </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
   <td colname="col2"> <p>The catalog record identifier for this static content item. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td colname="col2"> <p>The file path for this content item. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Expiration </span> </p> </td> 
   <td colname="col2"> <p>The TTL for this content item; <span class="codeph"> attribute::Expiration </span> is used if not specified or if empty. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>File modification time stamp; required when catalog-based validation is enabled with <span class="codeph"> attribute::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td colname="col2"> <p>Optional metadata associated with this static content item; available to the client with <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>Optional data type; can be used to filter requests for static content with the <span class="codeph"> type= command </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtering static content {#section-4c41bf41ff994910840c1352683d1f37}

This mechanism can help ensure that clients receive only contents appropriate for their needs. Assuming that the static content is tagged with appropriate `catalog::UserType` values, the client can add the `type=` command to the request. Image Serving compares the value provided with the `type=` command to the value of `catalog::UserType` and, in case of a mismatch, return an error instead of potentially inappropriate contents.

## Video caption files {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

You can encapsulate video caption files (WebVTT), CSS, or any text file in JSONP format. The JSON response is described below.

* For WebVTT files, the mime type of the response is text/javascript. JSON is not returned; instead, Javascript is returned that calls a method with JSON. Both the ID and handler are optional. 
* For CSS files, the mime type of the response is text/javascript. Both the ID and handler are optional. 
* By default, UTF-8 encoding is applied to ensure that it is decoded correctly. The default size limit is 2 MB.

You can also use tracks for other kinds of timed metadata. The source data for each track element is a text file made up of a list of timed cues. Cues can include data in formats such as JSON or CSV.

See [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) for more information about the JSONP format.

See [www.json.org](http://www.json.org) for more information about the JSON format.

## See also {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Image Catalog Reference](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5) 
