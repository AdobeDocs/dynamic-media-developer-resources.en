---
description: null
seo-description: null
seo-title: direction
solution: Experience Manager
title: direction
topic: Dynamic media
uuid: 0a30f3b0-64c8-4799-b4f5-fc8996a8b5a4
index: y
internal: n
snippet: y
---

# direction{#direction}

 `direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Specifies the way pages are displayed in the main view and thumbnails. It also specifies the way the user interacts with the viewer user interface to change between catalog frames. </p> <p>When <span class="codeph"> left </span> is used it sets a right alignment for the initial page, and left alignment for the last page. It stitches individual page sub-images for left-to-right rendering order. It also sets the main view to use right-to-left slide animation to advance the catalog (in case <span class="codeph"> PageView.frametransition </span> is set to slide). Finally, thumbnails are set for a left-to-right fill order. </p> <p>Similarly, when <span class="codeph"> right </span> is used it sets a left alignment for the initial page, and right alignment for the last page. It stitches individual page sub-images for right-to-left rendering order. It also sets the main view to use left-to-right slide animation to advance the catalog (in case <span class="codeph"> PageView.frametransition </span> is set to slide). Finally, it reverses the thumbnails order so that the thumbnails view is filled in right-to-left, top-to-bottom direction. </p> <p>When <span class="codeph"> auto </span> is set, the viewer applies <span class="codeph"> right </span> mode when locale is set to <span class="codeph"> ja; </span>otherwise, it uses <span class="codeph"> left </span> mode. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-a66ce10d6c0b449883f654e7e0657e2c}

Optional.

## Default {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Example {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right` 
