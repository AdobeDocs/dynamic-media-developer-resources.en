---
description: Use these server settings for SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
TQID: 'https://experienceleague.adobe.com/VOdDIzV6b9J9AZ-qZyAj3AI77MukT1BbSzM-UM-B5N4'
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# SSL{#ssl}

Use these server settings for SSL.

## TC::SslPort - Listening Port {#section-c80eb582bf684b3fa7313a77cc606769}

Specifies the listening port for the [!DNL Platform Server] for SSL connections. Default is 8443.

## TC::keystoreFile - Keystore File Path {#section-0cdf9b3cfcf249818b22221d01bafebe}

Specify the path/name of the SSL keystore file. May be an absolute path or a path relative to [!DNL *[!DNL install_folder]*/conf]. Default is *install_folder*/conf/scene7keystore.

## TC::keystorePass - Keystore Password {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

The password for the keystore file. Default is `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Select the type of keystore. ' `Java'` (default) and ' `PKCS12`' are supported.
