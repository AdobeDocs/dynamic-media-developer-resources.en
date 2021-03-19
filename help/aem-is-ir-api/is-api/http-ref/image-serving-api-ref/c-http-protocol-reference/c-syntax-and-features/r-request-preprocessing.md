---
description: Image Serving provides a simple request preprocessor based on regular-expression match and substitution rules.
seo-description: Image Serving provides a simple request preprocessor based on regular-expression match and substitution rules.
seo-title: Request preprocessing
solution: Experience Manager
title: Request preprocessing
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# Request preprocessing{#request-preprocessing}

Image Serving provides a simple request preprocessor based on regular-expression match and substitution rules.

Collections of rules (rule sets) can be attached to each image catalog, including the default catalog. Rules are specified with XML-formatted files.

Request preprocessing rules can modify the path and query portions of requests before they are processed by the Platform Server's parser, including manipulating the path, adding commands, changing command values, and applying templates or macros. Rules can also be used to configure and override certain security features which are normally controlled only with catalog attributes, such as request obfuscation, water-marking, as well as limiting HTTP service to specific client IP addresses.

Request preprocessing rules are suitable for a variety of applications, some of which are listed below:

* Implement a *virtual paths* mechanism, which allows remapping of the request path to file, FTP, and HTTP paths. 
* Selectively enforcing security features, such as watermarking, filtered by image name or path. 
* Omitting watermarks or other security features when accessing the server from specific IP addresses. 
* Forcing application of commands, such as `defaultImage=`, to all requests or to requests which exhibit a specific pattern in the URL path or query strings. 
* Disallowing use of CPU-intensive command(s) to prevent server abuse. 
* Allowing source images to be located on HTTP or FTP servers while still specifying them on the request path rather than with `src=`. 
* Control image quality settings (such as JPEG quality or sharpening) depending on the request path or image name.

Detailed information about creating, using, and managing rule sets can be found in the [Rule Set Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## See also {#see-also}

[Rule Set Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attribute::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093) 
