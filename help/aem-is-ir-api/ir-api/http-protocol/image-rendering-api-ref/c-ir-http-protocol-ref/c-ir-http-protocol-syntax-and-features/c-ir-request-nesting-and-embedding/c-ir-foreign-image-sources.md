---
description: Image Serving supports access to source images on foreign HTTP and FTP servers.
seo-description: Image Serving supports access to source images on foreign HTTP and FTP servers.
seo-title: Foreign image sources
solution: Experience Manager
title: Foreign image sources
uuid: 28a17400-4807-4e14-937a-80309be53d55
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# Foreign image sources{#foreign-image-sources}

Image Serving supports access to source images on foreign HTTP and FTP servers.

To specify a foreign URL for a `src=` or a `mask=` command; simply delimit the entire embedded URL with curly braces:

` …&src={ *[!DNL foreignUrl]*}&…`

Full absolute URLs (if `attribute::AllowDirectUrls` is set) and URLs relative to `attribute::RootUrl` are permitted. An error occurs if an absolute URL is embedded and attribute:: `AllowDirectUrls` is 0, or if a relative URL is specified and `attribute::RootUrl` is empty.

Foreign images are cached by the server according to the caching headers included with the HTTP response. 
