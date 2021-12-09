---
title: Assistive technology support
description: All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
exl-id: b2bfd93b-707e-4a03-a14e-14ec23328fdd
---
# Assistive technology support{#assistive-technology-support}

All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.

The top-level viewer element has role `region` and `aria-label` attribute set by default to the name of the viewer. You can control the label with the `Container.LABEL` localization symbol.

Buttons have the role `button` and descriptive text set with `aria-label` attribute. The value of `aria-label` attribute is populated from the value of the button's localization symbol. When a button is disabled, `aria-disabled` attribute is set accordingly.

Slider components have the role `slider` with attributes `aria-valuenow`, `aria-valuemin`, and `aria-valuemax` to describe the current slider position.

Drop-down lists are activated by buttons with additional `aria-haspopup` attribute set to `true` and `aria-controls` attribute referencing the actual drop-down panel element. The drop-down panel itself has the role `menu` with subelements having the role `menuitem`. Each menu item has the `aria-label` attribute specified.

Modal dialog boxes have the role `dialog`. The dialog box's header element is referenced by the `aria-labelledby` attribute.
