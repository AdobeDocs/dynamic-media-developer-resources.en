---
description: Image Serving components are managed by the Server Supervisor, which is a Linux daemon or Windows Service (S7Supervisor.exe, listed as 'Dynamic Media Image Serving' in the Services Control Panel).
seo-description: Image Serving components are managed by the Server Supervisor, which is a Linux daemon or Windows Service (S7Supervisor.exe, listed as 'Dynamic Media Image Serving' in the Services Control Panel).
seo-title: Server supervisor
solution: Experience Manager
title: Server supervisor
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
---

# Server supervisor{#server-supervisor}

Image Serving components are managed by the Server Supervisor, which is a Linux daemon or Windows Service (S7Supervisor.exe, listed as 'Dynamic Media Image Serving' in the Services Control Panel).

In addition to starting and stopping other Image Serving components, the Server Supervisor is responsible for ensuring the health of these other components. Should a component crash, it is automatically restarted to minimize any service interruptions.

## Starting and stopping {#section-061d28d74e034a30adc39ea3e2031cd0}

The Server Supervisor is started, stopped, and restarted with the Image Serving utility script. See the [Utilities documentation](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) for more information.

Starting and stopping the Server Supervisor automatically starts and stops all other Image Serving components.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6) 
