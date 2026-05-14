---
title: setContainerId
description: JavaScript API reference for Panoramic Viewer.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: b0145fb0-2b0d-40ce-ac18-029f54bc4050
autotag-review: '2026-05-13T22:10:33.187Z'
TQID: 'https://experienceleague.adobe.com/4Ndg-s-4Re6hMADDbkBDvKWdGFH8bzHGGooU-rNCraU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
---
# setContainerId{#setcontainerid}

JavaScript API reference for Panoramic Viewer.

 ` setContainerId( *`containerId`*)`

Sets the ID of the DOM container (normally a DIV) into which the viewer is inserted. It is not necessary to have the container element created by the time this method is called. However, the container must exist when `init()` is run. It must be called before `init()`.

This method is optional if the viewer configuration information is passed with the `config` JSON object to the constructor.

## Parameter {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID of container. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
