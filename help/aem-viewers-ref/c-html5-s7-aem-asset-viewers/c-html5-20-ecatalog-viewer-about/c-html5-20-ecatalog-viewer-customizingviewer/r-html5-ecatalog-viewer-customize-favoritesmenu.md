---
description: The Favorites menu drop-down list appears in the control bar. It consists of a button and a panel that expands when a user clicks or taps on a button. The panel contains individual Favorites tools.
seo-description: The Favorites menu drop-down list appears in the control bar. It consists of a button and a panel that expands when a user clicks or taps on a button. The panel contains individual Favorites tools.
seo-title: Favorites menu
solution: Experience Manager
title: Favorites menu
uuid: 816e614d-8253-49a8-b57e-0b57b44db535
feature: "Dynamic Media Classic,Viewers,SDK/API,eCatalog"
role: "Developer,Business Practitioner"
---

# Favorites menu{#favorites-menu}

The Favorites menu drop-down list appears in the control bar. It consists of a button and a panel that expands when a user clicks or taps on a button. The panel contains individual Favorites tools.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The position and size of the Favorites menu in the viewer user interface is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7favoritesmenu
```

**CSS properties of the Favorites menu button** 

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> The offset from the top of the control bar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> The distance to the next button on the left, or the left side of the control bar if this is the first button in a row. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of the button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of the button. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - set up a Favorites menu that is positioned four pixels from the top of the control bar and ten pixels from the closest button to the left and sized 28 x 28 pixels.

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

The appearance of the Favorites menu button is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

**CSS properties of the Favorites button**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
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

The button tool tip can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) for more information.

Example - set up a Favorites menu button that displays a different image for each of the four different button states.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

The appearance of the panel that contains individual Favorites icons is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**CSS properties of the Favorites menu panel**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>The background color of the panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - set up a panel to have a transparent color.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

