---
description: User data. The server returns the contents of this field to the client in response to req=userdata.
solution: Experience Manager
title: UserData
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
TQID: https://experienceleague.adobe.com/8s1LgDcS6610-Ti0s9z0OpFACsQIaoncmynV6yDl1rQ
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
# UserData{#userdata}

User data. The server returns the contents of this field to the client in response to req=userdata.

## Properties {#section-06f2002b77d54a64be07f12fff54ad13}

Text string value. It is recommended to use [property data](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) formatting. If property data formatting is not used, text string must not contain the '=' character.

The zoom, spin, and brochure viewer clients assume this field to use property data formatting. These clients use this field for viewer configuration and customization. See the viewer documentation for details.

This field participates in text string localization. Refer to [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in the *HTTP Protocol Reference* for details.

## Default {#section-7ee879762130467199745f2abc662f1e}

None.

## See also {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
