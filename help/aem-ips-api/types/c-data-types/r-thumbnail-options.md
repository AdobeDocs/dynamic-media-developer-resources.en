---
description: An optional type that lets you choose a particular video frame to use as the thumbnail image.
seo-description: An optional type that lets you choose a particular video frame to use as the thumbnail image.
seo-title: ThumbnailOptions
solution: Experience Manager
title: ThumbnailOptions
topic: Dynamic Media Image Production System API
uuid: 50b2ecee-8396-4323-83e1-1f5060bec6c4
---

# ThumbnailOptions{#thumbnailoptions}

An optional type that lets you choose a particular video frame to use as the thumbnail image.

 Syntax 

## Parameters {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>Sets in the time (in milliseconds from video start) for the frame you want to use for the video thumbnail. Values range from 0 to the end of the video. <p>Note: The system uses the first frame of the video for the thumbnail if you specify the time incorrectly. See <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```

