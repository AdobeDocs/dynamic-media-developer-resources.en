---
title: init
description: JavaScript API reference for Panoramic Viewer.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
autotag-review: '2026-05-13T22:09:33.410Z'
TQID: 'https://experienceleague.adobe.com/rpwcZhdc6cNM27k-LER-Bd8giGQkDzQTxJp0ejCDA8s'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
    internal-label: Dynamic Media Classic
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
---
# init{#init}

JavaScript API reference for Panoramic Viewer.

 `init()`

Starts the initialization of the Panoramic Viewer. By this time the container DOM element must be created so that the viewer code can find it by its ID.

If the container element is not a part of the web page layout yet (for example, it may be hidden using `display:none` style assigned to it), the viewer suspends its initialization process. It does so until the moment when the web page brings the container element back to the layout. When this event happens, the viewer load automatically resumes.

This method should be called only once during viewer life cycle, subsequent calls are ignored.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

None.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` A reference to the viewer instance.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
