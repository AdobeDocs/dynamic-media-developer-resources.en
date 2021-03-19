---
description: All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.
seo-description: All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.
seo-title: Assistive technology support
solution: Experience Manager
title: Assistive technology support
uuid: 9de323c9-d383-41e9-ae44-06600f44a85e
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,Business Practitioner
---

# Assistive technology support{#assistive-technology-support}

All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.

The top-level viewer element has role `region` and `aria-label` attribute set by default to the name of the viewer. You can control the label with the `Container.LABEL` localization symbol.

The main view has role `application`. A brief description of the main view is provided in `aria-roledescription`, with the value defined by the `ROLE_DESCRIPTION` localization symbol of the corresponding main view component. Navigation hints for keyboard users are provided using `aria-describedby`, the text for the usage hint comes from the `USAGE_HINT` localization symbol. If an asset has a label defined in the UserData field, the `aria-label` attribute is set with the value of such label.

Components that display swatches have the role `listbox` with `aria-label` attribute set to the value of the `LABEL` localization symbol of that component. Individual swatches have the role `option` with `aria-setsize` and `aria-posinset` attributes to describe the swatch position in the set. If a swatch is selected it gets the `aria-selected` attribute set to `true`. 
