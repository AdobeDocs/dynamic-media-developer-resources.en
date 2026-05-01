---
description: Four types of layers are supported.
solution: Experience Manager
title: Layer types
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
TQID: https://experienceleague.adobe.com/kYwZWWlsGZNgVWbsz-dL7rMJeR1BUCBBkqdS427Y5g8
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
# Layer types{#layer-types}

Four types of layers are supported.

## Image layers {#section-3e53df1437694272aca03f927fc0db07}

Image layers must have a `src=` command which specifies the image to be used as the layer. A separate image may be specified with `mask=` to be used as layer mask or the image may have already an alpha channel. The size of image layers is always derived from the image, but the image is often scaled to fit using the `size=` command. A clip path may be applied with `clipPath=`.

## Text layers {#section-dc2aec6416a340bcb20c1f884323c8d0}

Must have a `text=` or `textPs=` command which provides the text content in form of a rich-text-formatted (RTF) text fragment. Text layers can be self-sizing to their content, or may be given explicit sizes. For example, if text is to be wrapped to a specific width, or if the text must be constrained within a specific area. `textPs=` support flowing of text into arbitrary shapes defined with `textFlowPath=` and onto arbitrary paths defined with `textPath=`. `textPs=` also supports rendering text into the text box or specified shape at arbitrary angles ( `textAngle=`).

## Solid color layers {#section-56dfb672756643dda08dc93294809eb0}

Solid color layers are often used for layer 0 in templates, so that the size of the composite image is fixed and independent of any image content. Solid color layers require a `color=` attribute, and either `size=` or `mask=`, and support most other commands and attributes to modify appearance. Solid color layers may be given arbitrary shapes with `clipPath=`.

## Effect layers {#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop-style layer effects, such as drop shadows and glow effects, are implemented by IS using special sub-layers which can be attached to image, text, and solid color layers. These effect layers inherit the parent layer mask and position from the parent layer, and are limited in functionality.
