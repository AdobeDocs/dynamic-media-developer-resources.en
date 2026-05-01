---
description: JavaScript API reference for eCatalog Viewer.
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f1491091-f109-4836-b7f1-ad0619b72dce
TQID: https://experienceleague.adobe.com/FylFWGJa3AICyLRD1vjLPhLkwnr-6hbMMlsy-y6a4aI
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# setContainerId{#setcontainerid}

JavaScript API reference for eCatalog Viewer.

 [!DNL ` setContainerId( *`containerId`*)`]

Sets the ID of the `DOM` container (normally a `DIV`) into which the viewer is inserted. It is not necessary to have the container element created by the time this method is called. However, the container must exist when `init()` is run. It must be called before `init()`.

This method is optional if the viewer configuration information is passed with `config` JSON object to the constructor.

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
