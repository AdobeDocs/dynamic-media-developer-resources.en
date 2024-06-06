---
description: This release—Image Serving 6.6.1 and Image Rendering 6.6.1—supersedes Image Serving 6.5.3 and Image Rendering 6.5.3.
solution: Experience Manager
title: About this release
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
---
# About this release{#about-this-release}

This release—Image Serving 6.6.1 and Image Rendering 6.6.1—supersedes Image Serving 6.5.3 and Image Rendering 6.5.3.

## Known issues and behavior changes {#section-9dbc05206187477f926a78e8108a34e1}

* Use of the question mark character in asset IDs is no longer supported, even if the character is URL encoded. 
* Dynamic banner `/xfl/flash/` requests are no longer supported and now return an HTTP 404 error code. 
* W2P `/is/agm/` requests are no longer supported. 
* Some error messages no longer render to the browser. As such, you need to review the trace log to debug.

## New Features {#section-b1386e36cb4544ebb79766a06b16842d}

* Smart Swatch 
* Smart Crop

## Bug Fix {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Fixed issue where the `\qc` RTF option followed by a space caused a request to not render.
