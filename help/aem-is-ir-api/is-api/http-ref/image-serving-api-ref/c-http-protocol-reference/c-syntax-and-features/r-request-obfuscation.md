---
description: The contents of the entire modifiers part of request string, including the optional lock suffix may be obscured by applying standard base64 encoding.
seo-description: The contents of the entire modifiers part of request string, including the optional lock suffix may be obscured by applying standard base64 encoding.
seo-title: Request obfuscation
solution: Experience Manager
title: Request obfuscation
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
---

# Request obfuscation{#request-obfuscation}

The contents of the entire modifiers part of request string, including the optional lock suffix may be obscured by applying standard base64 encoding.

 The server attempts to decode if `attribute::RequestObfuscation` is set. If decoding fails, the request is rejected. If both request locking and request obfuscation are applied, the lock suffix must be generated and appended before base64 encoding.

>[!IMPORTANT]
>
>If you enable this feature, be aware that there are certain limitations to its use that include the following:<br>- The Dynamic Media user interface may not show the correct details for the **[!UICONTROL Last Published]** field. However, this affect does not impact publishing.<br>- Currently, HLS video streaming does not work when **[!UICONTROL Request obfuscation]** and **[!UICONTROL Request locking]** are enabled.<br>- Currently, some Dynamic Media Viewers do not work when **[!UICONTROL Request obfuscation]** and **[!UICONTROL Request locking]** are enabled.

## Example {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

encodes to:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Any occurrences of '=', '&', and '%' in value strings must be escaped using '%xx' encoding, before the request is obfuscated. It is not necessary to otherwise http-encode the *modifiers* part of the request either before or after obfuscation, even if request locking is applied, since base64 encoding is safe for http transmission.

## See also {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP Encoding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Request Locking](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd) 
