---
title: Installing under a different user account than administrator
description: After installation, set up services to run under the other user account.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 20bb00cb-3af6-4573-bbff-8c4f984ed2ae
TQID: 'https://experienceleague.adobe.com/XSRkCVE0e9lk-oxdU7JxPdWR-2hDi-XVquBE212g4HE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Installing under a different user account than administrator{#installing-under-a-different-user-account-than-administrator}

After installation, set up services to run under the other user account.

1. Access the Windows Local Security Policy settings by selecting **[!UICONTROL Start Menu]** > **[!UICONTROL Settings]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administration Tools]** > **[!UICONTROL Local Security Policy]**.
1. Select **[!UICONTROL Security Settings]** > **[!UICONTROL Local Policies]** > **[!UICONTROL User Rights Assignment]**.
1. Double-click the **[!UICONTROL Log on as a service]** policy.
1. Select **[!UICONTROL Add…]** and select the User or Group, then select **[!UICONTROL Ok]** to confirm.

