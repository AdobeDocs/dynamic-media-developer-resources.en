---
title: Interactive data support
description: The Interactive Video Viewer supports rendering interactive swatches based on interactive data passed to the viewer as a configuration parameter.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
TQID: 'https://experienceleague.adobe.com/HE4LeluT9FWi8xgQf259b1yakK0oQjeR3rDME0juZiU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
---
# Interactive data support{#interactive-data-support}

The Interactive Video Viewer supports rendering interactive swatches based on interactive data passed to the viewer as a configuration parameter.

 The currently visible swatch corresponds to the video time region with which it is associated. Clicking or tapping the interactive swatch triggers the action assigned to it at author time.

Interactive swatch can either activate a Quickview on the hosting web page by triggering a JavaScript callback or it can redirect the user to an external web page.

## About Quickview {#section-7990e44f641042d2a38ba20c9413b3f8}

These types of interactive swatches should be authored using the action type "quickview" in Adobe Experience Manager Assets - On-demand. When a user activates such a swatch, the viewer runs `quickViewActivate` JavaScript callback and passes the swatch data to it. It is expected that the embedding web page listens to this callback and when it triggers, the page opens its own Quickview implementation.

## Redirect to an external web page {#section-32ebe3c3a7f74892a428c5d48801de4d}

Swatches authored for the action type "quickview" in Experience Manager Assets - on-demand redirect the user to an external URL. Depending on the settings at the time of authoring, the URL can open either in a new browser tab, in the same window, or in the named browser window.
