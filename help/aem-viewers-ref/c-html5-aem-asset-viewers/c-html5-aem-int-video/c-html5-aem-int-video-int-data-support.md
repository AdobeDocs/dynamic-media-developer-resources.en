---
description: The Video Video Viewer supports rendering interactive swatches based on interactive data passed to the viewer as a configuration parameter.
seo-description: The Video Video Viewer supports rendering interactive swatches based on interactive data passed to the viewer as a configuration parameter.
seo-title: Interactive data support
solution: Experience Manager
title: Interactive data support
topic: Dynamic media
uuid: 70b2ec2e-0ea7-461d-a185-731fb0ef8f3e
index: y
internal: n
snippet: y
---

# Interactive data support{#interactive-data-support}

The Video Video Viewer supports rendering interactive swatches based on interactive data passed to the viewer as a configuration parameter.

 The currently visible swatch corresponds to the video time region with which it is associated. Clicking or tapping the interactive swatch triggers the action assigned to it at author time.

Interactive swatch can either activate a Quick View on the hosting web page by triggering a JavaScript callback or it can redirect the user to an external web page.

## About Quick View {#section-7990e44f641042d2a38ba20c9413b3f8}

These types of interactive swatches should be authored using the action type "quickview" in AEM Assets - on-demand. When a user activates such a swatch, the viewer runs `quickViewActivate` JavaScript callback and passes the swatch data to it. It is expected that the embedding web page listens to this callback and when it triggers, the page opens its own Quick View implementation.

## Redirect to an external web page {#section-32ebe3c3a7f74892a428c5d48801de4d}

Swatches authored for the action type "quickview" in AEM Assets - on-demand redirect the user to an external URL. Depending on the settings at the time of authoring, the URL can open either in a new browser tab, in the same window, or in the named browser window. 
