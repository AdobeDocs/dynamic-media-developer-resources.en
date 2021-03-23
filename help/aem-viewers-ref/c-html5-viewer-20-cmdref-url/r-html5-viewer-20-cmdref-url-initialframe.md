---
description: Parameter common to all viewers.


solution: Experience Manager
title: initialFrame

feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
---

# initialFrame{#initialframe}

Parameter common to all viewers.

>[!NOTE]
>
>This command does not apply to Video Image Viewer.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies a zero-based frame index that the viewer displays on load. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>A zero-based index of the page within the spread when the device is in portrait orientation. In a "left-to-right" environment <span class="codeph"> 0</span> means "left page" and <span class="codeph"> 1</span> means "right page". In "right-to-left" it is opposite: <span class="codeph"> 0</span> means "right page" and <span class="codeph"> 1</span> means "left page". </p> <p>If not specified, <span class="codeph"> 0</span> is assumed by default. Ignored when device is in landscape orientation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Default {#section-d411e450028c460392cb8508f8ccc5d9}

No default.

## Example {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```

