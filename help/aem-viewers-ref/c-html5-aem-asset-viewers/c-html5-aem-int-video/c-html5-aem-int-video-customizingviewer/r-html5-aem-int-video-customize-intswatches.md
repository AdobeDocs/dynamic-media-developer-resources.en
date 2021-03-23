---
description: The interactive swatches panel appears next to the video content if interactive data was passed to the viewer in configuration. It consists of a banner at the top that renders text such as "Click to View", a column of one or more interactive swatches and two scroll buttons (available only on desktop systems).


solution: Experience Manager
title: Interactive swatches

feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
---

# Interactive swatches{#interactive-swatches}

The interactive swatches panel appears next to the video content if interactive data was passed to the viewer in configuration. It consists of a banner at the top that renders text such as "Click to View", a column of one or more interactive swatches and two scroll buttons (available only on desktop systems).

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

On desktop systems and on touch devices, in landscape orientation, interactive swatches are rendered vertically to the right of the video content. On touch devices in portrait orientation they appear at the bottom of the viewer, as a horizontal row of swatches.

The following CSS class selector controls the location and orientation of the interactive swatches panel:

```
.s7interactivevideoviewer .s7interactiveswatches
```

## CSS properties of the interactive swatches {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of the interactive swatches panel </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of the interactive swatches panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Top position of he interactive swatches panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Bottom position of the interactive swatches panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Left position of the interactive swatches panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Right position of the interactive swatches panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

The run-time location and orientation of the interactive swatches panel is defined by a combination of the above CSS properties as follows:

* To render interactive swatches horizontally at the bottom of the viewer, set the height to an absolute pixel value; left and bottom to 0px; width, right, and top to auto. 
* To render interactive swatches vertically to the right of the video content, set the width to an absolute pixel; right and top to 0px; height, left and bottom to auto.

It is possible to use CSS markers in conjunction with this styling to achieve adaptive placement of the interactive swatches panel.

## Example {#example}

To set up an interactive swatches panel to render horizontally at the bottom of the viewer on touch devices in landscape orientation and to show vertically to the right of the video content in all other cases:

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The size and position of the banner is managed by the interactive swatches component based on other styling applied with CSS and cannot be set explicitly.

The following CSS class selector controls the appearance of the banner panel:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## CSS properties of the banner panel {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Background color of the banner panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Text color inside the banner panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Border around the banner panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>The font weight to use for the text inside the banner panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>The font size to use for the text inside the banner panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>The font family to use for the text inside the banner panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>The font alignment to use for the text inside the banner panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

The banner tool tip can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) for more information.

## Example {#section-e8caea0a303c425a8a637c2a47c06355}

To set up a banner with dark gray background, lighter gray two pixel border and the white text centered horizontally:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

The following CSS class selector controls the appearance of the swatches:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## CSS properties of the swatches area {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Background color of the swatches area. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-9cadd62a09fd44a280f55ff42437e416}

To set up swatches area with dark gray background:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

The following CSS class selector controls the spacing between swatch thumbnails:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## CSS properties of the swatches thumbnail spacing {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> The size of the horizontal and vertical margin around each thumbnail. The actual thumbnail spacing equals to the sum of the left and right margin set for <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-39fb270b7e494a9d99e6e8f6890ec53c}

To set up vertical spacing to be 10 pixels:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

The following CSS class selector controls the appearance of individual thumbnails:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## CSS properties of the appearance of individual thumbnails {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
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
>Thumbnail supports the `state` attribute selector, which you can use to apply different skins to different thumbnail states. In particular, `state="selected"` corresponds to the thumbnail for the currently selected image; `state="default"` corresponds to the rest of thumbnails; `state="over"` is used on mouse hover.

## Example {#section-69fec189ffaa440b97b6b846c320b75b}

To set up thumbnails that are 100 x 75 pixels:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

The following CSS class selector controls the appearance of the thumbnail label:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## CSS properties of the appearance of the thumbnail label {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Text color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Label border. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Horizontal text alignment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Font name. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-eb141eb6c1154183baa69796edb90536}

To set up labels to use left-aligned, white, 12 pixels, in Helvetica font, and a bottom border:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

The following CSS class selector controls the appearance of the up and down scroll buttons:

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

It is not possible to position the scroll buttons using CSS `top`, `left`, `bottom`, and `right` properties; instead, the viewer logic positions them automatically.

## CSS properties of the appearance of the up and down scroll buttons {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of the scroll button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of the scroll button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>The image that is displayed for a given button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>The position inside the artwork sprite, if CSS sprites are used. </p> <p>See also <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports the `state` attribute selector, which you can use to apply different skins to the button states: " `up`", " `down`", " `over`", and " `disabled`".

The button tool tips can be localized. See [Localization of user interface elements](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) for more information.

## Example {#section-e6ce4fa084b84288bc7583342b2c510c}

To set up scroll up button that is 60 x 36 pixels, have different artwork for each state and takes that artwork from the component's sprite image:

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```

