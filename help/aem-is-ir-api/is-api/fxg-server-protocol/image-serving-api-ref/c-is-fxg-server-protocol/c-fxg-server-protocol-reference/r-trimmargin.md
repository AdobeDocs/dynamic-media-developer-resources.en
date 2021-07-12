---
description: Set trim margin. Sets the trim margin that is set in the PDF file.
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
---
# trimMargin{#trimmargin}

Set trim margin. Sets the trim margin that is set in the PDF file.

 ` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in points

By default the `trimMargin` is set to the full size of document defined by `viewWidth` and `viewHeight`. The *[!DNL left]*, *[!DNL bottom]*, and *[!DNL right]* values are defaulted to the *[!DNL top]* value if not specified.
