---
description: Customizing Smart Crop Video Viewer
keywords: responsive
solution: Experience Manager
title: Customizing Smart Crop Video Viewer

feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 90dc93ee-fdd0-41c9-9eef-4c9952198356
---
# Customizing Smart Crop Video Viewer{#customizing-smartcrop-video-viewer}

All visual customization and most behavior customization is done by creating a custom CSS.

The suggested workflow is to take the default CSS file for the appropriate viewer, copy it to a different location, customize it, and specify the location of the customized file in the `style=` command.

Default CSS files can be found at the following location:

`<s7_viewers_root>/html5/SmartCropVideoViewer.css`

Custom CSS file must contain the same class declarations as the default one. If a class declaration is omitted, the viewer does not function properly because it does not provide built-in default styles for user interface elements.

An alternative way to provide custom CSS rules is to use embedded styles directly on the web page or in one of linked external CSS rules.

When you create custom CSS remember that the viewer assigns `.s7smartcropvideoviewer` class to its container DOM element. If you use an external CSS file that is passed with the `style=` command, use `.s7smartcropvideoviewer` class as parent class in descendant selector for your CSS rules. If you embed styles on the web page, additionally qualify this selector with an ID of the container DOM element as follows:

`#<containerId>.s7smartcropvideoviewer`

## Building responsive designed CSS {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

It is possible to target different devices in CSS to make your content display differently depending on a user's device. This targeting includes, but is not limited to, different user interface element sizes and artwork resolution.

The viewer supports two mechanisms of creating responsive designed CSS: CSS markers and standard CSS media queries. You can use these independently or together.

**CSS markers**

To assist in creating responsive designed CSS, the viewer supports CSS markers which special CSS classes dynamically assigned to the top-level viewer container element based on the run-time viewer size and the input type used on the current device.

The first group of CSS markers includes `.s7size_large`, `.s7size_medium`, and `.s7size_small` classes. They are applied based on the runtime area of the viewer container. That is, if the viewer area is equal to or bigger than the size of a common desktop monitor `.s7size_large` is used; if the area is close in size to a common tablet device `.s7size_medium` is assigned. For areas similar to mobile phone screens `.s7size_small` is set. The primary purpose of these CSS markers is to create different user interface layouts for different screens and viewer sizes.

The second group of CSS markers includes `.s7mouseinput` and `.s7touchinput`. `.s7touchinput` is set if the current device has touch input capabilities; otherwise, `.s7mouseinput` is used. These markers are intended to create user interface input elements with different screen sizes for different input types, because normally touch input requires larger elements. In case the device has both mouse input and touch capabilities, `.s7touchinput` is set and the viewer renders a touch-friendly user interface.

The following sample CSS sets the play/pause button size to 28 x 28 pixels on systems with mouse input, and 56 x 56 pixels on touch devices. In addition, it hides the button completely if the viewer size becomes really small:

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7smartcropvideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7smartcropvideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

To target devices with a different pixel density, use CSS media queries. The following media query block would contain CSS that is specific to high density screens:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Using CSS markers is the most flexible way of building responsive designed CSS as it allows you to target not only device screen size but actual viewer size, which may be useful for responsive design page layouts.

Use the default viewer CSS file as an example of a CSS markers approach.

**CSS media queries**

Device sensing can also be done using pure CSS media queries. Everything enclosed within a given media query block is applied only when it is run on a corresponding device.

When applied to Mobile Viewers, use four CSS media queries, defined in your CSS in the order listed below:

1. Contains only rules specific for all touch devices.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. Contains only rules specific for tablets with high resolution screens.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Contains only rules specific for all mobile phones.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Contains only rules specific for mobile phones with high resolution screens.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Using the CSS media queries approach, you should organize CSS with device sensing as follows:

* First, the desktop-specific section defines all properties which are either desktop-specific or common to all screens. 
* Second, the four media queries should go in order defined above and provide CSS rules specific for corresponding device type.

There is no need to duplicate the entire viewer CSS in each media query. Only properties that are specific to given devices are redefined inside a media query.

## CSS Sprites {#section-9b6d8d601cb441d08214dada7bb4eddc}

Many viewer user interface elements are styled using bitmap artwork and have more than one distinct visual state. A good example is a button that normally has at least 3 different states: "up", "over", and "down". Each state requires its own bitmap artwork assigned.

With a classic approach to styling, the CSS would have a separate reference to individual image file on the server for each state of the user interface element. The following is a sample CSS for styling a full screen button:

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

The drawback to this approach is that the end user experiences flickering or delayed user interface response when the element is interacted with for the first time. This action occurs because the image artwork for the new element state is not yet downloaded. Also, this approach may have a slight negative impact on performance because of an increase in the number of HTTP calls to the server.

CSS sprites is a different approach where image artwork for all element states is combined into a single PNG file called a "sprite". Such "sprite" has all visual states for the given element positioned one after another. When styling a user interface element with sprites the same sprite image is referenced for all different states in the CSS. Also, the `background-position` property is used for each state to specify which part of the "sprite" image is used. You can structure a "sprite" image in any suitable way. Viewers normally have it vertically stacked. Below is a "sprite"-based example of styling the same full screen button from above:

```
.s7smartcropvideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## General styling notes and advice {#section-097418bd618740bba36352629e4d88e1}

* All paths to external assets within CSS are resolved against the CSS location not the location of the viewer HTML page. Remember to take this rule into account when you copy the default CSS to a different location. Copy the default assets or update paths within the custom CSS. 
* The preferred format for bitmap artwork is PNG. 
* Bitmap artwork is assigned to user interface elements using the `background-image` property. 
* The `width` and `height` properties of a user interface element define its logical size. The size of the bitmap passed to `background-image` does not affect logical size. 

* To use the high pixel density of high-resolution screens like Retina, specify bitmap artwork twice as large as the logical user interface element size. Then, apply the `-webkit-background-size:contain` property to scale the background down to the logical user interface element size. 
* To remove a button from the user interface, add `display:none` to its CSS class. 
* You can use various formats for color value that CSS supports. If you need transparency, use the format `rgba(R,G,B,A)`. Otherwise, you can use the format `#RRGGBB`. 

* When customizing the viewer user interface with CSS the use of the `!IMPORTANT` rule is not supported to style viewer elements. In particular, `!IMPORTANT` rule should not be used to override any default or run-time styling provided by the viewer or Viewer SDK. The reason is that it may affect the behavior of proper components. Instead, you should use CSS selectors with the proper specificity to set CSS properties that are documented in this reference guide.

## Common User Interface Elements {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

The following is user interface elements reference documentation that applies to Smart Crop Video Viewer:
