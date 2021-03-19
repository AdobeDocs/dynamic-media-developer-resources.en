---
description: Certain content that the Basic Zoom Viewer displays is subject to localization, including zoom buttons and a full screen button.
seo-description: Certain content that the Basic Zoom Viewer displays is subject to localization, including zoom buttons and a full screen button.
seo-title: Localization of user interface elements
solution: Experience Manager
title: Localization of user interface elements
uuid: 842970d9-0882-4163-8c49-3ea35d372d35
feature: "Dynamic Media Classic,Viewers,SDK/API,Zoom"
role: "Developer,Business Practitioner"
---

# Localization of user interface elements{#localization-of-user-interface-elements}

Certain content that the Basic Zoom Viewer displays is subject to localization, including zoom buttons and a full screen button.

Every textual content in the viewer that can be localized is represented by a special Viewer SDK identifier called SYMBOL. Any SYMBOL has a default associated text value for the English locale ( `"en"`) supplied with the out-of-the-box viewer, and also may have user-defined values set for as many locales as needed.

When the viewer starts, it checks the current locale to see if there is a user-defined value for each supported SYMBOL in the locale. If there is, it uses the user-defined value; otherwise, it falls back to the out-of-the-box default text.

User-defined localization data can be passed to the viewer as a localization JSON object. Such an object contains the list of supported locales, SYMBOL text values for each locale, and the default locale.

An example of such localization object:

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

In the example above, the localization object defines two locales ( `"en"` and `"fr"`) and provides localization for two user interface elements in each locale.

The web page code should pass such localization object to the viewer constructor as a value of `localizedTexts` field of the configuration object. An alternative option is to pass the localization object by calling `setLocalizedTexts(localizationInfo)` method.

The following SYMBOLs are supported:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>Tooltip for the... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>ARIA label for the top-level viewer element. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>ARIA role description for the main view component. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA usage hints for keyboard users. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Close button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Zoom in button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Zoom out button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Zoom reset button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Full screen button in normal state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Full screen button in full screen state. </p> </td> 
  </tr> 
 </tbody> 
</table>

