---
description: Surface glossiness Specifies the relative glossiness of the material surface.


solution: Experience Manager
title: Gloss

feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Gloss{#gloss}

Surface glossiness Specifies the relative glossiness of the material surface.

This value is used by the renderer for the following purposes:

* Select the illumination map when `catalog::Illum` is -1. 
* Controls gloss effect (specular reflection) rendering in conjunction with `catalog::Type`. 
* Controls 3D reflection render effects in conjunction with `catalog::Type` and `catalog::Roughness`.

## Properties {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Integer number. Percentage number in the range 0…100. Optional for all materials. Used only for vignettes with multiple reflection maps or vignettes with 3D reflection capability. Leave empty or set to -1 if not known or not needed.

## Default {#section-2352721073524f1a8d461f64a363aac9}

A default value is provided by the vignette if this value is set to -1.

## See also {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalog::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161) 
