---
description: Source image properties. Returns selected properties of the image file or catalog entry specified in the URL path.
seo-description: Source image properties. Returns selected properties of the image file or catalog entry specified in the URL path.
seo-title: imageprops
solution: Experience Manager
title: imageprops
uuid: e9bf2780-a520-4fb1-ab4c-40bb799e36a4
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# imageprops{#imageprops}

Source image properties. Returns selected properties of the image file or catalog entry specified in the URL path.

 `req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Unique request identifier. </p></td> 
 </tr> 
</table>

The HTTP response is cacheable with the TTL based on `attribute::NonImgExpiration`.

Other commands in the request string are ignored.

Requests that support JSONP response format lets you specify the name of the JS callback handler using the extended syntax of `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is the name of the JS handler that is present in the JSONP response. Only a-z, A-Z, and 0-9 characters are allowed. Optional. Default is `s7jsonResponse`.

The following properties are returned: 

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> Property</b> </td> 
   <td> <b> Type</b> </td> 
   <td> <b> Description</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> or the default anchor point </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> or the default time to live </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>Full resolution image height in pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Name/description of the profile associated with this image </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image. embeddedIccProfile</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 if the associated profile is embedded in the image </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 if the image includes Photoshop path data </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image. embeddedXmpData</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 if the image includes XMP data </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 for no mask, 1 for premultiplied alpha, 2 for non-premultiplied alpha, and 3 for a separate mask image </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> or empty if not a catalog entry </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image. photoshopPathNames</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Comma-separated list of the names of all Photoshop paths associated with this image </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Image type, may be 'CMYK', 'RGB' or 'BW' (for gray-scale images) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> attribute::PostModifier</span> or empty if not a catalog entry </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> default print resolution in pixels/inch </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> or the default object resolution </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p>Modification date/time (from <span class="codeph"> catalog::TimeStamp</span> or the image file) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> catalog::ThumbRes</span> or the default thumbnail resolution </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catalog::ThumbType</span> or the default thumbnail type </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Full resolution image width in pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Catalog ID to which the <span class="varname"> object</span> specified in the path is resolved (see <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Object Id Translation</a>). </p> </td> 
  </tr> 
 </tbody> 
</table>

