---
description: JavaScript API reference for eCatalog Viewer.
seo-description: JavaScript API reference for eCatalog Viewer.
seo-title: dispose
solution: Experience Manager
title: dispose
topic: Dynamic media
uuid: b2073d03-a0a0-4f55-a350-7336ddcf031d
---

# dispose{#dispose}

JavaScript API reference for eCatalog Viewer.

 `dispose()`

Disposes this viewer instance by releasing all resources used by the viewer logic and deleting all inner objects and components created by the viewer in runtime.

The web page code should also delete the viewer instance variable as well to completely remove the viewer from the web browser memory.

If the web page code has registered event listeners directly on Viewer SDK components used by the viewer-or stored external references to such components-such listeners must be explicitly unregistered by the web page code, and such external component references must be deleted prior to calling `dispose()`.

Do not access the Viewer API any more after `dispose()` is called.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

None.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

