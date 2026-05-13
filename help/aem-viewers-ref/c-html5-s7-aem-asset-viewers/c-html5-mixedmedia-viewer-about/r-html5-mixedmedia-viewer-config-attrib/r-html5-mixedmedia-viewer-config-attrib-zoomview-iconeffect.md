---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 40b7887d-d525-4816-8c72-9ef8f5948de3
TQID: 'https://experienceleague.adobe.com/I0LPloUkd-2zlFBUDNzulvo6G3zR1TL16GvJkAh1JFE'
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
# ZoomView.iconeffect{#zoomview-iconeffect}

 ` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Enables the <span class="codeph"> iconeffect</span> to display on the top of the image when the image is in a reset state and it is suggestive of an available action to interact with the image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the maximum number of times the <span class="codeph"> iconeffect</span> appears and reappears. A value of <span class="codeph"> -1</span> indicates that the icon always reappears indefinitely. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p>Specifies the duration of the show or hide animation, in seconds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Sets the number of seconds that the <span class="codeph"> iconeffect</span> stays fully visible before it auto-hides. That is, the time after the fade-in animation is completed but before the fade-out animation starts. A setting of <span class="codeph"> 0</span> disables the auto-hide behavior. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
