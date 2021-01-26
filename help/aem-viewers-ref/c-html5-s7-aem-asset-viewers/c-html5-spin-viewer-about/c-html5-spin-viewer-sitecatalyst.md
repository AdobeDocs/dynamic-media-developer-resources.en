---
description: The Spin Viewer supports Adobe Analytics tracking out of the box.
seo-description: The Spin Viewer supports Adobe Analytics tracking out of the box.
seo-title: Support for Adobe Analytics tracking
solution: Experience Manager
title: Support for Adobe Analytics tracking
topic: Dynamic Media
uuid: 337671f0-22e8-4e3e-a0a9-ce49d271ea56
---

# Support for Adobe Analytics tracking{#support-for-adobe-analytics-tracking}

The Spin Viewer supports Adobe Analytics tracking out of the box.

## Out-of-the-box tracking {#section-d06145cfa2b9491bb485b599368d466e}

The Spin Viewer supports Adobe Analytics tracking out-of-the-box.

To enable tracking, pass the proper company preset name as `config2` parameter.

The viewer also sends a single tracking HTTP request to the configured Image Server with the viewer type and version information.

## Custom tracking {#section-47512156a1d64b338b50cfa39c84f4aa}

To integrate with third-party analytics systems, it is necessary to listen to the `trackEvent` viewer callback and process the `eventInfo` argument of the callback function, as necessary. The following code is an example of such handler function:

```
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

The viewer tracks the following SDK user events:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK user event </p> </th> 
   <th colname="col2" class="entry"> <p>Sent when... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>viewer is loaded first. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>an asset is swapped in the viewer using the <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> an image is zoomed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>an image is panned. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPIN </span> </p> </td> 
   <td colname="col2"> <p> a spin is performed. </p> </td> 
  </tr> 
 </tbody> 
</table>

