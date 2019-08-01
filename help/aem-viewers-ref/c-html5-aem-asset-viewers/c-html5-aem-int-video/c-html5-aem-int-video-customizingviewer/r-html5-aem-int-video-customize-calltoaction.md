---
description: The Call to action panel appears when the video ends and displays all interactive swatches associated with the particular video.
seo-description: The Call to action panel appears when the video ends and displays all interactive swatches associated with the particular video.
seo-title: Call to action
solution: Experience Manager
title: Call to action
topic: Dynamic media
uuid: 04a042d8-7329-4f1d-b3b9-312d620b1f29
index: y
internal: n
snippet: y
---

# Call to action{#call-to-action}

The Call to action panel appears when the video ends and displays all interactive swatches associated with the particular video.

<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>

The panel consists of a header area showing the video title, a replay button in the upper-right corner, and actual interactive swatches shown as a scrollable grid. You can disable the panel using the [callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6) configuration attribute.

The call to action panel always takes the entire available viewer area.

<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>

The following CSS class selector controls the appearance of the background color in the call to action panel:

```
.s7interactivevideoviewer .s7calltoaction
```

## CSS properties of the background color of the call to action panel {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Background color of the call to action panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#example}

To set up a call to action panel with dark gray background:

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>

The following CSS class selector controls the appearance of the header in the call to action panel:

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## CSS properties of the call to action panel header {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Background color of the header. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of the header. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-bottom </span> </p> </td> 
   <td colname="col2"> <p>Bottom border of the header. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#example-1}

To set up a header that is 70 pixels tall, with a dark gray background, and a slightly lighter gray two pixel border along the bottom:

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>

The following CSS class selector controls the appearance of the header title in the call to action panel:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## CSS properties of the header title in the call to action panel:  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Text color inside the banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Font size. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Line height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Font family. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Alignment of text in the banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left </span> </p> </td> 
   <td colname="col2"> <p>Left padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right </span> </p> </td> 
   <td colname="col2"> <p> Right padding to allow space for the Replay button. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#example-2}

To set up a video title with a 70 pixel line height, 25 pixel font size, white color, and left aligned:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>

The following CSS class selector controls the appearance of the close button in the call to action panel:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## CSS properties of the close button in the call to action panel: {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position from the top of the header, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Position from the right of the header, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Button height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Image displayed for a given button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Position inside the artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button support the `state` attribute selector, which can be used to apply different skins to different button states.

## Example {#example-3}

To set up a replay button that is 28 x 28 pixels; positioned 20 pixels from the top and from the right edge of the header; displays a different image for each of the four different button states; takes the artwork from the component's sprite image:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>

The following CSS class selector controls the appearance of the thumbnail grid view in the call to action panel:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## CSS properties of the thumbnail grid view in the call to action panel:  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Background color of the thumbnails area. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#example-4}

To set up a thumbnails area with a dark gray background:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>

The following CSS class selector controls the appearance of the thumb cell in the call to action panel:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## CSS properties of the thumbcell in the call to action panel: {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Size of the horizontal and vertical margin around each thumbnail. </p> <p>Actual horizontal thumbnail spacing equals the sum of the left and right margin set for <span class="codeph"> .s7thumbcell </span>. The same rule also applies but to vertical spacing. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#example-5}

To set up horizontal spacing of 24 pixels and vertical spacing of 18 pixels:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>

The following CSS class selector controls the appearance of the thumbnail in the call to action panel:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## CSS properties of the thumbnail in the call to action panel: {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of the thumbnail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of the thumbnail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Border of the thumbnail. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumbnail supports the `state` attribute selector, which can be used to apply different skins to different thumbnail states. In particular, `state="selected"` corresponds to the thumbnail for the image currently selected; `state="default"` corresponds to the rest of thumbnails; `state="over"` is used on mouse hover.

## Example {#example-6}

To set up thumbnails that are 94 x 100 pixels:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>

The following CSS class selector controls the appearance of the thumbnail label in the call to action panel:

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## CSS properties of the thumbnail label in the call to action panel: {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Text color of label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Horizontal alignment of label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Font name. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Font family. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#example-7}

To set up labels that use a white color, be center-aligned 15 pixels, and use an Arial font:

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>

If there are more thumbnails than can fit vertically into view, thumbnails renders a vertical scroll bar on the right side. By default, the call to action panel renders a tiny vertical bar without thumb and scroll buttons. However, it is possible to customize the bar by altering the viewer CSS.

The following CSS class selector controls the appearance of the scroll bar area in the call to action panel:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## CSS properties of the scroll bar area in the call to action panel: {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Width of scroll bar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Vertical scroll bar offset from the top of the thumbnails area. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Vertical scroll bar offset from the bottom of the thumbnails area. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> Horizontal scroll bar offset from the right edge of the thumbnails area. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#example-8}

To set up a scroll bar that is 22 pixels wide and does not have any margin from the top, right, or bottom of the thumbnails area:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<a id="section_E27B7253441543278E1081D70BA46122"></a>

The scroll bar track is the area between the top and bottom scroll bar buttons. The component automatically sets the position and height of the track.

The following CSS class selector controls the appearance of the scroll bar track in the call to action panel:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## CSS properties of the scroll track bar {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of scroll track bar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Background color of the track bar. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#example-9}

To set up a scroll bar track that is 22 pixels wide and has a gray color:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>

The scroll bar thumb moves vertically within the scroll track area. Its vertical position is fully controlled by the component logic; however, the thumb height does not dynamically change depending on the amount of content.

The following CSS class selector controls the appearance of the thumb height and other aspect:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## CSS properties of the thumb height in the call to action panel: {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of thumb. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of thumb. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>Vertical padding between the top of the track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p>Vertical padding between the bottom of the track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Radius of border. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color of thumb. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Image displayed for a given thumb state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb supports the `state` attribute selector, which can be used to apply different skins to the following different thumb states: `"up"`, `"down"`, `"over"`, and `"disabled"`.

## Example {#example-10}

To set up a scroll bar thumb that is 6 x 167 pixels, has three pixel rounded corners, and a gray color:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>

The following CSS class selector controls the appearance of the top and bottom scroll buttons:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

It is not possible to position scroll buttons using CSS top, left, bottom, or right properties; the viewer logic positions them automatically. The call to action panel in the interactive video viewer does not use these buttons in the scroll bar, so their size is set to 0 pixels in the default CSS.

## CSS properties of the top and bottom scroll buttons in the call to action panel:  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Width of button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Image displayed for a given button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>These buttons support the `state` attribute selector, which can be used to apply different skins to the following different thumb states: `"up"`, `"down"`, `"over"`, and `"disabled"`.

The button tool tips can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Example {#example-11}

Disable scroll buttons by setting their size to 0 and hiding them:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```

