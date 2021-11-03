---
description: The Smart Crop Video Viewer supports Adobe Analytics tracking out-of-the-box.


solution: Experience Manager
title: Support for Adobe Analytics tracking

feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 2cc7087d-ed02-4560-b9ce-533af2b11a24
---
# Support for Adobe Analytics tracking{#support-for-adobe-analytics-tracking}

The Smart Crop Video Viewer supports Adobe Analytics tracking out-of-the-box.

## Out-of-the-box tracking {#section-3b101fe30be943c1b679fd5c273569ca}

The Smart Crop Video Viewer supports Adobe Analytics tracking out-of-the-box.

To enable tracking, pass the proper company preset name as `config2` parameter.

The viewer also sends a single tracking HTTP request to the configured Image Server with the viewer type and version information.

## Custom tracking {#section-ab10bd7caf184721a366cf3953071934}

To integrate with third-party analytics systems it is necessary to listen to `trackEvent` viewer callback and process `eventInfo` argument of the callback function as necessary. The following code is an example of such handler function:

```
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
   <td colname="col2"> <p>an asset is swapped in the viewer using <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>playback is started. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>playback is paused. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>playback is stopped. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>playback reaches one of the following millstones: 0%, 25%, 50%, 75%, and 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>
