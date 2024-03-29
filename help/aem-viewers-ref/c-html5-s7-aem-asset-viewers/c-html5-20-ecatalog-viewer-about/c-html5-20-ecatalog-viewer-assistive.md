---
title: Assistive technology support
description: All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
---
# Assistive technology support{#assistive-technology-support}

All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.

The top-level viewer element has role `region` and `aria-label` attribute set by default to the name of the viewer. You can control the label with the `Container.LABEL` localization symbol.

Buttons have the role `button` and descriptive text set with the `aria-label` attribute. The value of `aria-label` attribute is populated from the value of the button's localization symbol. When a button is disabled, the `aria-disabled` attribute is set accordingly.

The main view has role `application`. A brief description of the main view is provided in `aria-roledescription`, with the value defined by the `ROLE_DESCRIPTION` localization symbol of the corresponding main view component. Navigation hints for keyboard users are provided using `aria-describedby`, the text for the usage hint comes from the `USAGE_HINT` localization symbol. If an asset has a label defined in the UserData field, the `aria-label` attribute is set with the value of such label.

Hot spots, regions, and image maps have the role `button` and descriptive text set with `aria-label` attribute, with the value of the hot spot or image map label. When the user puts a focus on hot spots or image maps, navigation hints for keyboard users are provided using `aria-describedby`, with the text for the usage hint coming from the `USAGE_HINT` localization symbol.

Thumbnails have the role `dialog` with `aria-label` attribute controlled by the `ThumbnailGridView.LABEL` localization symbol. Individual thumbnails have role `button`. If a thumbnail is selected, it gets `aria-selected` attribute set to `true`.

Components that display swatches have the role `listbox` with `aria-label` attribute set to the value of the `LABEL` localization symbol of that component. Individual swatches have the role `option` with `aria-setsize` and `aria-posinset` attributes to describe the swatch position in the set. If a swatch is selected, it gets the `aria-selected` attribute set to `true`.

Drop-down lists are activated by buttons with additional `aria-haspopup` attribute set to `true` and the `aria-controls` attribute referencing the actual drop-down panel element. The drop-down panel itself has the role `menu` with subelements having the role `menuitem`. Each menu item has the `aria-label` attribute specified.

Modal dialog boxes have the role `dialog`. The dialog box's header element is referenced by the `aria-labelledby` attribute.
