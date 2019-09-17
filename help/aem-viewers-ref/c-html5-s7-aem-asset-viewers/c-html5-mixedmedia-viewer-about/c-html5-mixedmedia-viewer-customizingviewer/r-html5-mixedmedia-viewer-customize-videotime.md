---
description: The video time is the numeric display that shows the current time and duration of the currently playing video.
seo-description: The video time is the numeric display that shows the current time and duration of the currently playing video.
seo-title: Video time
solution: Experience Manager
title: Video time
topic: Dynamic media
uuid: f93e495b-44a1-493c-9bc6-5c088478ddce
---

# Video time{#video-time}

The video time is the numeric display that shows the current time and duration of the currently playing video.

<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>

The video time font family, font size, and font color are among the properties that CSS can control. It can also be positioned, relative to the control bar that contains it, by CSS.

The appearance of the video time is controlled with the following CSS class selector:

```
.s7mixedmediaviewer .s7videotime
```

## CSS properties of video time {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position from the top border, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Position from the right border, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> The width of video time control. This property is required for Internet Explorer 8 or greater to function properly. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>The font family to use for the time display text. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>The font size to use for the time display text. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>The font color to use for the time display text. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-e8caea0a303c425a8a637c2a47c06355}

Set the video time to light gray (hexadecimal `#BBBBBB`), sized at 12 pixels, positioned 15 pixels from the top of the control bar, and 80 pixels from the right edges of the control bar.

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```

