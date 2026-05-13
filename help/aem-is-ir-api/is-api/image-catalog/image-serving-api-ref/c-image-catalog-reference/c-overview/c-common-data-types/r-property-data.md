---
description: Property data consists of a text string representing one or more properties.
solution: Experience Manager
title: Property data
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
TQID: 'https://experienceleague.adobe.com/jE8U1fgDsG9wdzG4O-BsPHvPOGLXDxZRMdZvL9LuYZE'
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
# Property data{#property-data}

Property data consists of a text string representing one or more properties.

A property consists of a property name and a property value, separated by =.

Multiple properties are separated by line separators, which may be either `??` or `<CR><LF>`. If the entire property data string is not enclosed in quotation marks, the server replaces each occurrence of `??` with `<CR><LF>` before transmitting the data to the client. Property names may consist of letters, numbers, '.', '-', and '_'. Property names are not case-sensitive.

Property values must not include line separators.

See [Text String](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) for additional rules applied to Property Data.
