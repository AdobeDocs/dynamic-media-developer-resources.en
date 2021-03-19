---
description: The Image Serving command string that is applied to all thumbnails.
seo-description: The Image Serving command string that is applied to all thumbnails.
seo-title: FavoritesView.iscommand
solution: Experience Manager
title: FavoritesView.iscommand
uuid: be3d49d1-d5d2-4ecd-bc8f-fe5f80204c76
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
---

# FavoritesView.iscommand{#favoritesview-iscommand}

The Image Serving command string that is applied to all thumbnails.

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> If specified in the URL, all occurrences of <span class="codeph"> &amp;</span> and <span class="codeph"> =</span> must be HTTP-encoded as <span class="codeph"> %26</span> and <span class="codeph"> %3D</span>, respectively. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

None.

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

When specified in the viewer URL.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

When specified in the config data.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`] 
