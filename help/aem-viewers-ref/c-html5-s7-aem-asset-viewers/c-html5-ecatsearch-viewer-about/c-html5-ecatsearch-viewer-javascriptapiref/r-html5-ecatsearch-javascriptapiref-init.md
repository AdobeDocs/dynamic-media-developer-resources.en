---
description: JavaScript API reference for eCatalog Viewer.
seo-description: JavaScript API reference for eCatalog Viewer.
seo-title: init
solution: Experience Manager
title: init
uuid: b01f1497-8bee-4e01-8f92-272b324cb2dd
feature: "Dynamic Media Classic,Viewers,SDK/API,eCatalog Search"
role: "Developer,Business Practitioner"
---

# init{#init}

JavaScript API reference for eCatalog Viewer.

 [!DNL `init()`]

Starts the initialization of the eCatalog Viewer. By this time container DOM element must be created so that the viewer code can find it by its ID.

If the container element is not a part of the web page layout just yet (for example, it may be hidden using [!DNL `display:none`] style assigned to it), the viewer suspends its initialization process until the moment when the web page brings the container element back to the layout. When this happens, the viewer load automatically resumes.

Only call this method once during the viewer life cycle; subsequent calls are ignored.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

None.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] A reference to viewer instance.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

