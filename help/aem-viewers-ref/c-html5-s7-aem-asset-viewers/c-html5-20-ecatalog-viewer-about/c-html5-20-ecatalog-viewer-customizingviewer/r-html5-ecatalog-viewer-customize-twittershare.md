---
title: Twitter share
description: Twitter share tool consists of a button added to the Social share panel. When the button is selected, the user is redirected to a sharing dialog box that is provided by a social service. The position of the button is fully managed by the Social share tool.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 31b6f36d-e4bc-44e9-88a1-6aff6f2254ef
---
# Twitter share{#twitter-share}

Twitter share tool consists of a button added to the Social share panel. When the button is selected, the user is redirected to a sharing dialog box that is provided by a social service. The position of the button is fully managed by the Social share tool.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

The appearance of the Twitter share button is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7twittershare
```

**CSS properties of the Twitter share tool** 

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Button height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> The image that is displayed for a given button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See also <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

It is possible to remove the button from the Social share panel by setting `display:none` CSS property on its CSS class.

The button tool tip can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) for more information.

Example - To set up a Twitter share button that is 28 x 28 pixels, and displays a different image for each of the four different button states:

```
.s7ecatalogviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7ecatalogviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7ecatalogviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7ecatalogviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
