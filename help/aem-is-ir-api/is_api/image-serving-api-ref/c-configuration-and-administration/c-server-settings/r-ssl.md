---
description: Use these server settings for SSL.
seo-description: Use these server settings for SSL.
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: 06869e8c-5278-4b57-b531-8e9fca63f5e2
index: y
internal: n
snippet: y
---

# SSL{#ssl}

Use these server settings for SSL.

## TC::SslPort - Listening Port {#section-c80eb582bf684b3fa7313a77cc606769}

Specifies the listening port for the Platform Server for SSL connections. Default is 8443.

## TC::keystoreFile - Keystore File Path {#section-0cdf9b3cfcf249818b22221d01bafebe}

Specify the path/name of the SSL keystore file. May be an absolute path or a path relative to [!DNL *[!DNL install_folder]*/conf]. Default is *install_folder*/conf/scene7keystore.

## TC::keystorePass - Keystore Password {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

The password for the keystore file. Default is `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Select the type of keystore. ' `Java'` (default) and ' `PKCS12`' are supported. 
