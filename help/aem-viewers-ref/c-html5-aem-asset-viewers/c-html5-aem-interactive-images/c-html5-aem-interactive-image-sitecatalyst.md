---
description: Support for analytics tracking
solution: Experience Manager
title: Support for analytics tracking
uuid: ae870d2e-2a09-4551-935a-916d0e657653
feature: "Dynamic Media Classic,Viewers,SDK/API,Interactive Images"
role: "Developer,Business Practitioner,Data Engineer,Data Architect"
---

# Support for analytics tracking{#support-for-analytics-tracking}

## Custom tracking {#section-cda48fc9730142d0bb3326bac7df3271}

By default, the viewer sends a single tracking HTTP request to configured Image Server with the viewer type and version information.

To integrate with third-party analytics systems, it is necessary to listen to the `trackEvent` viewer callback and process the `eventInfo` argument of the callback function as necessary. The following code is an example of such handler function:

```
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
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
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>user activates hotspot. </p> </td> 
  </tr> 
 </tbody> 
</table>

