---
title: Assistive technology support
description: All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets,Accessibility
role: Developer,User
exl-id: f0cde820-237c-4594-8a16-d272af4c976b
---
# Assistive technology support{#assistive-technology-support}

All viewer components support ARIA (Accessible Rich Internet Applications) roles and attributes to improve integration with assistive technologies such as screen readers.

The top-level viewer element has role `region` and `aria-label` attribute set by default to the name of the viewer. You can control the label with the `Container.LABEL` localization symbol.

Buttons have the role `button` and descriptive text set with `aria-label` attribute. The value of `aria-label` attribute is populated from the value of the button's localization symbol. When a button is disabled, `aria-disabled` attribute is set accordingly.

The main view has role `application`. A brief description of the main view is provided in `aria-roledescription`, with the value defined by the `ROLE_DESCRIPTION` localization symbol of the corresponding main view component. Navigation hints for keyboard users are provided using `aria-describedby`, the text for the usage hint comes from the `USAGE_HINT` localization symbol. If an asset has a label defined in the UserData field, the `aria-label` attribute is set with the value of such label.
