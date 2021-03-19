---
description: All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.
seo-description: All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.
seo-title: Assistive technology support
solution: Experience Manager
title: Assistive technology support
uuid: 0abed8d4-9754-47b1-9de7-cce665de03b4
feature: "Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility"
role: "Developer,Business Practitioner"
---

# Assistive technology support{#assistive-technology-support}

All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.

The top-level viewer element has role `region` and `aria-label` attribute set by default to the name of the viewer. You can control the label with the `Container.LABEL` localization symbol.

Buttons have the role `button` and descriptive text set with `aria-label` attribute. The value of `aria-label` attribute is populated from the value of the button's localization symbol. When a button is disabled, `aria-disabled` attribute is set accordingly.

Slider components have the role `slider` with attributes `aria-valuenow`, `aria-valuemin`, and `aria-valuemax` to describe the current slider position.

Thumbnails have the role `dialog` with `aria-label` attribute controlled by the `ThumbnailGridView.LABEL` localization symbol. Individual thumbnails have role `button`. If a thumbnail is selected, it gets `aria-selected` attribute set to `true`.

Components that display swatches have the role `listbox` with `aria-label` attribute set to the value of the `LABEL` localization symbol of that component. Individual swatches have the role `option` with `aria-setsize` and `aria-posinset` attributes to describe the swatch position in the set. If a swatch is selected it gets the `aria-selected` attribute set to `true`.

Drop-down lists are activated by buttons with additional `aria-haspopup` attribute set to `true` and `aria-controls` attribute referencing the actual drop-down panel element. The drop-down panel itself has the role `menu` with sub-elements having the role `menuitem`. Each menu item has the `aria-label` attribute specified.

Modal dialog boxes have the role `dialog`. The dialog box's header element is referenced by the `aria-labelledby` attribute. 
