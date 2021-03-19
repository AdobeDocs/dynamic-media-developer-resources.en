---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
uuid: 16a0ca99-1ed5-4f1d-b068-55adc46fde0b
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

 ` [FlyoutZoomView.|<containerId>_flyout.]tip= *`duration`*[, *`count`*][, *`fade`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the number of seconds the tip text is displayed before it hides. When set to <span class="codeph"> -1</span>, the message is always displayed, even if the user activates the flyout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the number of times the text is displayed when viewing new images in the set. A value of <span class="codeph"> -1</span> means that the text is always displayed when viewing any image in the set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> Specifies the duration of a fade animation that occurs when the text appears or disappears. A value of <span class="codeph"> 0</span> indicates no fade transition. </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0` 
