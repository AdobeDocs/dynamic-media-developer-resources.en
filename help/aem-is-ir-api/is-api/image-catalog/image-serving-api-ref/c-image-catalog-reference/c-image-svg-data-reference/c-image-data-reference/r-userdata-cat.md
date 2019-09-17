---
description: User data. The server returns the contents of this field to the client in response to req=userdata.
seo-description: User data. The server returns the contents of this field to the client in response to req=userdata.
seo-title: UserData
solution: Experience Manager
title: UserData
topic: Scene7 Image Serving - Image Rendering API
uuid: cadc9f3c-c0ca-4c88-bc8a-97c28b439b01
---

# UserData{#userdata}

User data. The server returns the contents of this field to the client in response to req=userdata.

## Properties {#section-06f2002b77d54a64be07f12fff54ad13}

Text string value. It is recommended to use [property data](r_property_data.md#reference_835FF0D97B9C4C24A6E6E74BAE4EDE59) formatting. If property data formatting is not used, text string must not contain the '=' character.

The zoom, spin, and brochure viewer clients assume this field to use property data formatting. These clients use this field for viewer configuration and customization. See the viewer documentation for details.

This field participates in text string localization. Refer to [Text String Localization](r_text_string_localization.md#reference_CAE5F6CEA4764762852ACAAB3B7B3527) in the *HTTP Protocol Reference* for details.

## Default {#section-7ee879762130467199745f2abc662f1e}

None.

## See also {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](r_req.md#reference_907CDB4A97034DB7AD94695F25552E76) , [Text String Localization](r_text_string_localization.md#reference_CAE5F6CEA4764762852ACAAB3B7B3527) 
