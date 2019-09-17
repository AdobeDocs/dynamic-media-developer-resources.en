---
description: The viewer lets you output the catalog content to a printer.
seo-description: The viewer lets you output the catalog content to a printer.
seo-title: Print feature
solution: Experience Manager
title: Print feature
topic: Dynamic media
uuid: 4ff170a3-ce37-454f-b4b0-b323de3dc9c9
---

# Print feature{#print-feature}

The viewer lets you output the catalog content to a printer.

 The print feature is triggered by a dedicated button in the toolbar. Clicking the button lets the user choose a print range and the number of pages per sheet.

The quality of the print can be adjusted using the `printquality` configuration parameter. Note that setting `printquality` to values significantly higher than the default is not recommended. The reason is because it leads to very high memory consumption by the web browser on the client's system. Also, make sure that the maximum image response size set for your SPS company is larger than the configured `printquality` value.

>[!NOTE]
>
>The Print feature is only available on desktop systems, except Internet Explorer 9.

