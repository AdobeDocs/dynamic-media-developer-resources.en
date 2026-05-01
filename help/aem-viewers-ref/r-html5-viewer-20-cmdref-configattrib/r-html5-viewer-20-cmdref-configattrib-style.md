---
title: style
description: style
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
TQID: https://experienceleague.adobe.com/cpA2SrNY0hYncmJezg5bE-h9AtJ9Ohz7LN6ruzdKABA
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# style{#style}

You can apply the following command both from the URL query string and config. The command applied in the URL query string always takes precedence over the same command present in config.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Relative or absolute CSS location. </p> <p>Specifies the location of the custom CSS file. If the <span class="codeph"><span class="varname"> cssPath</span></span> is relative, it is resolved against the viewer HTML page location and the value of <span class="codeph"> contentUrl=</span> parameter. </p> </td> 
  </tr> 
 </tbody> 
</table>

All asset references within the CSS file are resolved against the CSS file location, not the location of the calling HTML page.

## Properties {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Optional.

## Default {#section-79a827f7a3bb4f36b3d72c309155059e}

None.

## Examples {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
