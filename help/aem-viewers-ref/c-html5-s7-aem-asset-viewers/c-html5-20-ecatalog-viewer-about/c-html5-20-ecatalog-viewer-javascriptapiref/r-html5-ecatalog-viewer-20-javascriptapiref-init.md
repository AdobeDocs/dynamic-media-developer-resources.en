---
title: init
description: JavaScript API reference for eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e7775a65-67bf-4ad6-8e51-1fdf141946bc
---
# init{#init}

JavaScript API reference for eCatalog Viewer.

 `init()`

Starts the initialization of the eCatalog Viewer. By this time container DOM element must be created so that the viewer code can find it by its ID.

If the container element is not a part of the web page layout yet &ndash; for example, it may be hidden using `display:none` style assigned to it &ndash; the viewer suspends its initialization process. It does so until the moment when the web page brings the container element back to the layout. When this action happens, the viewer load automatically resumes.

Only call this method once during the viewer life cycle; subsequent calls are ignored.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

None.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` A reference to viewer instance.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```
