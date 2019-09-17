---
description: Options for automatically cropping images based on color.
seo-description: Options for automatically cropping images based on color.
seo-title: AutoColorCropOptions
solution: Experience Manager
title: AutoColorCropOptions
topic: Scene7 Image Production System API
uuid: 632ae721-7b39-4cd1-a1c6-1a3554167a4e
---

# AutoColorCropOptions{#autocolorcropoptions}

Options for automatically cropping images based on color.

 Syntax 

## Parameters {#section-0302e9238dbc4704914e938f42c881e6}

<table id="table_F6A0DBA37F704C2097C617A0A6767566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> corner</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Choice of AutoCrop Corner. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolerance</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Color match specification. Uses: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 to match colors exactly. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 to enable the most color differences. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

