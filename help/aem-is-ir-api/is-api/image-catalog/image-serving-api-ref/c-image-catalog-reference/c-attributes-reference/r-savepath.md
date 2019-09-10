---
description: Root path for saveToFile=. Relative path for the root folder to which images generated with req=saveToFile should be written.
seo-description: Root path for saveToFile=. Relative path for the root folder to which images generated with req=saveToFile should be written.
seo-title: SavePath
solution: Experience Manager
title: SavePath
topic: Scene7 Image Serving - Image Rendering API
uuid: 02b88e83-7fee-40d4-95ea-daba9a608e8e
index: y
internal: n
snippet: y
---

# SavePath{#savepath}

Root path for saveToFile=. Relative path for the root folder to which images generated with req=saveToFile should be written.

 `SavePath` is a text string value.

## Properties {#section-343d1371e966491c92854a8df14c3c50}

Text string. Must be empty or a valid relative folder path. Always combined with the absolute root path configured with `ImageServer::SaveDirectory`.

## Default {#section-ae751eea97654f399c6aaee3f3252cbb}

Inherited from `default::SavePath` if not defined. Saving to files is disabled if the resolved value is empty.

## See also {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) 
