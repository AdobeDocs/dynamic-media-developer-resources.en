---
description: JavaScript API reference for Flyout Viewer.


solution: Experience Manager
title: setLocalizedTexts

feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
---

# setLocalizedTexts{#setlocalizedtexts}

JavaScript API reference for Flyout Viewer.

 ` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Object </span>} JSON object with localization data. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Localization of user interface elements </a> for more information. </p> <p>See the <i>Viewer SDK User Guide</i> and the example for more information about the object's content. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sets localization SYMBOL values for one or more locales. This parameter must be called before `init()`.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom"},"fr":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer"},defaultLocale:"en"})
```

