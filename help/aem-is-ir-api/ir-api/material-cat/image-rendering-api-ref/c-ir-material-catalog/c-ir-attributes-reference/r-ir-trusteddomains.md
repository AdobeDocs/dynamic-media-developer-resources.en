---
description: Flash application web domains. Adobe Flash applications may require access to the properties of images delivered in swf format. The swf must grant access explicitly by registering the name of application domain(s) it trusts.
solution: Experience Manager
title: TrustedDomains *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
---
# TrustedDomains *{#trusteddomains}

Flash application web domains. Adobe Flash applications may require access to the properties of images delivered in swf format. The swf must grant access explicitly by registering the name of application domain(s) it trusts.

## Properties {#section-5d6ecfa431a04abd8628a28e0ab3be83}

String containing a comma-separated list of web domain names. If empty, applications must be served from the same domain as Image Rendering to be able to access the properties of images in [!DNL swf]-formatted responses.

## Default {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Inherited from `default::TrustedDomains` if not present.

## See also {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
