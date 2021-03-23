---
description: Use these server settings to configure alert thresholds.
solution: Experience Manager
title: Alert thresholds
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Alert thresholds{#alert-thresholds}

Use these server settings to configure alert thresholds.

## AS:: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS:: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

A response time alert is emitted when the average time to process a request during the sampling interval exceeds the threshold set here. Expressed in msec; integer 0 or larger. Typical values are between 100 and 1000 msec, depending on the complexity of operations.

>[!NOTE]
>
>Requests which result in 4xx or 5xx response status are not considered for this alert.

## AS::monitorAlertGenerator.maxErrorRate - Error Response Rate ThresholdAS::monitorAlertGenerator.maxErrorRate - Error Response Rate {#section-76ba77fd3102419395e0f86719a1f3ec}

An error alert is issued when the ratio of HTTP error responses to total responses during the sampling interval exceeds the specified threshold.

Real value between 0.0 and 1.0.Typically set to between 0.005 and 0.1. Set to 1 to disable error alerts.

## AS::monitorAlertGenerator.minRequestRate - Low Traffic Threshold {#section-8dfb89ed138640fd86f5ce1dae2a533e}

A minimum traffic alert is sent when the average number of requests per second received during the current sampling interval falls below this threshold. Disable the alert by setting this value to 0. Expressed in requests per second. Real value 0 or larger.

## AS::monitorAlertGenerator.minFreeHeapSpace -Free Heap Space Threshold {#section-ce6705045f6842769030ccb1894594cc}

Specifies the minimum free Java heap space. A priority alert is sent immediately after a Java garbage collection cycle when the free heap space is below this threshold. 50 MB is recommended for safe operation of the Platform Server. Keeping the free heap space above this value reduces the frequency of garbage collection cycles, which may improve overall server performance. Integer value in bytes, 0 or larger.

## AS::monitorAlertGenerator.maxOverlap - Maximum Number of Concurrent Requests {#section-ddc6925bff944758ab19bcc9cf3f2589}

An overlap alert is triggered when the average number of requests processed concurrently during the averaging interval exceeds this threshold. A high overlap can indicate a possible server overload condition.

Integer value 1 or larger. Typical range is 20 to 50, depending on the cache hit rate and request compexity.

## AS::monitorAlertGenerator.lockedThreshold - Locked Request Threshold {#section-012a1c9937d445708380339279c62d80}

Specifies the number of seconds a request must be pending before it is considered locked or hung. A locked request alert is issued if at the end of an averaging interval at least one request has been pending for longer than the specified time period. Positive integer value in msec.

To account for complex render requests and requests that involve obtaining data from foreign HTTP servers, it is recommended to set this value to at least 30 seconds (unless such a condition is to be detected by this alert). 
