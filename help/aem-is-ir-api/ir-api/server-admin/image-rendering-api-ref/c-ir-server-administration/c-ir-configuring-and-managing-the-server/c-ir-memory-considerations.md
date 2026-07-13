---
description: The amount of memory used by Image Rendering can vary widely and depends highly on actual server load and usage (for example, few vs. many different vignettes, size and complexity of vignettes, and so on).
solution: Experience Manager
title: Memory considerations
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
TQID: 'https://experienceleague.adobe.com/l41dx4mMn82TvImVVCJJKgJZbP-mWT5KbnzfZ5xFJqg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Memory considerations{#memory-considerations}

The amount of memory used by Image Rendering can vary widely and depends highly on actual server load and usage (for example, few vs. many different vignettes, size and complexity of vignettes, and so on).

For best performance, memory paging (swapping) should be avoided.

Image Rendering shares the memory management of Image Server. When using Image Rendering, additional memory should be allocated. 30 to 50% of physical memory may be reasonable.

Refer to the Image Serving documentation for information on how to change the Image Server memory allocation (ImageServer::PhysicalMemory).

