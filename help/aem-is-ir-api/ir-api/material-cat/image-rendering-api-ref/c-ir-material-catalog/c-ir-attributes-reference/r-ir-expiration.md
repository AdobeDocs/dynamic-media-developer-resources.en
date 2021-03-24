---
description: Default client cache time to live. Provides a default expiration interval in case a particular catalog record does not contain a valid catalog Expiration or vignette Expiration value, or if a vignette file or material file is accessed directly, rather than via a catalog record.
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Expiration{#expiration}

Default client cache time to live. Provides a default expiration interval in case a particular catalog record does not contain a valid catalog::Expiration or vignette::Expiration value, or if a vignette file or material file is accessed directly, rather than via a catalog record.

## Properties {#section-8e2bade105ec4905ae5c4911f500279f}

Real number, 0 or greater. Number of hours until expiration since the reply data was generated. Set to 0 to always expire the reply image immediately, which effectively disables client caching. Set to -1 to mark as *never expire*.

## Default {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Inherited from default::Expiration if not defined or if empty.

## See also {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c) 
