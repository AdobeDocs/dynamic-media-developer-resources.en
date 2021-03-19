---
description: Flash application web domains. Adobe Flash applications may require access to the properties of images delivered with fmt=swf or fmt=swf3.
seo-description: Flash application web domains. Adobe Flash applications may require access to the properties of images delivered with fmt=swf or fmt=swf3.
seo-title: TrustedDomains
solution: Experience Manager
title: TrustedDomains
uuid: 1d056d68-b699-413c-897c-8612444735c5
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
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
