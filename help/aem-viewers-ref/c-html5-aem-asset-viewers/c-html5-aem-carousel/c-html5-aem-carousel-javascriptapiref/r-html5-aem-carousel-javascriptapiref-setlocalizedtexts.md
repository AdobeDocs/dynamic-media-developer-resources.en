---
description: JavaScript API reference for Carousel Viewer.
seo-description: JavaScript API reference for Carousel Viewer.
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
uuid: f69d3232-dd7c-41b5-87a0-146b8fb1bdb1
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
---

# setLocalizedTexts{#setlocalizedtexts}

JavaScript API reference for Carousel Viewer.

 ` setLocalizedTexts( *`localizationInfo`*)`

Sets localization SYMBOL values for one or more locales. This parameter must be called before `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSON object with localization data. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local"> Localization of user interface elements</a> for more information. </p> <p>See also the <i>Viewer SDK User Guide</i> and the example for more information about the object's content. </p> </td> 
  </tr> 
 </tbody> 
</table>

See also [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```

