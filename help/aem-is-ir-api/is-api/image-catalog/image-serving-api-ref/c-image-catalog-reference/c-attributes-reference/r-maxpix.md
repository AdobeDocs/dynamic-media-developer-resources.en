---
description: Reply image size limit. Maximum reply image width and height that may be returned to the client.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
TQID: 'https://experienceleague.adobe.com/lX4ooC7B0VIJDRr0yZJVmp45qnXbSuimMZSyU9rWLcw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# MaxPix{#maxpix}

Reply image size limit. Maximum reply image width and height that may be returned to the client.

The server returns an error if a request would cause a reply image whose width or height is larger than `attribute::MaxPix`.

## Properties {#section-b175425b9e9f48e0b1a71640f6a9e936}

Two integer numbers, larger than 0, separated by a comma. Width and height in pixels. May also be set to `0,0` to permit any reply image size with no limitations.

## Default {#section-1003537434da432fb2af100ecdbf9d72}

Inherited from `default::MaxPix` if not defined or if empty.

## See also {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
