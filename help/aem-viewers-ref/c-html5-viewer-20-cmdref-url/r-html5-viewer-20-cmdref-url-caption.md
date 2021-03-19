---
description: Parameter common to all viewers.
seo-description: Parameter common to all viewers.
seo-title: caption
solution: Experience Manager
title: caption
uuid: e5a715c4-9b5b-48fc-8228-5e7416e2b71a
feature: "Dynamic Media Classic,Viewers,SDK/API"
role: "Developer,Business Practitioner"
---

# caption{#caption}

Parameter common to all viewers.

>[!NOTE]
>
>This command does not apply to Video Image Viewer.

` caption= *`file`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies a URL or path to the WebVTT caption content. Image Serving serves up the WebVTT file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Specifies the default caption state. Enabled is <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

This viewer supports closed captioning by way of hosted WebVTT files. Captions specified with this parameter apply to the video that comes first in media sets; subsequent videos play without captions. Overlapping cues and regions are not supported. Supported cue positioning operators:

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Key </p> </th> 
   <th colname="col2" class="entry"> <p>Name </p> </th> 
   <th colname="col3" class="entry"> <p>Values </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>test align </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end </span> </p> </td> 
   <td colname="col4"> <p> Controls the alignment of text. </p> <p>Default is <span class="codeph"> middle </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>text position </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentage of inset into the VideoPlayer component for the beginning of the caption text. </p> <p>Default is <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>line size </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentage of video width used for captions. </p> <p>Default is <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>line position </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> Determines the line position on the page. </p> <p>If it is expressed as an integer with no percent sign, then it is the number of lines from the top where the text is displayed. </p> <p>If it is expressed as a percentage-the percent sign is the last character- then the caption text is displayed that percent down the display area. </p> <p>Default is <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Be aware that if there are any other WebVTT features present within the WebVTT file, they are not supported; however, they will not disrupt captioning.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies an URL or path to WebVTT caption content. The WebVTT file is served by Image Serving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Specifies the default caption state. </p> <p>Enabled is <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Default {#section-d411e450028c460392cb8508f8ccc5d9}

None.

## Example {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```

