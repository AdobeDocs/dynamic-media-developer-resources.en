---
description: All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.
seo-description: All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.
seo-title: Assistive technology support
solution: Experience Manager
title: Assistive technology support
topic: Dynamic media
uuid: 72b414f4-b647-4afa-a409-a8ba90227d3f
---

# Assistive technology support{#assistive-technology-support}

All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.

The top-level viewer element has role `region` and `aria-label` attribute set by default to the name of the viewer. You can control the label with the `Container.LABEL` localization symbol.

Buttons have the role `button` and descriptive text set with `aria-label` attribute. The value of `aria-label` attribute is populated from the value of the button's localization symbol. When a button is disabled, `aria-disabled` attribute is set accordingly.

Buttons which let you navigate through carousel slides have labels that update in run-time depending on the currently selected slide. The template for these button's label is set with `CAROUSELVIEWER_TOOLTIP_GOTO` localization symbol.

The main view has role `application`. A brief description of the main view is provided in `aria-roledescription`, with the value defined by the `ROLE_DESCRIPTION` localization symbol of the corresponding main view component. Navigation hints for keyboard users are provided using `aria-describedby`, the text for the usage hint comes from the `USAGE_HINT` localization symbol. If an asset has a label defined in the UserData field, the `aria-label` attribute is set with the value of such label.

Hot spots, regions, and image maps have the role `button` and descriptive text set with `aria-label` attribute, with the value of the hot spot or image map label. When the user puts a focus on hot spots or image maps, navigation hints for keyboard users are provided using `aria-describedby`, with the text for the usage hint coming from the `USAGE_HINT` localization symbol. 
