---
description: Certain content that the Carousel Viewer displays is subject to localization. This includes slide navigation buttons.
solution: Experience Manager
title: Localization of user interface elements
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
---
# Localization of user interface elements{#localization-of-user-interface-elements}

Certain content that the Carousel Viewer displays is subject to localization. This includes slide navigation buttons.

Every textual content in the viewer that can be localized is represented by the special Viewer SDK identifier called SYMBOL. Any SYMBOL has a default associated text value for an English locale ( `"en"`) supplied with the out-of-the-box viewer, and also may have user-defined values set for as many locales as needed.

When the viewer starts, it checks the current locale to see if there is a user-defined value for each supported SYMBOL for such locale. If there is, it uses the user-defined value; otherwise, it falls back to the out-of-the-box default text.

User-defined localization data can be passed to the viewer as a localization JSON object. Such object contains the list of supported locales, SYMBOL text values for each locale, and the default locale.

An example of such a localization object is the following:

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
}, 
defaultLocale:"en" 
}
```

In the example above, the localization object defines two locales ( `"en"` and `"fr"`) and provides localization for two user interface elements in each locale.

The web page code should pass the localization object to the viewer constructor, as a value of `localizedTexts` field of the configuration object. An alternative option is to pass the localization object by calling `setLocalizedTexts(localizationInfo)` method.

The following SYMBOLs are supported:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>Tool tip for... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Selected play pause button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Unselected play pause button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> Tool tip and ARIA label for previous and next slide buttons. </p> <p>Accepts two replacement tokens: <span class="codeph"> $CURRENT_FRAME$ </span> for the current slide index and <span class="codeph"> $TOTAL_FRAMES$ </span> for the total number of slides. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> ARIA label for top level viewer element. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> ARIA role description for main view component. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> ARIA usage hints for keyboard users. </p> </td> 
  </tr> 
 </tbody> 
</table>
