---
title: System requirements for Dynamic Media HTML5 viewers
description: System requirements for Dynamic Media HTML5 viewers.
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
---
# Dynamic Media HTML5 viewers system requirements{#system-requirements}

System requirements for Dynamic Media HTML5 viewers.

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Server hardware and software {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media Image Serving 6.7.1 or later.
* HTML5 viewers require SDK JavaScript server-side libraries 3.11.5 or later.
* *Email a Friend* social features require s7ondemand 5.0.9 or later.
* eCatalog Viewer - [Info panel popup](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) support requires info server 2.1.8 or later.
* Search feature components require s7search 2.3.0 or later.

## Viewers system requirements {#section-cc72b1e209524d038b4d5b92b35e998e}

**Client browser minimum requirements for component viewers:**

* Supported on the following operating system versions or later:
  * Microsoft® Windows® 7
  * macOS X 10.12
* Supported on the following browser/platform versions or later:
  * Android™ OS 4.x
  * BlackBerry® 10 on native browsers. Only video playback is supported.
  * Chrome 82
  * Edge
  * Firefox 77
  * Internet Explorer 11
  * iOS6
  * iPad 2 (Safari and Chrome browsers only)
  * iPhone 3GS
  * Safari 11
* Internet Explorer on mobile devices is not supported.
* *PanoramicViewer* is supported on the following browser/platform versions or later:
  * Android™ 4.4 (phone devices only)
  * Chrome 82
  * Edge
  * Firefox 77
  * Internet Explorer 11
  * iOS 10
  * Safari 11
* *Video360Viewer* and *DimensionalViewer* is supported on the following browser/platform versions or later:
  * Android™ 5 (phone devices only)
  * Chrome 82
  * Edge
  * Firefox 77
  * iOS 12
  * Safari 12
* *ZoomVerticalViewer* is supported on the following browser/platform versions or later:
  * Android™ 4.x
  * Chrome 82
  * Edge
  * Firefox 77
  * Internet Explorer 11
  * iOS 10
  * Safari 11

**IMPORTANT**
Effective September 30, 2022, Adobe Dynamic Media Viewers will end support for the following:

* TLS (Transport Layer Security) 1.0 and 1.1
* The following weak ciphers in TLS 1.2:
  * `TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384`
  * `TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA`
  * `TLS_RSA_WITH_AES_256_GCM_SHA384`
  * `TLS_RSA_WITH_AES_256_CBC_SHA256`
  * `TLS_RSA_WITH_AES_256_CBC_SHA`
  * `TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256`
  * `TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA`
  * `TLS_RSA_WITH_AES_128_GCM_SHA256`
  * `TLS_RSA_WITH_AES_128_CBC_SHA256`
  * `TLS_RSA_WITH_AES_128_CBC_SHA`
  * `TLS_RSA_WITH_CAMELLIA_256_CBC_SHA`
  * `TLS_RSA_WITH_CAMELLIA_128_CBC_SHA`
  * `TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA`
  * `TLS_RSA_WITH_SDES_EDE_CBC_SHA`

<!-- Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android™ 2.3.7
* Android™ 4.0.4
* Android™ 4.1.1
* Android™ 4.2.2
* Android™ 4.3
* Internet Explorer 7 on Window Vista®
* Internet Explorer 8 on Windows® XP
* Internet Explorer 8-10 on Windows® 7
* Internet Explorer 10 on Windows® Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java™ 6u45
* Java™ 7u25
* OpenSSL 0.9.8y
* Baidu January 2015 -->

<!-- >[!NOTE]
>
>FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->
