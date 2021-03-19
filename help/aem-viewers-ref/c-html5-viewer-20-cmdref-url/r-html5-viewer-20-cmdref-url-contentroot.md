---
description: Parameter common to all viewers.
seo-description: Parameter common to all viewers.
seo-title: contentUrl
solution: Experience Manager
title: contentUrl
uuid: 85b00c4e-b382-4970-b780-e4ef59108cb7
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
---

# contentUrl{#contenturl}

Parameter common to all viewers.

 ` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifies the base path to custom CSS files, any closed captioning content, or navigation content. </p> <p>If the path does not have a leading <span class="filepath"> /</span>, it is relative to the location of the viewer HTML page. If the path has a leading <span class="filepath"> /</span>, it specifies an absolute path on the same server. </p> <p> Does not affect the loading of the default CSS file when you do not specify a style command. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Default {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Examples {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```

