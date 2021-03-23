---
description: General Server Settings
solution: Experience Manager
title: General
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# General{#general}

General Server Settings

## TC::PsPort - Main Listening Port {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Specifies the main listening port for the Platform Server. This port is also used to access the documentation and example pages for Image Serving, Image Rendering, and the Dynamic Media Viewers (if installed).

## IS::CacheServerUrl - Caching Service Root Url {#section-bcca227a1f91453b834db4ea050968e2}

Specifies the HTTP root path to allow the Image Server access to the caching service. Must be set to [!DNL http://localhost:TC::PsPort /is/cache/secondary], with the port number matching `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - Remote Image Source Default TTL {#section-e4c31228b459492cacd2f482d9575f71}

The TTL for cached images obtained via HTTP from a remote source using the `src={…}` construct. Only used when the remote server does not include an Expiration header in its HTTP response. Integer value in seconds.

## IS::RemoteUrlTimeout - Remote Image Source Timeout {#section-437646c479cc4bea81dae42100a3c50a}

The time the Image Server will wait for a remote server to deliver the requested image file via HTTP before returning an error. Integer value in seconds.

## PS::allowDefaultCatalogRequests - Enable/Disable Default Catalog Requests {#section-484e442a115a49b4ac269d1718b351e1}

Set to false to disallow requests which do not include a valid catalog id in the path. Default is `true`. When set to `false`, an error is returned for requests without a catalog id.

>[!NOTE]
>
>`req=catalogprops` is not subject to this setting.

## PS::saveToFile.saveTimeout - File Save Timeout {#section-d22afd8ad86144b28684ed95a59db40e}

Default timeout value for `req=saveToFile` when `timeout=`is not specified. `msec`. An error will be returned if the save operation is not completed within the specified amount of time. 
