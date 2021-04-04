---
description: The viewer displays Favorites icons over the main view in places where it was originally added by the user.


solution: Experience Manager
title: Favorites effect

feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: e87226cf-56bf-4d54-8df5-91295eae90a8
---
# Favorites effect{#favorites-effect}

The viewer displays Favorites icons over the main view in places where it was originally added by the user.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The appearance of the Favorite icon is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**CSS properties of the Favorite icon**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> The image that is displayed for the icon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See also <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of the icon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of the icon. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - set up a 36 x 36 pixels Favorites icon.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

On desktop systems, the component supports the `cursortype` attribute selector which you can apply to the `.s7favoriteseffect` class and controls the type of the cursor based on the selected user action. The following `cursortype` values are supported:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>Displayed user is adding a new Favorite icon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>Displayed user is removing an existing Favorite icon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view </span> </p> </td> 
   <td colname="col2"> <p>Displayed in normal operation mode when Favorites editing is not active. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - have different mouse cursors for each type of component state.

```
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```
