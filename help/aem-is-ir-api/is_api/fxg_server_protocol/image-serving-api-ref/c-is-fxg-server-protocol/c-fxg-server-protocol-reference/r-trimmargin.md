---
description: Set trim margin. Sets the trim margin that is set in the PDF file.
seo-description: Set trim margin. Sets the trim margin that is set in the PDF file.
seo-title: trimMargin
solution: Experience Manager
title: trimMargin
topic: Scene7 Image Serving - Image Rendering API
uuid: ff1220e4-9841-4a1a-a3bc-1da11f87ad8c
index: y
internal: n
snippet: y
---

# trimMargin{#trimmargin}

Set trim margin. Sets the trim margin that is set in the PDF file.

 ` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in points

By default the `trimMargin` is set to the full size of document defined by `viewWidth` and `viewHeight`. The *[!DNL left]*, *[!DNL bottom]*, and *[!DNL right]* values are defaulted to the *[!DNL top]* value if not specified. 
