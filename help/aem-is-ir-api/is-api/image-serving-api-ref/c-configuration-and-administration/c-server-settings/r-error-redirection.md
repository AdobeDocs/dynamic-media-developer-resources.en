---
description: Use these server settings to redirect errors.
solution: Experience Manager
title: Error redirection
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
TQID: 'https://experienceleague.adobe.com/3fcob7pfE-bMms-4PtD5MKkcolKHmXEWdzEL7vgzLhc'
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
# Error redirection{#error-redirection}

Use these server settings to redirect errors.

>[!NOTE]
>
>Pipe characters (|) in the net path are not supported for error redirection.

## PS::errorRedirect.rootUrl - Redirect Server {#section-85f22e48d68842a490b0e1191543b558}

The root URL ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]]) for the secondary Image Serving deployment to which requests which fail locally should be redirected. Error redirect is disabled (default) when this setting is empty or not defined.

## PS::errorRedirect.connectTimeout - Redirect Connection Timeout {#section-3971be8f720d4b32a2cc7860b4085971}

Maximum time (in msec) the server waits for a connection with the secondary server to be established before returning an error to the client.

## PS::errorRedirect.socketTimeout - Redirect Response Timeout {#section-69d8579f748d4044bca99dfb64dd523c}

Maximum time (in msec) the server waits for the secondary server to return data before abandoning the redirect request and returning an error to the client.
