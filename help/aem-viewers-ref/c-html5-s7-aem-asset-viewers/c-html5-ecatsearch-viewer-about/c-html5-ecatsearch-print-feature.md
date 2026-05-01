---
description: The viewer lets you output the catalog content to a printer.
solution: Experience Manager
title: Print feature
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
TQID: https://experienceleague.adobe.com/ui4QqLbhl80-QFV3l4Tu3pUkkIXMfqJHm1BIOKd9Iq8
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Print feature{#print-feature}

The viewer lets you output the catalog content to a printer.

 The print feature is triggered by a dedicated button in the toolbar. Clicking the button lets the user choose a print range and the number of pages per sheet.

The quality of the print can be adjusted using the `printquality` configuration parameter. Note that setting `printquality` to values significantly higher than the default is not recommended. The reason is because it leads to very high memory consumption by the web browser on the client's system. Also, make sure that the maximum image response size set for your Dynamic Media Classic company is larger than the configured `printquality` value.

>[!NOTE]
>
>The Print feature is only available on desktop systems, except Internet Explorer 9.
