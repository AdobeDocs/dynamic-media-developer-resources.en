---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
TQID: 'https://experienceleague.adobe.com/ZQj4mwz-MZWHf8MeY-hrrESZLucBeqXpGQV6tnD-U9w'
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
# SpinView.autospin{#spinview-autospin}

 ` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`duration`*][, *`direction`*][, *`spin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Enables or disables the automatic spin animation. To achieve the best auto spin experience, it is recommended that you preload all frames by setting <span class="codeph"> maxloadradius</span> to <span class="codeph"> -1</span>. Note, however, that this setting results in increased load time and higher bandwidth usage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> The number of seconds per one full spin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> direction</span></span> </p> </td> 
   <td colname="col2"> <p> The spin direction which is <span class="codeph"> 0</span> for spinning east and <span class="codeph"> 1</span> for spinning west. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> The number of full rotations done before autospin stops. The number is a floating point number. Set to <span class="codeph"> -1</span> for an infinite auto spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Default {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Example {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
