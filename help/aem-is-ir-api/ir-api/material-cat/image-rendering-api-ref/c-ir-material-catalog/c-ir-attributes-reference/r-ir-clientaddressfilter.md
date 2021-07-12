---
description: Client IP address filter. Allows specification of one or more IP addresses or address ranges.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
---
# ClientAddressFilter{#clientaddressfilter}

Client IP address filter. Allows specification of one or more IP addresses or address ranges.

When specified, requests to this image catalog that originate from a client at an unlisted IP address will be rejected. `localhost` is always implicitly part of the `ClientAddressFilter` definition, even if not explicitly specified. Requests originating from `localhost` are never rejected, regardless of the `ClientAddressFilter` specification.

## Properties {#section-21a2992f108d42fb8660c0d65aa61e13}

Comma-separated list of IP addresses with optional netmasks ([CIDR notation](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) is used):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* IP address in *[!DNL ddd.ddd.ddd.ddd]* format 

* *[!DNL netmask]* net mask (0…32)

This attribute is ignored when a pre-processing rule with an `<addressfilter>` element is applied.

## Default {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Inherited from `default::AddressFilter` if not defined or if empty.

## Examples {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* No access restrictions: `0.0.0.0/0` 
* Grant access to all addresses starting with `192: 192.0.0.0/8` 
* Grant access to the 512 hosts with addresses between `192.168.12.0` and `192.168.13.255: 192.168.12.0/23` 

* Grant access to a single IP address: `192.168.2.117` or `192.168.2.117/32`

## See also {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
