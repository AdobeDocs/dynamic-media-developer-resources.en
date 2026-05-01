---
description: Image anchor. Origin point when this image is used as a layer in a template or composite image.
solution: Experience Manager
title: Anchor
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
TQID: https://experienceleague.adobe.com/-TTw4Ax-VpOdeyD7T-Q-94A2I-BsrOYUuU2mdjiL3zQ
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
---
# Anchor{#anchor}

Image anchor. Origin point when this image is used as a layer in a template or composite image.

Also defines the default center point for rotation.

## Properties {#section-95740f14160744e7bc763094b8be40d8}

Two integer numbers, separated by a comma. Pixel offset relative to the top, left corner of the full-resolution image.

Overridden by `anchor=`(which in turn can be overridden with `origin=`).

## Default {#section-ca3a4cc837d643519eff15951f2b47a1}

The center point of the image is used if this field is not present or if it is empty, and if this is a valid image record (that is, if `catalog::Path` is valid).

## See also {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
