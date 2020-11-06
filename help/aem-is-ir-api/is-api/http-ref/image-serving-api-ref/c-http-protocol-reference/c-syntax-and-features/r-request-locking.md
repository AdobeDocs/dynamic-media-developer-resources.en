---
description: To reduce opportunity for tampering with requests, a simple locking facility is provided.
seo-description: To reduce opportunity for tampering with requests, a simple locking facility is provided.
seo-title: Request locking
solution: Experience Manager
title: Request locking
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
---

# Request locking{#request-locking}

To reduce opportunity for tampering with requests, a simple locking facility is provided.

 If attribute::RequestLock is set, a lock value must be appended to the request, in form of `&xxxx`, with xxxx being a four digit hex value. This hex value is generated using a simple hashing algorithm applied to the *modifiers* portion of the request (after the '?' which separates the URL path from the *modifiers*). This must be done after the request is fully http-encoded, but before it is (optionally) obfuscated. After de-obfuscating the request, the server will use the same hashing algorithm on the modifier string (excluding the last 5 characters, which contain the lock value). If the generated key does not match the lock, the request is rejected.

 If you enable this feature be aware that there are certain limitations to its use that include the following:

* The Dynamic Media user interface may not show the correct details for the [!UICONTROL Last Published] field. However, this affect does not impact publishing.
* Currently, HLS video streaming does not work when [!UICONTROL Request Obfuscation] and [!UICONTROL Request Locking] are enabled.

C++ sample code to generate the request lock value:

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 

```

## See also {#section-a6d45406c0354669ac581793e4fa8436}

[HTTP Encoding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Request Obfuscation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0) 
