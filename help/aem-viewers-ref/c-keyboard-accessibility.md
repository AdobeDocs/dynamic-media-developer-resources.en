---
description: All features exposed in the Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Dimensional (3D), Carousel, Interactive Image, Interactive Video, and Video360 viewer interface are keyboard accessible.
solution: Experience Manager
title: Keyboard accessibility and navigation
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
---

# Keyboard accessibility and navigation{#keyboard-accessibility-and-navigation}

All features exposed in the Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Carousel, Dimensional (3D), Interactive Image, Interactive Video, and Video360 viewer interface are keyboard accessible.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Keyboard accessibility and navigation {#topic-f5650e9493404e55a3627c8d1366b861}

All features exposed in the Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Carousel, Dimensional (3D), Interactive Image, Interactive Video, and Video360 viewer interface are keyboard accessible. 

An end user can navigate between viewer user interface elements using **[!UICONTROL Tab]** and **[!UICONTROL Shift+Tab]** keystrokes. Using **[!UICONTROL Tab]** advances input focus to the next user interface element in the tabbing order; using **[!UICONTROL Shift+Tab]** brings input focus back to the previous user interface element. The focus traversal follows the natural user interface element location on the screen and moves in a left-to-right, then top-to-bottom order.

Depending on the operating system and web browser settings, the user interface element that has input focus may receive a visual focus indication. For example, the visual indicator can be a thin border rendered around the user interface element.

It is possible to disable or customize such focus highlight in the viewer CSS. In the table of contents of this Help system, under a specific viewer name (for example, Basic Zoom or Interactive Video), click **Customizing*name of viewer*** > **Focus highlight**.

Keystrokes supported by individual viewer user interface elements are-in most cases-obvious and easy to discover.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Action </p> </th> 
   <th colname="col2" class="entry"> <p>Keystroke </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Activate button components </p> </td> 
   <td colname="col2"> <p>Space or Enter key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoom in or out </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> or <span class="uicontrol"> - </span>, respectively. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoom reset </p> </td> 
   <td colname="col2"> <p>Esc key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pan </p> </td> 
   <td colname="col2"> <p>Up, down, left, or right arrow key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Spinning a 360 degree image </p> </td> 
   <td colname="col2"> <p>Use arrow keys when the image is in a reset state. </p> <p>Use up or down arrow key when working with multi-dimensional spin sets. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Product swatch selection </p> </td> 
   <td colname="col2"> <p>Up, down, left, or right arrow key; Home or End key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Product swatch activation </p> </td> 
   <td colname="col2"> <p>Space or Enter key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video and Interactive Video, gradual rewind </p> </td> 
   <td colname="col2"> <p>Left or up arrow key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video and Interactive Video, fast forward </p> </td> 
   <td colname="col2"> <p>Right or down arrow key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video and Interactive Video, go to beginning or end </p> </td> 
   <td colname="col2"> <p>Home or End key, respectively. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video and Interactive Video, control volume level when focus is on slider </p> </td> 
   <td colname="col2"> <p>Up, down, left, or right arrow key; Home or End key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video and Interactive Video, mutable volume </p> </td> 
   <td colname="col2"> <p>Arrow, Home, and End keys to control volume level when focus is on its slider part. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Video, when modal dialog box is displayed, focus traversal becomes limited to dialog box controls only. </p> </td> 
   <td colname="col2"> <p>Esc key to close the dialog box. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carousel, change banner image in main view </p> </td> 
   <td colname="col2"> <p>Left or right arrow key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carousel, hotspot selection and hotspot activation </p> </td> 
   <td colname="col2"> <p>Hotspot selection: up, down, left, or right arrow key </p> <p>Hotspot activation: Space or Enter key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, change the page image in the main view </p> </td> 
   <td colname="col2"> <p> Left or right arrow keys. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, thumbnail selection </p> </td> 
   <td colname="col2"> <p>Arrow keys; Home and End key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, swatch activation </p> </td> 
   <td colname="col2"> <p>Space or Enter key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, hot spot selection </p> </td> 
   <td colname="col2"> <p>Arrow keys. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, activation </p> </td> 
   <td colname="col2"> <p>Space or Enter keys. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, activating drop-down components </p> </td> 
   <td colname="col2"> <p> Down arrow key; Space, or Enter key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, when focus is in drop-drown panel </p> </td> 
   <td colname="col2"> <p>Use arrow keys to select a specific item in the panel before activating it. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, when a modal dialog box is displayed, focus traversal becomes limited to dialog box controls only. </p> </td> 
   <td colname="col2"> <p>Esc key to close the dialog box. </p> </td> 
  </tr> 
 </tbody> 
</table>

