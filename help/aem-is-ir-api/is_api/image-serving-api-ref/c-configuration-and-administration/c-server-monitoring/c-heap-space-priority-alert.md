---
description: A priority alert is sent when the free Java heap space is below the specified threshold immediately following a Java garbage collection cycle.
seo-description: A priority alert is sent when the free Java heap space is below the specified threshold immediately following a Java garbage collection cycle.
seo-title: Heap space priority alert
solution: Experience Manager
title: Heap space priority alert
topic: Scene7 Image Serving - Image Rendering API
uuid: 5e82a34b-b8c7-4058-a123-05c693b524b6
index: y
internal: n
snippet: y
---

# Heap space priority alert{#heap-space-priority-alert}

A priority alert is sent when the free Java heap space is below the specified threshold immediately following a Java garbage collection cycle.

Repeated alerts should be addressed by increasing the Java heap space. Subsequent occurrences of this condition does not result in an email alert until the delay period specified with `AS::monitorAlertGenerator.heapSpaceResetInterval` has expired. 
