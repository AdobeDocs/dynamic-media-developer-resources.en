---
description: Image Serving source data files include image and mask files, fonts, and ICC profiles.
seo-description: Image Serving source data files include image and mask files, fonts, and ICC profiles.
seo-title: Source data
solution: Experience Manager
title: Source data
topic: Scene7 Image Serving - Image Rendering API
uuid: d654eee7-ef2d-4546-93bb-72f80c38e018
---

# Source data{#source-data}

Image Serving source data files include image and mask files, fonts, and ICC profiles.

All source data files must be accessible to the Image Server. Image Serving provides a number of alternatives for specifying the location of data files:

` *`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> relative image file path and name specified in an Image Serving HTTP request</span> </p></td> 
 </tr> 
</table>

The server combines path segments right to left until an absolute file path is established.

All ` *`rootPath`*` segments can be empty, relative, or absolute path segments.

` *`catalogPath`*` is either an absolute or relative file path/name. ` *`requestPath`*` must be a relative file path/name.

`Multiple IS::RootPath` values can be defined in ImageServerRegistry.xml (or by way of the admin interface). This allows source data files to be distributed across multiple file systems. The Image Server will try alternate paths in the order specified until the data file is found.

New data files of any kind can be added anytime without stopping the server. 
