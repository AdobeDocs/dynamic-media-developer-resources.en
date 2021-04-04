---
description: Certain content that the eCatalog Viewer displays is subject to localization, including zoom buttons, page change buttons, thumbnail button, full screen button, close button, and scroll bar buttons.


solution: Experience Manager
title: Localization of user interface elements

feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
exl-id: c44bfb38-a523-4399-8dbd-936830bb7cac
---
# Localization of user interface elements{#localization-of-user-interface-elements}

Certain content that the eCatalog Viewer displays is subject to localization, including zoom buttons, page change buttons, thumbnail button, full screen button, close button, and scroll bar buttons.

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

The following SYMBOLs are supported (assuming containerId is theID of the viewer container):

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>Tool tip for... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>ARIA label for the top-level viewer element. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>ARIA role description for the main view component. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.USAGE_HINT </span> </p> </td> 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Scroll up button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Scroll down button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_rightButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Large next page button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_leftButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Large previous page button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_lastPageButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Last page button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_secondaryLastPageButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Last page button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_firstPageButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>First page button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_secondaryFirstPageButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>First page button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_toolBarRightButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Next page button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_toolBarLeftButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Previous page button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Thumbnails button in thumbnails mode. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Thumbnails button in normal mode. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Close button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InfoPanelPopup.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Info Panel close button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Social share tool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Email share button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Email dialog header. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Email dialog box upper-right close button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSS </span> </p> </td> 
   <td colname="col2"> <p>Error message displayed in case email address is malformed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO </span> </p> </td> 
   <td colname="col2"> <p>Label for the "To" input field. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD </span> </p> </td> 
   <td colname="col2"> <p>Add Another Email Address button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD </span> </p> </td> 
   <td colname="col2"> <p>Add Another Email Address button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.FROM </span> </p> </td> 
   <td colname="col2"> <p>From input field. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE </span> </p> </td> 
   <td colname="col2"> <p>Message input field. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE </span> </p> </td> 
   <td colname="col2"> <p>Remove Email Address button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Caption for the Cancel button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Cancel button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Caption for the Select All button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Select All button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Caption for the close button displayed in the bottom of dialog after form submission. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Close button that is displayed in the bottom of dialog after form submission. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Caption for the form submission button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Form submission button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS </span> </p> </td> 
   <td colname="col2"> <p>Confirmation message displayed when email was sent successfully. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE </span> </p> </td> 
   <td colname="col2"> <p>Error message that is displayed when email was not sent successfully. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Embed share button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Embed dialog box header. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Embed dialog box upper-right close button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Description of the embed code text. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Label for the embed size combo box. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Caption for the Cancel button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Cancel button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Text for the last "custom size" entry in the embed size combo box. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Link share button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Link dialog box header. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Link dialog box upper-right close button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Description of the share link. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Caption for the Cancel button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Cancel button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Caption for the Select All button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Select All button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Facebook share button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Twitter share button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Print button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Print dialog header. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Print dialog box top right close button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE </span> </p> </td> 
   <td colname="col2"> <p>Label for the "Select Print Pages" section. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_CURRENT </span> </p> </td> 
   <td colname="col2"> <p>Caption for the "Current pages" radio button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_FROM </span> </p> </td> 
   <td colname="col2"> <p>Caption for the "Spread range from" radio button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_TO </span> </p> </td> 
   <td colname="col2"> <p>Caption for the "to" numeric picker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_ALL </span> </p> </td> 
   <td colname="col2"> <p>Caption for the "All pages" radio button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING </span> </p> </td> 
   <td colname="col2"> <p>Label for the "Page Handling" section. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_ONE </span> </p> </td> 
   <td colname="col2"> <p>Caption for the "1 page per sheet" radio button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_TWO </span> </p> </td> 
   <td colname="col2"> <p>Caption for the "2 pages per sheet" radio button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Caption for the Cancel button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p> Cancel button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Caption for the Send to print button </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Send to print button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesMenu.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Favorites menu button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>"Add favorite" button in edit Favorites mode. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>"Add favorite" button in normal mode. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>"Remove favorite" button in edit Favorites mode. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>"Remove favorite" button in normal mode. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>"View all favorites" button when Favorites view is active. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>"View all favorites" button when Favorites view is inactive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesEffect.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Single favorite icon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_XX[_YY] </span> </p> </td> 
   <td colname="col2"> <p>Page label that is generated by the viewer at load time. </p> <p>The name of that symbol is a template, where <span class="codeph"> XX </span> is a zero-based spread index in landscape orientation, and optional <span class="codeph"> YY </span> is a zero-based page index inside the spread targeted by <span class="codeph"> XX </span>. </p> <p>Applies only for the initially loaded asset; ignored if an asset is changed using the <span class="codeph"> setAsset() </span> API call. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_DELIM </span> </p> </td> 
   <td colname="col2"> <p> Character used as a page labels delimiter in case labels are defined for left and right pages within a spread. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Main control bar scroll left button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Main control bar scroll right button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.PLACEHOLDER </span> </p> </td> 
   <td colname="col2"> <p>Localized prompt shown inside search input box before user starts entering the search text. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_PROMPT </span> </p> </td> 
   <td colname="col2"> <p>Localized message shown when the search panel is opened for the first time, suggesting user perform the search. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_NO_RESULTS </span> </p> </td> 
   <td colname="col2"> <p>Localized message shown when the search did not return any results. </p> <p>This symbol supports the following runtime replacement token: <span class="codeph"> $SEARCH_TEXT$ </span>. The component replaces it with the search text entered by the user. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_RESULTS </span> </p> </td> 
   <td colname="col2"> <p>Localized message shown when the search is successfully completed and returneds at least one result. </p> <p>This symbol supports the following runtime replacement tokens: </p> <p> 
     <ul id="ul_30B76EAB921848069BE843A5F91F697A"> 
      <li id="li_16AF3EFCC4BF4180B66DE5EA82CC77F4"> <span class="codeph"> $SEARCH_TEXT$ </span> - The search text entered by the user. </li> 
      <li id="li_A0FBF12344B04BF0B702A2B7473330A8"> <span class="codeph"> $HIT_COUNT$ </span> - The total number of search hits found. </li> 
      <li id="li_9EB7B41A989B455ABEC72E052284F117"> <span class="codeph"> $PAGE_COUNT$ </span> - The number of catalog pages that contain at least one search hit. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.THUMBNAIL_LABEL </span> </p> </td> 
   <td colname="col2"> <p>Localized label for results thumbnail of search panel. </p> <p>This symbol supports the following runtime replacement tokens: </p> <p> 
     <ul id="ul_7620C59FA56544CD9CE9E49B1871BCC1"> 
      <li id="li_FAF092734B4B4B55A309413690DA3FCC"> <span class="codeph"> $PAGE$ </span> - Page number. </li> 
      <li id="li_3414176505BB4A768FB42341A315E96F"> <span class="codeph"> $PAGE_HIT_COUNT$ </span> - The number of search results found on the page. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.LABEL </span> </p> </td> 
   <td colname="col2"> <p>Defines a value of the <span class="codeph"> aria-label </span> ARIA attribute for the entire search panel. </p> </td> 
  </tr> 
 </tbody> 
</table>
