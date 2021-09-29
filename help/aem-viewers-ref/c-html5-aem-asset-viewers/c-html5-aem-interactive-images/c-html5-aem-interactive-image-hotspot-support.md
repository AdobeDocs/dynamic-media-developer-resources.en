---
title: Hotspot support
description: Hotspot support
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
---
# Hotspot support{#hotspot-support}

The viewer supports the rendering of hotspot icons on top of the main view. The appearance of hotspot icons is controlled through CSS as described in the Hotspots section.

See [Hotspots](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots can either activate a Quickview feature on the hosting web page by triggering a JavaScript callback or redirect a user to an external web page.

## Quickview hotspots {#section-cda48fc9730142d0bb3326bac7df3271}

These types of hotspots should be authored using the "Quickview" action type in Dynamic Media, of Adobe Experience Manager Assets - On-demand. When a user activates such a hotspot, the viewer runs the `quickViewActivate` JavaScript callback and passes the hotspot data to it. It is expected that the embedding web page listens for this callback. When it triggers the page, it opens its own Quickview implementation.

## Redirect to external web page {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots authored for the action type "Quick View" in Dynamic Media of Experience Manager Assets - On-demand redirects the user to an external URL. Depending on settings made during authoring, the URL opens in a new browser tab, in the same window, or in the named browser window.
