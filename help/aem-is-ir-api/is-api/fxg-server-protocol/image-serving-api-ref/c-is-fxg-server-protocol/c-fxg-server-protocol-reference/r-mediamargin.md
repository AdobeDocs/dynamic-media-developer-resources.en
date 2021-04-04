---
description: Set media margin. Sets the media margin that is set in the PDF file.
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
---
# mediaMargin{#mediamargin}

Set media margin. Sets the media margin that is set in the PDF file.

 ` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in points

By default the `mediaMargin` is set to the full size of document defined by `viewWidth` and `viewHeight`. The *[!DNL left]*, *[!DNL bottom]*, and *[!DNL right]* values are defaulted to the *[!DNL top]* value if not specified.
