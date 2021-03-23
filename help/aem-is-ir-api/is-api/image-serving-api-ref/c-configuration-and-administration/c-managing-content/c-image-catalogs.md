---
description: Image catalogs provide many server configuration settings, as well as fonts, ICC profiles, command macros.
solution: Experience Manager
title: Image catalogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Image catalogs{#image-catalogs}

Image catalogs provide many server configuration settings, as well as fonts, ICC profiles, command macros.

They map image and static content ids used in requests to actual file paths, store various image metadata, such as image maps, and provide containers for templates and image sets.

Image catalogs are accessed only by the Platform Server, never by the Image Server. Catalog attribute files must have an .ini suffix and be placed in the Platform Server's catalog folder ( `PS::CatalogFolder`). At least the default image catalog is required and must be populated with all attributes for correct functioning of the Platform Server. 
