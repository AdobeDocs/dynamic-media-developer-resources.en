---
description: The default catalog provides default values for all catalog attributes for all image catalogs.
solution: Experience Manager
title: Default catalog
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
---
# Default catalog{#default-catalog}

The default catalog provides default values for all catalog attributes for all image catalogs.

If a particular attribute cannot be found in a specific image catalog, the server uses the corresponding value from the default catalog instead. Similarly, the default catalog can be used to provide defaults for specific catalog data records (images, macro definitions, fonts, and ICC profiles). If a particular data record cannot be found in a specific image catalog, the server attempts to find it in the default catalog instead. This allows image catalogs to be sparsely populated and simplifies management of global attributes and data, such as shared templates, macros, fonts, etc.

In addition, the default catalog provides all attributes and data records (macros, fonts, ICC profiles, request pre-processing rules) when no specific image catalog is involved in an operation.

For correct functioning of the [!DNL Platform Server] the catalog attributes file for the default catalog must be named [!DNL default.ini], must always exist in the catalog folder, and must be fully populated with all required attributes, excluding `attribute::RootId` and the references to the various catalog data files, which are all optional.

>[!NOTE]
>
>All catalog attribute files except [!DNL default.ini] must contain a unique `attribute::RootId` value. `attribute::RootId` in [!DNL default.ini] must be empty.
