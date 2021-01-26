---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
topic: Dynamic Media
uuid: 6c853c6a-a57d-4cab-ad71-74baf9e870d1
---

# PageView.iscommand{#pageview-iscommand}

 ` [PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> The Image Serving command string that is applied to page image. If specified in the URL all occurrences of <span class="codeph"> &amp;</span> and <span class="codeph"> =</span> must be HTTP-encoded as <span class="codeph"> %26</span> and <span class="codeph"> %3D</span>, respectively. </p> <p> <p>Note:  Image sizing manipulation commands are not supported. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-df5a0604766b4ac2b9a6742b377e427c}

Optional.

## Default {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

None.

## Example {#section-813de2905d6c44c0991cfe0931581462}

When specified in the viewer URL.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

When specified in the config data.

`iscommand=op_sharpen=1&op_colorize=0xff0000` 
