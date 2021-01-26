---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic Media
---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

 [!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Info server URL template is used to fetch key/value pairs for the variable substitution in the info panel content template. The specified template typically contains macro place holders that are replaced with the actual data before the request is sent to the server. </p> <p><span class="codeph"> $1$</span> is replaced with the rollover value that triggered the <span class="codeph"> InfoPanelPopup</span> activation. </p> <p><span class="codeph"> $2$</span> is replaced with the sequence number of the current frame in the image set. </p> <p><span class="codeph"> $3$</span> is replaced with the first path element specified in the name of the parent set of the current item. It typically corresponds to the catalog id. </p> <p><span class="codeph"> $4$</span> is replaced with the following element in the path and corresponds to the asset id. The actual info server request syntax is info server dependent and it differs from server to server. For example, the following is a typical Dynamic Media info server request template: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Be aware that when you configure Info Panel Popup, the HTML code and JavaScript code passed to the Info Panel runs on the client's computer. Therefore, make sure that such HTML code and JavaScript code are secure.

## Properties {#section-71356e3c13244e62b0582980d9d05328}

Optional.

## Default {#section-22e9af803f724434807d34e200eb7518}

None.

## Example {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`] 
