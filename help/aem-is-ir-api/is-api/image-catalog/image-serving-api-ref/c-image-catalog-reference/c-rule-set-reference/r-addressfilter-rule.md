---
description: Address filter element. Optional in <rule> and <pathrule> elements.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
TQID: https://experienceleague.adobe.com/l8bzsLv-bQ3rgQEGjpoBZzON9l9XuMO2eBKJnRPT41E
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
# addressfilter{#addressfilter}

Address filter element. Optional in `<rule>` and `<pathrule>` elements.

Overrides `attribute::ClientAddressFilter` when the rule is applied.

## Attributes {#section-31e9ad29e9934933ac154bccbc729172}

None.

## Data {#section-c762bdfe425140d689ea5abf25e9a48a}

Comma-separated list of IP addresses. Each individual address may include an optional netmask suffix to allow specification of IP address ranges. See `attribute::ClientAddressFilter` for details.

## Description {#section-d561b2485e004ef8a2085997d0f4bca6}

Access to this image catalog can be restricted to one or more specific client IP addresses by specifying them in an `<addressfilter>` element. A "request refused" error is returned to the client if the client IP address is not matched.

Access is not restricted if `<addressfilter>` is empty or not specified.

If the `<expression>` in the `<rule>` element is absent or empty, the `<addressfilter>` is applied to all requests.

## See also {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
