---
title: Selection commands
description: These commands are used to select vignette groups, objects, sub-areas of groups or objects.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43f6ec6e-e4eb-468d-9c66-841af5e0a8a5
TQID: 'https://experienceleague.adobe.com/kPVDPxUrgIeRABa46wNXBJDEo2Gh6KeM-vGCIFbuEEU'
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
# Selection commands{#selection-commands}

These commands are used to select vignette groups, objects, sub-areas of groups or objects.

 The command, or the material, or both, are specified after this selection command and before the next selection command (or the end of the request) is applied to the selected item. Selection commands delimit material specification segments (MSS).

<table id="simpletable_028957E516644FE8A7B1BC056A32FCD1"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a" type="reference" format="dita" scope="local"> obj</a> </span> </p></td> 
  <td class="stentry"> <p>Select a vignette group or object by name. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b" type="reference" format="dita" scope="local"> sel</a></span> </p></td> 
  <td class="stentry"> <p>Select a vignette group or object by pixel location. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-decal.md#reference-3a5f1adc7fe24c91aa5655d64038e857" type="reference" format="dita" scope="local"> decal</a></span> </p></td> 
  <td class="stentry"> <p>Select the decal area of the selected object. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sub.md#reference-3cedba817f3c401495ba32bd1bf9b383" type="reference" format="dita" scope="local"> sub</a></span> </p></td> 
  <td class="stentry"> <p>Select a sub-area of the selected group or object. </p></td> 
 </tr> 
</table>

