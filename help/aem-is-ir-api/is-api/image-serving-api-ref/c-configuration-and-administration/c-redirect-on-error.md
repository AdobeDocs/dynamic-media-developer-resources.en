---
description: IS servers can be configured to fail-over to alternate servers for requests which involve a source image which cannot be opened or read successfully.
solution: Experience Manager
title: Redirect on error
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
---
# Redirect on error{#redirect-on-error}

IS servers can be configured to fail-over to alternate servers for requests which involve a source image which cannot be opened or read successfully.

The following types of requests are redirected:

* IS Images that are in the catalog, but not on disk.

  If an image is not in a catalog, error redirect should not happen when the image can't be found. 

* Corrupt images, color profiles, or fonts. 
* Static content can't be found on disk.

  Static content requests are redirected when it can't be found on disk, even if the referenced static content does not have a catalog record.

Error redirect will not happen in any other case.

When enabled and when such an error occurs during the processing of the request, the primary server will send the request to the secondary server for processing. The response, regardless of whether it indicates success or failure, is then forwarded directly to the client. The primary server marks log entries of such forwarded requests with cache use `REMOTE`. The response data is not cached locally by the primary server.

Error redirect is enabled by setting `PS::errorRedirect.rootUrl` to the HTTP domain name and port number of the secondary server. In addition, the connection timeout is configured with `PS::errorRedirect.connectTimeout` and the maximum time the primary server will wait for a response from the secondary server before returning an error to the client is configured with `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>If the secondary server cannot be contacted, a text error response will be returned to the client, even if a default image or error image is configured.

>[!NOTE]
>
>Pipe characters (|) in the net path are not supported for error redirection.

## See also {#section-2e8bfc128b944baf8108279d16492f3f}

[Error Redirection](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
