---
description: URL command for Video Viewer.
seo-description: URL command for Video Viewer.
seo-title: caption
solution: Experience Manager
title: caption
topic: Dynamic media
uuid: 670d83c2-bfc5-411a-8581-5103a62aa8cf
index: y
internal: n
snippet: y
---

# caption{#caption}

URL command for Video Viewer.

 ` caption= *`file`*[,0|1]`

The viewer supports closed captioning through hosted WebVTT files. Overlapping cues and regions are not supported. Supported cue positioning operators include the following: 

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Key </p> </th> 
   <th colname="col2" class="entry"> <p>Name </p> </th> 
   <th colname="col3" class="entry"> <p>Value </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>text align </p> </td> 
   <td colname="col3"> <p><span class="codeph"> left|right|middle|start|end</span> </p> </td> 
   <td colname="col4"> <p> Control text alignment. </p> <p>Default is <span class="codeph"> middle</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>text position </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentage of inset into the VideoPlayer component for the beginning of the caption text. </p> <p>Default is 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>line size </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentage of video width used for captions. </p> <p>Default is 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>line position </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> Determines the line position on the page. </p> <p>If it is expressed as an integer (no percent sign), then it is the number of lines from the top where the text is displayed. </p> <p>If it is a percentage (the percent sign is the last character), then the caption text is displayed that percent down the display area. </p> <p>Default is 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

Other WebVTT features present in the WebVTT file are not supported, but should not disrupt the captioning. 

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> file</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies a URL or path to the WebVTT caption content. Serve the WebVTT file by ImageServing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Specifies the default caption state (enabled is <span class="codeph"> 1</span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

None.

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```

