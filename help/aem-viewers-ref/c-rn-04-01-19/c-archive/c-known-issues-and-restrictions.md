---
description: Enhancements, bug fixes, and known issues in Scene7 Viewers 4.9.2
seo-description: Enhancements, bug fixes, and known issues in Scene7 Viewers 4.9.2
seo-title: Scene7 Viewers 4.9.2 Release Notes
solution: Experience Manager
title: Scene7 Viewers 4.9.2 Release Notes
topic: Dynamic media
uuid: 285c2170-90e8-44dd-bacd-9debd8590afc
---

# Scene7 Viewers 4.9.2 Release Notes{#scene-viewers-release-notes}

Enhancements, bug fixes, and known issues in Scene7 Viewers 4.9.2

## Enhancements in Scene7 Viewers 4.9.2 {#section-0b0363fae0274737bace119f281e740f}

Viewer upgrades are backwards compatible and therefore, no changes are necessary to your existing web code. However, it is recommended that you test the new viewers on our staging environment. Contact Technical Support for instructions on how to access the staging server so you can test your viewers. After this is done, you can check your website to test the upgrades.

* Increased minimum requirements for viewers to iOS6. 
* Added support for custom event tracking to viewers. 
* Added support to set the initial bit rate for Video viewer. 
* Video viewer now defaults to use HLS streaming on Safari desktop. 
* Refactored tooltips to address various bugs. 
* Removed social feature restrictions on Video and eCatalog viewers from mobile devices.

## Bug fixes in Scene7 Viewers 4.9.2 {#section-405e47e202e54943bd843d82415c91cb}

The following bugs are now fixed:

* viewers were displaying at the incorrect size after returning from full-screen and swapping assets. 
* viewers were displaying close button in Full-screen mode. 
* eCatalog viewer were not displaying image maps in portrait mode on mobile devices. 
* eCatalog viewer was displaying pan buttons on mobile phones. 
* eCatalog viewer default tool tips did not apply if the container id is not "ecatalog". 
* eCatalog viewer Tooltips were hidden behind thumbnails in grid view. 
* eCatalog viewer was displaying a page divider for single page. 
* eCatalog viewer image maps failed to function on IE9. 
* Mixed Media viewer was resetting the video scrubber position after resizing the viewer. 
* Mixed Media viewer was using the incorrect art for spin pan buttons. 
* Mixed Media viewer video was showing tooltips under mixed media swatches. 
* HTMl5 Mixed Media viewer spin buttons were displaying on tablet devices. 
* Spin and Zoom viewer tooltips were clipped by edge in embedded viewer. 
* Social Share tooltip position was displaced for the social buttons. 
* Social Share tooltips format were not matching viewer tooltips. 
* Tooltips did not display in full-screen mode on Mac OS with Safari 5. 
* Video viewer incorrect size occurred for progressbar when rotating iPad and switching between screen modes. 
* Video viewer was generating console logs by default.

## Known issues in Scene7 Viewers 4.9.2 {#section-368dd0dc138b44e28b49314e4ad0fa1a}

**All Scene7 viewers**

* Watermarks, obfuscation, and locking are not supported.

**All viewers**

* Parameters with explicit instance names in the code must be overwritten; instance names in a URL must also be overwritten. For example, `zoomView.iconeffect=0`. 
* Image Serving command crop is not supported. 
* Close button only works if the viewer is open in a child window. 
* To customize the tooltip format you add `!IMPORTANT` to the CSS declaration.

**eCatalog viewer**

* JavaScript templates in image maps are not supported. 
* Navigating to another HTML page and then returning occasionally causes the viewer to reset back to the first page. 
* Set `ImageMapEffect` rollover modifier to `1` to invoke infopanels. 

* `Frametransition` set to `none` or `fade` is not supported. 

* Page layout occasionally displays incorrectly after rotating the iOS device. Zoom into page corrects layout.

**Mixed Media viewer**

* Sound track play is not supported at this time.

**Social viewer**

* To render thumbnails properly in outgoing email the `serverurl` modifier should have an absolute URL.

**Video viewer**

* The poster image may encounter "max size" error. The user may need to increase the limit setting for Image Serving Publish. 
* Video captions require a company ruleset if they are hosting an HTML page that is served from an external server that is not a Scene7 server. Contact Adobe technical support for assistance.

**Flash AS3-all viewers**

* Double encode the # character in asset names. 
* Server Support fails to load SWF animations with embedded videos. 
* Server Support fails to load viewer skins if compiled for Flash Player 6. Workaround is to compile for Flash Player 7. 
* Macintosh OS and Flash Player version 10,0,32,18: Workaround depends on a JavaScript bridge instead of a LocalConnection to communicate between Flex and Flash. So, the Flex application must be imbedded in the HTML wrapper. 
* Currently the Flash Viewers support SWFs complied for Flash 7 only. 
* Because of an issue with Java v.1.5.0_06 the server component is not supported with that version of Java. [http://bugs.sun.com/bugdatabase/view_bug.do?bug_id=6274990](http://bugs.sun.com/bugdatabase/view_bug.do?bug_id=6274990). 
* For a skin custom URL parameter, the parameter in the Skin URL must be URL encoded. 
* Image Sets with extended ASCII characters in the name must be URL encoded twice when sent to the viewer or the FVCTX request fails because the Flash player decodes the name before passing it to the viewer code. 
* If the embedding HTML page has significant content after the viewer, it is possible that the viewer may call a JavaScript function before the page is fully loaded. This may abort page loading. A suggested workaround is to use an onLoad event handler to delay initializing the viewer until after the page load is complete. 
* The changes to the `S7Config.setFlashParam()` allow for more than one parameter/value to be passed with this `syntax S7Config.setFlashParam(<viewer ID>, <parameter name>, <parameter value> [, <parameter name>, <parameter value>])`, but in that case the first parameter to be passed must be the "image" parameter followed by the "currentFrame" parameter (if required), and then any other parameters. 

* When using the `skipFrames=frameList` parameter to omit images, the viewer returns an error if an omitted frame is called directly either by the JavaScript change image function, `InitialFrame`, or in the case of a RenderSet that has two or more swatches associated with an image - when the swatch combination referencing the omitted frame is selected. 

* Crop is not supported in conjunction with zoom targets or swatches in either the `image=` or `modifier=` arguments. 

* The `rgn` argument is not supported for the flash viewers for image modifier. 
* A new IE security patch requires the user to activate Flash and other ActiveX applications in IE. Please see the Microsoft site for information about workarounds. 
* Security issues prevent the viewer from reading from a different server on the same domain unless both URLs are fully qualified domain names or the "cross domain policy" is specifically set to allow access from that server. 
* With Flash 7's new security features, if the viewers attempt to read from a different server on the same domain from where the viewers are located (that is, they are redirected by the paths in the `infoServerUrl`, `searchEngineUrl`, or the `serverUrl parameters`) a security alert notifies the user of this fact and asks if you want to allow this, unless the "cross domain policy" is set to allow access from that server.

  For more information on how to set up a "cross domain policy" see the following article: [http://kb2.adobe.com/cps/142/tn_14213.html](http://kb2.adobe.com/cps/142/tn_14213.html). 

* Exception error generated when viewer is embedded in HTTPS page. Issue is due to communication with server logging. For more information: [http://helpx.adobe.com/flash-player/kb/flash-player-issues-secure-sockets.html](http://helpx.adobe.com/flash-player/kb/flash-player-issues-secure-sockets.html)

