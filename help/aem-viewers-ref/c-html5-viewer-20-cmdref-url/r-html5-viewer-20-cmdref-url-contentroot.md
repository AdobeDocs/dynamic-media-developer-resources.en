---
title: contentUrl
description: Parameter common to all viewers.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
TQID: 'https://experienceleague.adobe.com/D95dvILCIpQtQ6D1TcPwj-xfgjXb6AvyMmm5vDlemWw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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

<!--

```
contentUrl=https://demos-pub.assetsadobe.com/
```

-->
