---
title: Foreign image sources
description: Image Serving supports access to source images on foreign HTTP and FTP servers.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
TQID: 'https://experienceleague.adobe.com/doS6fbVfaXGtLVNBAmOkB-TquNmOc5B2B--IewouFDY'
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
# Foreign image sources{#foreign-image-sources}

Image Serving supports access to source images on foreign HTTP and FTP servers.

To specify a foreign URL for a `src=` or a `mask=` command; simply delimit the entire embedded URL with curly braces:

` …&src={ *[!DNL foreignUrl]*}&…`

Full absolute URLs (if `attribute::AllowDirectUrls` is set) and URLs relative to `attribute::RootUrl` are permitted. An error occurs if an absolute URL is embedded and attribute:: `AllowDirectUrls` is 0, or if a relative URL is specified and `attribute::RootUrl` is empty.

Foreign images are cached by the server according to the caching headers included with the HTTP response.
