---
description: Use these server settings to configure the monitoring and alerting system.
solution: Experience Manager
title: Monitoring and alerting system
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Monitoring and alerting system{#monitoring-and-alerting-system}

Use these server settings to configure the monitoring and alerting system.

## AS::monitorAlertGenerator.enableGlobalAlerting - Alerting System Enable {#section-612f8ea61794426ab205e22e5f665fa9}

Enable email notification by setting to 'true' and configuring the email notification settings. Setting to `false` turns off all email alerts - this can be useful when taking a server off-line for maintenance. Boolean.

## AS::mailSender.host - SMTP Host {#section-151df07e7b44446581339bb7abeeba7a}

The IP address of the SMTP email server.

## AS::mailSender.port- SMTP Port {#section-4b25efca8fd84d5c92dafacd0555e99d}

The listening port for the SMTP email server.

## AS::monitorAlertGenerator.messageTo - Message Recipient {#section-0017bbaa15434117a70900c3f1163960}

One or more email addresses to which alerts should be sent. Use semicolons as separators.

## AS::monitorAlertGenerator.messageFrom - Message Sender {#section-db320cba4ac2438ca1cfe6abce4aed87}

The email address that should be used in the **[!UICONTROL From]** email field.

## AS::monitorAlertGenerator.alertInterval - Monitoring Interval {#section-99cb2e3380c1499e9d5aec3671ed73c7}

The monitoring system will accumulate alert conditions during the alert interval and send an alert email containing all accumulated alerts at the end of each interval. Milliseconds, integer value, 60000 or larger. Typically set to 5 or 10 minutes.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Heap Space Alert Interval {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Minimum time after an heap space alert before another one will be emitted. Interval time in msec. Integer value, 0 or larger.

## AS::monitorAlertGenerator.minTrafficForAlerts - Minimum Traffic to Enable Alerting {#section-8b4db2d6f96642309ca35c49eb3ab230}

Requests per second. No response time and error alerts will be emitted if traffic falls below this threshold. Set to 0 to send response time and error alerts regardless of the traffic volume. Real value 0 or larger. 
