---
title: init
description: JavaScript API reference for Carousel Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 00e09e26-1380-487c-9512-34d805f1330d
---
# init{#init}

JavaScript API reference for Carousel Viewer.

 `init()`

Starts the initialization of the Carousel Viewer. By this time the container DOM element must be created so that the viewer code can find it by its ID.

If the container element is not a part of the web page layout yet &ndash; for example, it may be hidden using `display:none` style &ndash; the viewer suspends its initialization process. It is suspended until the moment when the web page brings the container element back to the layout, at which point the viewer load automatically resumes.

Call this method only once during viewer life cycle; subsequent calls are ignored.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

None.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` A reference to the viewer instance.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
