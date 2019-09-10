---
description: Four types of layers are supported.
seo-description: Four types of layers are supported.
seo-title: Layer types
solution: Experience Manager
title: Layer types
topic: Scene7 Image Serving - Image Rendering API
uuid: d88b2163-7c9f-4885-9722-be3339e7127a
index: y
internal: n
snippet: y
---

# Layer types{#layer-types}

Four types of layers are supported.

## Image layers {#section-3e53df1437694272aca03f927fc0db07}

Image layers must have a `src=` command which specifies the image to be used as the layer. A separate image may be specified with `mask=` to be used as layer mask or the image may have already an alpha channel. The size of image layers is always derived from the image, but the image is often scaled to fit using the `size=` command. A clip path may be applied with `clipPath=`.

## Text layers {#section-dc2aec6416a340bcb20c1f884323c8d0}

Must have a `text=` or `textPs=` command which provides the text content in form of a rich-text-formatted (RTF) text fragment. Text layers can be self-sizing to their content, or may be given explicit sizes, (for example, if text is to be wrapped to a specific width, or if the text must be constrained within a specific area). `textPs=` support flowing of text into arbitrary shapes defined with `textFlowPath=` and onto arbitrary paths defined with `textPath=`. `textPs=` also supports rendering text into the text box or specified shape at arbitrary angles ( `textAngle=`).

## Solid color layers {#section-56dfb672756643dda08dc93294809eb0}

Solid color layers are often used for layer 0 in templates, so that the size of the composite image is fixed and independent of any image content. Solid color layers require a `color=` attribute, and either `size=` or `mask=`, and support most other commands and attributes to modify appearance. Solid color layers may be given arbitrary shapes with `clipPath=`.

## Effect layers {#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop-style layer effects, such as drop shadows and glow effects, are implemented by IS using special sub-layers which can be attached to image, text, and solid color layers. These effect layers inherit the parent layer mask and position from the parent layer, and are limited in functionality. 
