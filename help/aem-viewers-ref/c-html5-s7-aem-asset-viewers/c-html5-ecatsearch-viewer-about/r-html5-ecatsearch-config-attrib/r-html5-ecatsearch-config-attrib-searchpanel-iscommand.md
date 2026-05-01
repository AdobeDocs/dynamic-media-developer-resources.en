---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4e843866-75a5-4543-a275-e134b3aee75a
TQID: https://experienceleague.adobe.com/94EAfe7F-wmYpR36TFvhiEYE9GNoJlTWOs5tkca1kFk
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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
