---
title: SynthesizeFontStyles
description: Enable synthesized font variations. Controls whether the server should generate an error response or synthesize a bold, italic, or bold/italic font style if such a style is requested but cannot be found in the font map.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08f20748-71c7-4b9f-9b45-70352f9abf35
TQID: https://experienceleague.adobe.com/f0qZL-eepq1KmPksbOoXU0WHnH1Gk9omAvrpJXHwBaw
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
# SynthesizeFontStyles{#synthesizefontstyles}

Enable synthesized font variations. Controls whether the server should generate an error response or synthesize a bold, italic, or bold/italic font style if such a style is requested but cannot be found in the font map.

>[!NOTE]
>
>Synthesizing font styles often result in lower-quality renderings than using actual fonts for such styles.

## Properties {#section-3205560a74774ebf9c916b07bd15aca6}

Flag. Set to 0 to disable and to 1 to enable synthetic font styles.

## Default {#section-71f94aa65e404d14b441674c040b59e3}

Inherited from `default::SynthesizeFontStyles` if not defined or if empty.

## See also {#section-47a79659cc844272b6d5f36c946e12ac}

[Font Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
