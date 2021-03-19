---
description: Parameter common to all viewers.
seo-description: Parameter common to all viewers.
seo-title: serverUrl
solution: Experience Manager
title: serverUrl
uuid: a079a223-7478-4b6a-bc99-284e3366fb30
feature: "Dynamic Media Classic,Viewers,SDK/API"
role: "Developer,Business Practitioner"
---

# serverUrl{#serverurl}

Parameter common to all viewers.

 ` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Relative or absolute Image Serving root path. </p> <p> Specifies a relative or absolute path to Image Serving, from where the viewer retrieves images. If the path does not have a leading <span class="filepath"> /</span>, it is relative to the location of the viewer HTML page. If the path has a leading <span class="filepath"> /</span>, it specifies an absolute path on the same server. </p> <p> Use only an absolute path in case the Email share module is enabled in the viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-10ee45d637134e0fbcd943c62578cb78}

Optional. Not needed for standard SaaS (software as a service) usage.

## Default {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## Examples {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

