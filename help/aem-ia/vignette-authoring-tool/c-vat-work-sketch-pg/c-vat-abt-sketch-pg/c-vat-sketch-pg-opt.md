---
description: null
seo-description: null
seo-title: Sketch Page Options
solution: Experience Manager
title: Sketch Page Options
topic: Scene7 Image Authoring
uuid: 29ea1dbe-e895-4cac-bc9e-9f66da9915ec
---

# Sketch Page Options{#sketch-page-options}

The following options are available at the bottom of the side menu:

**Solver:** When you solve on the [!DNL Sketch] page, [!DNL Image Authoring] distributes the preview material over the features you've defined so far.

Click **[!UICONTROL Start]** each time you want to solve the sketch features for the selected object. The button name changes to [!DNL Stop]. When the material distribution looks correct, click **[!UICONTROL Stop]**.

Click the **[!UICONTROL Action]** button to use the [!DNL Reset], [!DNL Incremental Mode], and [!DNL Set Current As Base] options to periodically save your work as the baseline for a particular object. Choose [!DNL Incremental Mode] and create a few features. When you are completely satisfied with those features, click **[!UICONTROL Set Current As Base]**. From then on, each time you click **[!UICONTROL Reset]**, you start from the point at which you clicked [!DNL Set Current As Base]. The next time you reach a point where you are satisfied with your work, choose **[!UICONTROL Set Current As Base]** again. Now, when you start over, you start from the new [!DNL Set Current As Base] point. If you don't choose [!DNL Incremental Mode], you always start over from the very beginning.

** Display:** Switch between the following:

* Normal shows the sketch lines you've added with a preview material applied. 
* Texture shows the preview material without the sketch lines. 
* Features shows the sketch lines without the preview material.

**Image:** Switch between the [!DNL View] display (the editable view) and the [!DNL Render] display (showing an applied material).

**Origin:** The choices in this drop-down list are determined by the [origins] section of the [!DNL vat.ini] file. You can have a total of up to six user-defined origins, but origin 2 must always be skipped. The entry in the first position in the [!DNL vat.ini] file is the default choice in the drop-down list. Choose an origin from the list and define it by positioning the origin manually on the selected object. The origin value is in inches relative to the top, left corner of the texture space.

** Preview Texture:** [Choose the texture](../../c-vat-flow-pg/c-vat-test-flow-work/t-vat-prev-text.md#task-ae35e07a54de4eebb9c17721f54e1132) for previewing your sketch work.

**Preview Blend:** Move the slider between Transparent and Opaque to adjust the rendering of the [!DNL Preview Texture] on the image. 
