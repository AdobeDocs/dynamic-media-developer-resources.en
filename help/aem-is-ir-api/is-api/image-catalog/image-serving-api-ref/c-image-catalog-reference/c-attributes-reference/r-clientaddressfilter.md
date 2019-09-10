---
description: Client IP address filter. Allows specification of one or more IP addresses or address ranges.
seo-description: Client IP address filter. Allows specification of one or more IP addresses or address ranges.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a557795-0caf-4b5f-974e-fb4c1481a83c
index: y
internal: n
snippet: y
---

# ClientAddressFilter{#clientaddressfilter}

Client IP address filter. Allows specification of one or more IP addresses or address ranges.

When specified, requests to this image catalog that originate from a client at an unlisted IP address will be rejected.

## Properties {#section-d785265988324af68835410c9ba54147}

Comma-separated list of IP addresses with optional netmasks (CIDR notation is used):

` *`ipAddress`*[/ *`netmask`*]&#42;[, *`ipAddress`*[/ *`netmask`*]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>IP address in <span class="varname"> ddd.ddd.ddd.ddd</span> format. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmask</span> </p></td> 
  <td class="stentry"> <p>Net mask (0…32). </p></td> 
 </tr> 
</table>

This attribute is ignored when a preprocessing rule with an `<addressfilter>` element is applied.

## Default {#section-de26e8c9225745e985e4beac1f03f4f6}

Inherited from `default::AddressFilter` if not defined or if empty.

## Examples {#section-a955314d2b6a4213a16c12a8b18d8627}

No access restrictions: `0.0.0.0/0`

Grant access to all addresses starting with 192: `192.0.0.0/8`

Grant access to the 512 hosts with addresses between 192.168.12.0 and 192.168.13.255: `192.168.12.0/23`

Grant access to a single IP address: `192.168.2.117` or `192.168.2.117/32`

## See also {#section-4ea89a7d82e14a4a800487d2d8801465}

[<addressfilter>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1) 
