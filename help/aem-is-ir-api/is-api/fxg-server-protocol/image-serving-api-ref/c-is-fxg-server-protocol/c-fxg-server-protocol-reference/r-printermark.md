---
description: Display printer marks. Specifies how to display the printer marks.
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
---
# printerMark{#printermark}

Display printer marks. Specifies how to display the printer marks.

 ` printerMark= *`trim marks`*, *`bleed marks`*, *`registration marks`*, *`color bars`*, *`page information`*, *`style`*, *`line weight`*, *`layer embed`*`

The different marks can be turned off or on. The style of the printer marks can also be controlled.

The following are the valid values:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>trim marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Default is 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>bleed marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Default is 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>registration marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Default is 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>color bars= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Default is 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page information= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Default is 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Default </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>Default is Default </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>line weight= </p></td> 
  <td class="stentry"> <p>Any value in the range 0.125 - 2.0, both values inclusive. </p></td> 
  <td class="stentry"> <p>Default is 0.25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Default is 1. </p></td> 
 </tr> 
</table>

## Example {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
