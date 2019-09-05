---
description: Image anchor. Origin point when this image is used as a layer in a template or composite image.
seo-description: Image anchor. Origin point when this image is used as a layer in a template or composite image.
seo-title: Anchor
solution: Experience Manager
title: Anchor
topic: Scene7 Image Serving - Image Rendering API
uuid: b43da34b-e785-444a-be70-150ce4fa3d98
index: y
internal: n
snippet: y
---

# Anchor{#anchor}

Image anchor. Origin point when this image is used as a layer in a template or composite image.

Also defines the default center point for rotation.

## Properties {#section-95740f14160744e7bc763094b8be40d8}

Two integer numbers, separated by a comma. Pixel offset relative to the top, left corner of the full-resolution image.

Overridden by `anchor=`(which in turn can be overridden with `origin=`).

## Default {#section-ca3a4cc837d643519eff15951f2b47a1}

The center point of the image is used if this field is not present or if it is empty, and if this is a valid image record (i.e. if `catalog::Path` is valid).

## See also {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](r_anchor.md#reference_6661E548AB284B82828D8D94C8DDEB7C) , [origin=](r_origin.md#reference_E11C7AC06E2240CC884C3FEC98F05138) 
