---
description: Set media margin. Sets the media margin that is set in the PDF file.
seo-description: Set media margin. Sets the media margin that is set in the PDF file.
seo-title: mediaMargin
solution: Experience Manager
title: mediaMargin
topic: Scene7 Image Serving - Image Rendering API
uuid: f813daac-ba18-4f73-9b48-eb2dd3285990
index: y
internal: n
snippet: y
---

# mediaMargin{#mediamargin}

Set media margin. Sets the media margin that is set in the PDF file.

 ` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in points

By default the `mediaMargin` is set to the full size of document defined by `viewWidth` and `viewHeight`. The *[!DNL left]*, *[!DNL bottom]*, and *[!DNL right]* values are defaulted to the *[!DNL top]* value if not specified. 
