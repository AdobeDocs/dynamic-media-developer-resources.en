---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand

feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4e843866-75a5-4543-a275-e134b3aee75a
---
# SearchPanel.iscommand{#searchpanel-iscommand}

 [!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> The Image Serving command string that is applied to all thumbnails. If specified in the URL all occurrences of <span class="codeph"> &amp;</span> and <span class="codeph"> =</span> must be HTTP-encoded as <span class="codeph"> %26</span> and <span class="codeph"> %3D</span>, respectively. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-df5a0604766b4ac2b9a6742b377e427c}

Optional.

## Default {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

None.

## Example {#section-813de2905d6c44c0991cfe0931581462}

When specified in the viewer URL.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

When specified in the config data.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
