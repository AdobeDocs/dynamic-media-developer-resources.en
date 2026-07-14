---
title: init
description: JavaScript API reference for eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
TQID: 'https://experienceleague.adobe.com/Hb-C6aORHF8--oX3IqgRZIi1rfbLg39F0Ewzb4sg45U'
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
# init{#init}

JavaScript API reference for eCatalog Viewer.

 [!DNL `init()`]

Starts the initialization of the eCatalog Viewer. By this time, the container DOM element must be created so that the viewer code can find it by its ID.

If the container element is not a part of the web page layout yet&mdash;for example, it may be hidden using [!DNL `display:none`] style assigned to it&mdash;the viewer suspends its initialization process. It does so until the moment when the web page brings the container element back to the layout. When this event happens, the viewer load automatically resumes.

Only call this method once during the viewer life cycle; subsequent calls are ignored.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

None.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] A reference to viewer instance.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

