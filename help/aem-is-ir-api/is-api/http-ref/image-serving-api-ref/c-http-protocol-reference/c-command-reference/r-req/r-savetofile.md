---
description: Save image to file.
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# saveToFile{#savetofile}

Save image to file.

 `req=saveToFile&name= *`file`*[&timeout= *`val`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p> </td> 
  <td class="stentry"> <p>Relative path to target image file. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Timeout interval (milliseconds). </p></td> 
 </tr> 
</table>

Saves the response image to a file on the server instead of returning it to the client.

When the save request completes successfully, the request returns several Java-formatted properties, including the following: 

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Property</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>File creation time (number of milliseconds since midnight, January 1, 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Number of pixels in saved image. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> done</span> if successful. </p> </td> 
  </tr> 
 </tbody> 
</table>

Returns HTTP response status 200 if successful and 403 if the request fails or times out. The response has MIME type `text/plain` and is not cacheable.

Important Saving to files must be enabled by specifying the path to an existing writeable folder in `attribute::SavePath`. `saveToFile=` fails if `attribute::SavePath` is empty.

*`file`* is required and must be a relative path which is combined with `attribute::SavePath`. Image Serving does not create folders. The target folder must exist on the server and have the appropriate permission settings for Image Serving to create files.

`timeout=` is optional. The default timeout is 60,000 msec, or whichever value is configured with `PS::SaveTimeout`. 
