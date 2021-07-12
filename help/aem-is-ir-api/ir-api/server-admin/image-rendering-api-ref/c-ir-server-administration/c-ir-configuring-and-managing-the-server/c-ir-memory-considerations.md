---
description: The amount of memory used by Image Rendering can vary widely and depends highly on actual server load and usage (for example, few vs. many different vignettes, size and complexity of vignettes, and so on).
solution: Experience Manager
title: Memory considerations
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
---
# Memory considerations{#memory-considerations}

The amount of memory used by Image Rendering can vary widely and depends highly on actual server load and usage (for example, few vs. many different vignettes, size and complexity of vignettes, and so on).

For best performance, memory paging (swapping) should be avoided.

Image Rendering shares the memory management of Image Server. When using Image Rendering, additional memory should be allocated. 30 to 50% of physical memory may be reasonable.

Refer to the Image Serving documentation for information on how to change the Image Server memory allocation (ImageServer::PhysicalMemory).
