---
description: JavaScript API reference for Interactive Video Viewer.
seo-description: JavaScript API reference for Interactive Video Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic Media
uuid: e6ec0730-1ddc-4026-939c-2c9f8ecee5c7
---

# init{#init}

JavaScript API reference for Interactive Video Viewer.

 `init()`

Starts the initialization of the Interactive Video Viewer. By this time the container DOM element must be created so that the viewer code can find it by its ID.

If the container element is not a part of the web page layout just yet (for example, it may be hidden using `display:none` style assigned to it), the viewer suspends its initialization process until the moment when the web page brings the container element back to the layout. When this happens, the viewer load automatically resumes.

Call this method only once during viewer life cycle; subsequent calls are ignored.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

None.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` A reference to the viewer instance.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

