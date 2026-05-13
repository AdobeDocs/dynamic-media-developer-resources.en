---
description: Set media margin. Sets the media margin that is set in the PDF file.
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
TQID: 'https://experienceleague.adobe.com/xbnVRTqP7h5vs3Cdlur8ge1nPz7rjGzpChCFDwue6U0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# mediaMargin{#mediamargin}

Set media margin. Sets the media margin that is set in the PDF file.

 ` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in points

By default the `mediaMargin` is set to the full size of document defined by `viewWidth` and `viewHeight`. The *[!DNL left]*, *[!DNL bottom]*, and *[!DNL right]* values are defaulted to the *[!DNL top]* value if not specified.
