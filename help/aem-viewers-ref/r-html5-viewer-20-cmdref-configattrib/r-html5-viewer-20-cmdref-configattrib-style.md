---
description: style
solution: Experience Manager
title: style
topic: Dynamic Media
uuid: 6320c8dd-4827-41dc-a621-6fdf22e55003
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
