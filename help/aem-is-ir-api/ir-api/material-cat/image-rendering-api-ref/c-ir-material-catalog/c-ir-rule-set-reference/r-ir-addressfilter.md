---
description: Address filter element. Optional in <rule> elements. Overrides attribute ClientAddressFilter when the rule is applied.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
---
# addressfilter{#addressfilter}

Address filter element. Optional in `<rule>` elements. Overrides attribute::ClientAddressFilter when the rule is applied.

## Attributes {#section-e7a0960f7f0045da91de37824aa4aeaa}

None.

## Data {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Comma-separated list of IP addresses. Each individual address may include an optional netmask suffix to allow specification of IP address ranges. See ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` for details.

## Description {#section-099b7839c4be40c68cbff29dad14e7d5}

Access to this image catalog can be restricted to one or more specific IP addresses by specifying them in an `<addressfilter>` element. A "request refused" error is returned to the client if the client IP address is not matched.

Access is not restricted if `<addressfilter>` is empty or not specified.

If the `<expression>` in the `<rule>` element is absent or empty, the `<addressfilter>` is applied to all requests.

`localhost` is always implicitly part of the `ClientAddressFilter` definition, even if not explicitly specified. Requests originating from `localhost` are never rejected, regardless of the `ClientAddressFilter` specification.

## SeeaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
