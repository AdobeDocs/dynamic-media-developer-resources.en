---
description: The default catalog provides default values for all catalog attributes for all image catalogs.
solution: Experience Manager
title: Default catalog
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
TQID: 'https://experienceleague.adobe.com/qbfEwBJ-eQmCbBR0MJQhP7x3ZEd30nfLJHWjBVoXIjc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Default catalog{#default-catalog}

The default catalog provides default values for all catalog attributes for all image catalogs.

If a particular attribute cannot be found in a specific image catalog, the server uses the corresponding value from the default catalog instead. Similarly, the default catalog can be used to provide defaults for specific catalog data records (images, macro definitions, fonts, and ICC profiles). If a particular data record cannot be found in a specific image catalog, the server attempts to find it in the default catalog instead. This allows image catalogs to be sparsely populated and simplifies management of global attributes and data, such as shared templates, macros, fonts, and so on.

In addition, the default catalog provides all attributes and data records (macros, fonts, ICC profiles, request pre-processing rules) when no specific image catalog is involved in an operation.

For correct functioning of the [!DNL Platform Server] the catalog attributes file for the default catalog must be named [!DNL default.ini], must always exist in the catalog folder, and must be fully populated with all required attributes, excluding `attribute::RootId` and the references to the various catalog data files, which are all optional.

>[!NOTE]
>
>All catalog attribute files except [!DNL default.ini] must contain a unique `attribute::RootId` value. `attribute::RootId` in [!DNL default.ini] must be empty.
