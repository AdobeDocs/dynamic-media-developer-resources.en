---
description: A priority alert is sent when the free Java heap space is below the specified threshold immediately following a Java garbage collection cycle.
seo-description: A priority alert is sent when the free Java heap space is below the specified threshold immediately following a Java garbage collection cycle.
seo-title: Heap space priority alert
solution: Experience Manager
title: Heap space priority alert
topic: Scene7 Image Serving - Image Rendering API
uuid: 1146f593-9bf0-4900-bc35-9e4483f0fbb8
index: y
internal: n
snippet: y
---

# Heap space priority alert{#heap-space-priority-alert}

A priority alert is sent when the free Java heap space is below the specified threshold immediately following a Java garbage collection cycle.

Repeated alerts should be addressed by increasing the Java heap space. Subsequent occurrences of this condition does not result in an email alert until the delay period specified with `AS::monitorAlertGenerator.heapSpaceResetInterval` has expired. 
