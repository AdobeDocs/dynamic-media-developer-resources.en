---
title: dispose
description: JavaScript API reference for eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fda6d50f-0e1b-436c-af2e-1ccc9cd51c39
TQID: https://experienceleague.adobe.com/BzeUiVU83InaOmye-Jz9VmHw7vwP1kXT3XTajidpgF8
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

JavaScript API reference for eCatalog Viewer.

 [!DNL `dispose()`]

Disposes this viewer instance by releasing all resources used by the viewer logic and deleting all inner objects and components created by the viewer in runtime.

The web page code should also delete the viewer instance variable as well to completely remove the viewer from the web browser memory.

If the web page code has registered event listeners directly on Viewer SDK components used by the viewer&mdash;or stored external references to such components&mdash;such listeners must be explicitly unregistered by the web page code. And, such external component references must be deleted before calling [!DNL `dispose()`].

Do not access the Viewer API anymore after [!DNL `dispose()`] is called.

## Parameters {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

None.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
