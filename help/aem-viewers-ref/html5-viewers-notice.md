---
title: HTML5 Viewers SDK removing support for Adobe Flash-based video content notice
description: HTML5 Viewers SDK removing support for Adobe Flash-based video content.
---

# HTML5 Viewers SDK removing support for Adobe Flash-based video content notice {#html5-viewers-flash-notice}

Adobe is updating the HTML5 Viewers SDK to remove support for Flash-based video content. This change impacts the `VideoPlayer` component in the SDK, versions 2.2 to 3.4.
 
* Customers who used HTML5 viewers out-of-the-box are not impacted; no change is required.
 
* Customers who used the HTML5 Viewers SDK to create a customized player to support the HDS format are not impacted; no change is required. Videos will continue to be delivered in native HTML5 following completion of the update. 
 
* Customers who are using the HTML5 Viewers SDK on their own servers for HDS format support, must update their custom viewer configuration to explicitly use HTML5 for video playback. Following the completion of the update, HDS video playback will not be available. See the HTML5 SDK API documentation for more details. 