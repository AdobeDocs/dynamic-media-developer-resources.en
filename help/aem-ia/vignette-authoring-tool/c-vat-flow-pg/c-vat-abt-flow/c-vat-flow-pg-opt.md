---
description: null
seo-description: null
seo-title: Flowline Page Options
solution: Experience Manager
title: Flowline Page Options
topic: Scene7 Image Authoring
uuid: efcb99ab-0e40-43e6-aa5a-35813a97607b
index: y
internal: n
snippet: y
---

# Flowline Page Options{#flowline-page-options}

The following options are available at the bottom of the side menu:

**Display:** Use any of the following display options:

* **Texture:** Displays a pattern that covers the masked portion of the current object. Does not display the [!DNL Flowline Mesh], but changes to the flowlines affect the [!DNL Flowline Mesh]. 

* ** Normal:** Displays a pattern that covers the masked portion of the current object, as well as the [!DNL Flowline Mesh]. 

* **Unmasked:** The pattern ignores the current object and fills the [!DNL Flowline] with Mesh. If you change the size of the [!DNL Flowline], the pattern adjusts to keep the Mesh filled. 

* **Flowlines:** Displays the [!DNL Flowline] without any pattern. You can drag flowlines faster in this mode because the absence of the pattern requires less recalculating.

** Image:** Switch between the [!DNL View] image (without a material applied) and the [!DNL Render] image (showing an applied material).

**Origin:** The choices in this drop-down list are determined by the [origins] section of the [!DNL vat.ini] file. You can have a total of up to six user defined origins, but origin 2 must always be skipped. The entry in the first position in the [!DNL vat.ini] file is the default choice in the drop-down list. Choose an origin from the list and define it by positioning the origin manually on the selected object. The origin value is in inches relative to the top, left corner of the texture space.

Use the continuous origin setting when you are applying textures that have no significant center point, for example, stripes or plaids, and you want to [match the texture across adjacent flowline objects](../../c-vat-flow-pg/c-vat-test-flow-work/t-vat-match-text.md#task-568d59da3f7e48838669b17fe96fbed0).

[!DNL Image Authoring] may change the location of the origin when you match textures on adjacent objects.

**Preview Texture:** [Choose the texture](../../c-vat-flow-pg/c-vat-test-flow-work/t-vat-prev-text.md#task-ae35e07a54de4eebb9c17721f54e1132) for previewing your flowline work.

** Blend:** You can change the translucence of the preview material by dragging the [!DNL Blend] slider. 
