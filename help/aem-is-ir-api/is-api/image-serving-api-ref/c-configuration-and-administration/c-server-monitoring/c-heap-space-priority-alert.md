---
description: A priority alert is sent when the free Java heap space is below the specified threshold immediately following a Java garbage collection cycle.
solution: Experience Manager
title: Heap space priority alert
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Heap space priority alert{#heap-space-priority-alert}

A priority alert is sent when the free Java heap space is below the specified threshold immediately following a Java garbage collection cycle.

Repeated alerts should be addressed by increasing the Java heap space. Subsequent occurrences of this condition does not result in an email alert until the delay period specified with `AS::monitorAlertGenerator.heapSpaceResetInterval` has expired. 
