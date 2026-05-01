---
description: Image Serving components are managed by the Server Supervisor, which is a Linux daemon or Windows Service (S7Supervisor.exe, listed as 'Dynamic Media Image Serving' in the Services Control Panel).
solution: Experience Manager
title: Server supervisor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
TQID: https://experienceleague.adobe.com/BlWS2Yko-7HLw0Byvzj09EGY8iukEzgFJbfdQ1GiQLE
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Server supervisor{#server-supervisor}

Image Serving components are managed by the Server Supervisor, which is a Linux daemon or Windows Service (S7Supervisor.exe, listed as 'Dynamic Media Image Serving' in the Services Control Panel).

In addition to starting and stopping other Image Serving components, the Server Supervisor is responsible for ensuring the health of these other components. Should a component crash, it is automatically restarted to minimize any service interruptions.

## Starting and stopping {#section-061d28d74e034a30adc39ea3e2031cd0}

The Server Supervisor is started, stopped, and restarted with the Image Serving utility script. See the [Utilities documentation](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) for more information.

Starting and stopping the Server Supervisor automatically starts and stops all other Image Serving components.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
