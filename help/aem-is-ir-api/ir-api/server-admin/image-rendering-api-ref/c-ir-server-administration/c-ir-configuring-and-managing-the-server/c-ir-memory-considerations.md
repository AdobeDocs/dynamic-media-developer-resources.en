---
description: The amount of memory used by Image Rendering can vary widely and depends highly on actual server load and usage (for example, few vs. many different vignettes, size and complexity of vignettes, and so on).
seo-description: The amount of memory used by Image Rendering can vary widely and depends highly on actual server load and usage (for example, few vs. many different vignettes, size and complexity of vignettes, and so on).
seo-title: Memory considerations
solution: Experience Manager
title: Memory considerations
uuid: 21247081-ff27-4237-93da-5fc996417dfd
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Memory considerations{#memory-considerations}

The amount of memory used by Image Rendering can vary widely and depends highly on actual server load and usage (for example, few vs. many different vignettes, size and complexity of vignettes, and so on).

For best performance, memory paging (swapping) should be avoided.

Image Rendering shares the memory management of Image Server. When using Image Rendering, additional memory should be allocated. 30 to 50% of physical memory may be reasonable.

Refer to the Image Serving documentation for information on how to change the Image Server memory allocation (ImageServer::PhysicalMemory). 
