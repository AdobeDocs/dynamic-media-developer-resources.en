---
title: Installing multiple Dynamic Media viewers on the same server
description: Instructions for installing the Dynamic Media Viewers API.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
---
# Installing multiple viewers on the same server{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instructions for installing the Dynamic Media viewers API.

Install and test Image Serving before you install the Image Serving viewers.

Copy the IS Viewers files to your hard drive and then deploy the `s7viewers.war` file into the `../ImageServing/webapps` directory. See your Image Serving documentation for instructions on how to deploy, start, stop, and manage the Image Server.

>[!NOTE]
>
>There is no upgrade install for the Image Serving viewers. Adobe recommends that you back up any existing Dynamic Media viewers (s7viewers) directory before you continue with the install.

**To install multiple viewers on the same server:**

1. Rename the viewer .war to the desired context and deploy file to the location you want.
1. Set `this.isViewerRoot` parameter in `config.js`.
1. Open `config.js` at the root of the newly created viewer folder.
1. Set parameter `this.isViewerRoot = "/s7viewers"` to the context of the `s7viewers.war` file. For example, `"/s7viewers-4.0"`.
1. Save the file and close.
