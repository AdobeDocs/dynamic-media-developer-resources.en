---
description: Flash application web domains. Adobe Flash applications may require access to the properties of images delivered with fmt=swf or fmt=swf3.
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
TQID: 'https://experienceleague.adobe.com/xGn-usdBOB3NjRaffq6w0SJDlDerpeQJHGhKej-L3Cw'
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
# TrustedDomains{#trusteddomains}

Flash application web domains. Adobe Flash applications may require access to the properties of images delivered with fmt=swf or fmt=swf3.

The swf must grant access explicitly by registering the name of application domains it trusts.

## Properties {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

String containing a comma-separated list of web domain names. If empty, applications must be served from the same domain as Image Rendering to be able to access the properties of images in swf-formatted responses.

## Default {#section-5c52ed3c7310488380f5a6f9540bf981}

Inherited from `default::TrustedDomains` if not present.

## See also {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
