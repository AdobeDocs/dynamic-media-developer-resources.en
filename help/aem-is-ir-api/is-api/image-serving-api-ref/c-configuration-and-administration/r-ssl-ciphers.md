---
description: The Connector tag in server.xml supports a ciphers attribute to limit the ciphers that can be chosen for an SSL connection.
solution: Experience Manager
title: Defining SSL ciphers
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 7734ba02-4442-4a3d-acbf-e14d8ad66279
---
# Defining SSL ciphers{#defining-ssl-ciphers}

The Connector tag in server.xml supports a ciphers attribute to limit the ciphers that can be chosen for an SSL connection.

By default all ciphers are available. The list is comma separated and can contain any of the following values:

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

`SSL_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

`TLS_RSA_WITH_AES_128_CBC_SHA`

If any of the values is wrong, Tomcat will enable every single cipher. So it is essential to check with an external tool after configuration to see which ciphers are actually enabled.

As an example the following configuration will enable only the "128-bit" cipher suites and above:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
