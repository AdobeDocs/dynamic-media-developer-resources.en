---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 300bbee8-29f1-444d-bf98-42aeb9c5017b
---
# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Specifies internal alignment (anchoring) of the swatches container within the component area. In Swatches, the internal thumbnail container is sized so that only a whole number of swatches is shown. As a result, there is some padding between the internal container and the external component bounds. This command specifies how the internal swatches container is positioned inside the component.

<table id="table_33CC037517964DA89EE0C005BB6B32BB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> left|center|right</span> </p> </td> 
   <td colname="col2"> <p> Sets horizontal swatches alignment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
   <td colname="col2"> <p> Sets vertical swatches alignment. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

`center,center`

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`align=left,top`
