---
title: Session catalog
description: The session catalog is the material catalog which provides session attributes for the request, and a default catId value for all src=, vignette=, and icc= commands.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
TQID: 'https://experienceleague.adobe.com/--3F69i8XdliFxf5IhMPbUThRzMNyIDjtW4-Y-SBCFE'
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
# Session catalog{#session-catalog}

The session catalog is the material catalog which provides session attributes for the request, and a default catId value for all `src=`, `vignette=`, and `icc=` commands.

The session catalog is specified as the first path element of the HTTP request path (immediately following the server name). If the first path element does not match attribute::RootId of any catalog, the default catalog is used as a session catalog.

The session catalog provides the following session default values:

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attribute </p> </th> 
   <th class="entry"> <p>Notes </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> Root path for material data files </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::VignettePath</span> </p> </td> 
   <td> <p> Root path for vignette files </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::IccProfileRgb</span> </p> </td> 
   <td> <p> Default working color space if a vignette does not embed an ICC profile </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> Root URL for relative HTTP file paths in <span class="codeph"> src=</span> commands </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Initial show/hide state for overlap objects </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> Time-to-live value of the reply image for proxy server and browser caches </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
   <td> <p> The maximum allowed reply image width and height </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> Default values for <span class="codeph"> wid=</span> and <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Format</span> </p> </td> 
   <td> <p> Default value for <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::JpegQuality</span> </p> </td> 
   <td> <p> Default value for <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::TiffEncoding</span> </p> </td> 
   <td> <p> Compression type for TIFF image output </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Sharpen</span> </p> </td> 
   <td> <p> Default value for <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailSel</span> </p> </td> 
   <td> <p> Specifies behavior when a <span class="codeph"> sel=</span> command fails </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> Specifies behavior when an <span class="codeph"> obj=</span> command fails </p> </td> 
  </tr> 
 </tbody> 
</table>
