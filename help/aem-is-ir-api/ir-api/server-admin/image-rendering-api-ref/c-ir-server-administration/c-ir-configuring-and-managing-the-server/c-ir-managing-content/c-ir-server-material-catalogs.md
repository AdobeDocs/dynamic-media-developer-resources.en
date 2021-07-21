---
description: Material catalogs provide many Image Rendering configuration settings.
solution: Experience Manager
title: Material catalogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
---
# Material catalogs{#material-catalogs}

Material catalogs provide many Image Rendering configuration settings.

 Material catalogs map vignette and material ids used in requests to actual file paths, can store all metadata associated with materials, and provide containers for templates. They keep track of ICC profiles and command macros.

Material catalogs are accessed only by the Java component of Image Rendering (co-located with the Platform Server). Catalog attribute files must have a [!DNL .ini] suffix and be placed in the registered catalog folder ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). The default material catalog ( [!DNL default.ini]) must always be present and must be populated with all attributes for correct functioning of Image Serving.
