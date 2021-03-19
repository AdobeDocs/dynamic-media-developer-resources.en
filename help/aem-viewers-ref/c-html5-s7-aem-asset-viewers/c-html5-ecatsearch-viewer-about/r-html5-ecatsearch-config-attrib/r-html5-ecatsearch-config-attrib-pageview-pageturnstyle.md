---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
uuid: 748adb73-bfb6-4fce-aa6a-4216184edabb
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
---

# PageView.pageturnstyle{#pageview-pageturnstyle}

 [!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *`dividerWidth`*, *`dividerColor`*, *`dividerOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`]

Controls the component appearance when a [!DNL `PageView.frametransition`] is set to [!DNL `turn`] or to [!DNL `auto`] on desktop systems.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> The width in pixels of the page divider shadow that separates the left and right pages in the spread. It also controls the width of the running shadow displayed next to the turning page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> The shadow color in RRGGBB format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>The shadow opacity in the range of <span class="codeph"> 0</span> to <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> The flag (either <span class="codeph"> 0</span> or <span class="codeph"> 1</span>) which turns the border around the turning page on and off. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> The border color in RRGGBB format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> The color of the solid fill of the component area used during page turn animation, in RRGGBB format. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-54c634116cfe4f17813318e07539264c}

Optional.

## Default {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## Examples {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`] 
