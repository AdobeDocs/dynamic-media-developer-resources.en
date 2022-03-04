---
title: Request pre-processing
description: Image Rendering provides a simple request pre-processor based on regular-expression match and substitution rules.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
---
# Request pre-processing{#request-pre-processing}

Image Rendering provides a simple request pre-processor based on regular-expression match and substitution rules.

Collections of rules (rule sets) can be attached to each material catalog, including the default catalog. Rules are specified with XML-formatted files.

Request pre-processing rules can modify the path and query portions of requests before they are processed by the Image Rendering parser. This precept includes manipulating the path, adding commands, changing command values, and applying templates, or macros. Rules can also be used to configure and override certain features which are normally controlled only with catalog attributes, such as setting the default reply image size or limiting HTTP service to specific client IP addresses.

Request pre-processing rules are suitable for various applications, some of which are listed below:

* Implement a *virtual paths* mechanism, which allows remapping of the request path to file, FTP, and HTTP paths. 
* Disallowing use of CPU-intensive commands to prevent server abuse. 
* Control image quality settings (such as JPEG quality or sharpening) depending on the request path or image name.

Detailed information about creating, using, and managing rule sets can be found in the Rule Set Reference.

See also Rule Set Reference, attribute::RuleSetFile
