---
title: Customizing Flyout Viewer
description: Customizing Flyout Viewer
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b7898044-5178-4cdf-ab52-9996a61a3a35
---
# Customizing Flyout Viewer{#customizing-flyout-viewer}

All visual customization and most behavior customization are done by creating a custom CSS.

The suggested workflow is to take the default CSS file for the appropriate viewer, copy it to a different location, customize it, and specify the location of the customized file in the `style=` command.

Default CSS files can be found at the following location:

`<s7_viewers_root>/html5/FlyoutViewer.css`

Custom CSS file must contain the same class declarations as the default one. If a class declaration is omitted, the viewer does not function properly because it does not provide built-in default styles for user interface elements.

Alternative way to provide custom CSS rules is to use embedded styles directly on the web page or in one of linked external CSS rules.

When creating custom CSS, keep in mind that the viewer assigns `.s7flyoutviewer` class to its container DOM element. If you are using external CSS file passed with `style=` command, use `.s7flyoutviewer` class as parent class in descendant selector for your CSS rules. If you are doing embedded styles on the web page, also qualify this selector with an ID of the container DOM element as follows:

`#<containerId>.s7flyoutviewer`

## Building responsive designed CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

It is possible to target different devices and embedding sizes in CSS to make your content display differently, depending on a user's device or a particular web page layout. This ability includes, but is not limited to, different web page layouts, user interface element sizes, and artwork resolution.

The viewer supports two methods for creating responsive designed CSS: CSS markers and standard CSS media queries. You can use these methods independently or together.

**CSS markers**

To help create responsive designed CSS, the viewer supports CSS markers which special CSS classes dynamically assigned to the top-level viewer container element. The assignment is based on the run-time viewer size and the input type used on the current device.

The first group of CSS Markers includes `.s7size_large`, `.s7size_medium`, and `.s7size_small` classes. They are applied based on the runtime area of the viewer container. That is, if the viewer area is equal to or bigger than the size of a common desktop monitor `.s7size_large` is used; if the area is close in size to a common tablet device `.s7size_medium` is assigned. For areas similar to mobile phone screens, `.s7size_small` is set. The primary purpose of these CSS markers is to create different user interface layouts for different screens and viewer sizes.

The second group of CSS Markers includes `.s7mouseinput` and `.s7touchinput`. The marker `.s7touchinput` is set if the current device has touch input capabilities; otherwise, `.s7mouseinput` is used. These markers are intended to create user interface input elements with different screen sizes for different input types, because normally touch input requires larger elements. In cases where the device has both mouse input and touch capabilities, `.s7touchinput` is set and the viewer renders a touch-friendly user interface.

The following sample CSS sets the zoom in button size to 28 x 28 pixels on systems with mouse input, and 56 x 56 pixels on touch devices. In addition, it hides the button completely if the viewer size becomes small:

```
.s7flyoutviewer.s7mouseinput .s7swatches .s7thumb {  
 width: 28px; 
 height: 28px; 
} 
.s7flyoutviewer.s7touchinput .s7swatches .s7thumb {  
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer.s7size_small .s7swatches {  
 visibility: hidden; 
}
```

To target devices with a different pixel density, use CSS media queries. The following media query block would contain CSS that is specific for high-density screens:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Using CSS markers is the most flexible way of building responsive designed CSS. The reason is because it lets you target not only device screen size but actual viewer size, which may be useful for responsive designed web page layouts.

**CSS media queries**

Device sensing can also be done using pure CSS media queries. Everything enclosed within a given media query block is applied only when it is run on a corresponding device.

When applied to Mobile Viewers, use four CSS media queries, defined in your CSS in the following order:

1. Contains only rules specific for all touch devices.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. Contains only rules specific for tablets with high-resolution screens.

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

1. Contains only rules specific for mobile phones with high-resolution screens.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Using a media queries approach, you should organize CSS with device sensing as follows:

* First, the desktop-specific section defines all properties that are either desktop-specific or common to all screens. 
* And second, the four media queries go in the order defined above and provide CSS rules that are specific for the corresponding device type.

There is no need to duplicate the entire viewer CSS in each media query. Only properties that are specific to given devices are redefined inside a media query.

## CSS Sprites {#section-0711ece44a4740168cfd7624c9010bd1}

Many viewer user interface elements are styled using bitmap artwork and have more than one distinct visual state. A good example is a button that normally has at least three different states: "up", "over", and "down". Each state requires its own bitmap artwork assigned.

With a classic approach to styling, the CSS would have a separate reference to individual image file on the server for each state of the user interface element. The following is a sample CSS for styling scroll button:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-image:url(images/v2/ScrollLeftButton_up.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-image:url(images/v2/ScrollLeftButton_down.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-image:url(images/v2/ScrollLeftButton_disabled.png);  
}
```

The drawback to this approach is that the end user experiences flickering or delayed user interface response when the element is interacted with for the first time. This action occurs because the image artwork for the new element state is not yet downloaded. Also, this approach may have a slight negative impact on performance because of an increase in the number of HTTP calls to the server.

CSS sprites is a different approach where image artwork for all element states is combined into a single PNG file called a "sprite". Such "sprite" has all visual states for the given element positioned one after another. When styling a user interface element with sprites, the same sprite image is referenced for all different states in the CSS. Also, the `background-position` property is used for each state to specify which part of the "sprite" image is used. You can structure a "sprite" image in any suitable way. Viewers normally have it vertically stacked. Below is a "sprite"-based example of styling the same scroll button from above:

```
.s7flyoutviewer .s7scrollleftbutton[state]  { 
    background-image: url(images/v2/ScrollLeftButton_light_sprite.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-position: -56px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-position: -0px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-position: -56px -448px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-position: -0px -448px;  
}
```

## General styling notes and advice {#section-95855dccbbc444e79970f1aaa3260b7b}

* When customizing the viewer user interface with CSS, the use of the `!IMPORTANT` rule is not supported to style viewer elements. In particular, `!IMPORTANT` rule should not be used to override any default or run-time styling provided by the viewer or Viewer SDK. The reason is that it may affect the behavior of proper components. Instead, you should use CSS selectors with the proper specificity to set CSS properties that are documented in this reference guide. 
* All paths to external assets within CSS are resolved against the CSS location, not the viewer HTML page location. Be aware of this rule when you copy the default CSS to a different location. Either copy the default assets as well or update paths within the custom CSS. 
* The preferred format for bitmap artwork is PNG. 
* Bitmap artwork is assigned to user interface elements using the `background-image` property. 
* The `width` and `height` properties of a user interface element define its logical size. The size of the bitmap passed to `background-image` does not affect logical size. 
* To use the high pixel density of high-resolution screens like Retina, specify bitmap artwork twice as large as the logical user interface element size. Then, apply the `-webkit-background-size:contain` property to scale the background down to the logical user interface element size. 
* To remove a button from the user interface, add `display:none` to its CSS class. 
* You can use various formats for color value that CSS supports. If you need transparency, use the format `rgba(R,G,B,A)`. Otherwise, you can use the format `#RRGGBB`.

## Common User Interface Elements {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

The following is user interface elements reference documentation that applies to Flyout Viewer: 

* [Flyout zoom view](r-html5-flyout-viewer-20-customize-flyoutzoomview.md)
* [Focus highlight](r-html5-flyout-viewer-20-customize-focushighlight.md)
* [Main viewer area](r-html5-flyout-viewer-20-customize-mainviewerarea.md)
* [Swatches](r-html5-flyout-viewer-20-customize-swatches.md)
* [Tooltips](r-html5-flyout-viewer-20-customize-tooltips.md)
