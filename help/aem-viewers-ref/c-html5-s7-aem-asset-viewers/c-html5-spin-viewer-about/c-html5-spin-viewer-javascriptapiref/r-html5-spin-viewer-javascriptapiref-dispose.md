---
title: dispose
description: JavaScript API reference for Spin Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: c19466a8-9fc5-440c-8bb1-c4528937a522
TQID: https://experienceleague.adobe.com/zKNl49C-Ak-6ET2NUNwsXUfv1cEY6cVnrivr3--Dqtw
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# dispose{#dispose}

JavaScript API reference for Spin Viewer.

 `dispose()`

Disposes this viewer instance by releasing all resources used by the viewer logic and deleting all inner objects and components created by the viewer in runtime.

The web page code should also delete the viewer instance variable as well to completely remove the viewer from the web browser memory.

If the web page code has registered event listeners directly on Viewer SDK components used by the viewer &ndash; or stored external references to such components &ndash; such listeners must be explicitly unregistered by the web page code. And, such external component references must be deleted before calling `dispose()`.

Do not access the Viewer API anymore after `dispose()` is called.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

None.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
