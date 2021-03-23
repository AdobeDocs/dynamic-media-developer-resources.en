---
description: Use these server settings to debug trace logging.
solution: Experience Manager
title: Debug_trace logging
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Debug_trace logging{#debug-trace-logging}

Use these server settings to debug trace logging.

>[!NOTE]
>
>It is recommended to configure all log files to be written to the same folder as `TC::directory`. This ensures that all Image Serving log files participate in the automatic log file rotation configured with `TC::maxDays`, which will prevent potential server instability due to out-of-disk-space conditions.

## SV::log - Server Supervisor Trace Log File Path {#section-3697bc480ff646e79cacc2812c55ef26}

Folder and base file name for Server Supervisor log files. The path can be absolute or relative to *[!DNL install_folder]*. The Server Supervisor will append a hyphen and the current date ( *[!DNL -yyyy-mm-dd]*) to the file name (before the file suffix, if any). It is recommended to send all log files to the same folder as Platform Server log files ( `PS::LogFolder`) to leverage the log file management implemented by the Platform Server ( `PS::LogDays`). Default is [!DNL logs/Supervisor.log].

>[!NOTE]
>
>The new folder must be created before changing this setting. Make sure the access permissions are set so that the Server Supervisor has the necessary create, read, and write privileges.

## SV::tracelevel - Server Supervisor Trace Log Level {#section-36f8634741da4c618d67aa628b5fe474}

Log level can be 1, 2, 3, or 4. Default is 2.

## IS::Log - Image Server Debug Log File Path {#section-73a3f09b77f2446c9f82207b7d8aec39}

Folder and base file name for Image Server trace log files. The path can be absolute or relative to *[!DNL install_folder]*. The ImageServer will append a hyphen and the current date ( *[!DNL -yyyy-mm-dd]*) to the file name (before the file suffix, if any). It is recommended to send Image Server log files to the same folder as Platform Server log files ( `PS::LogFolder`) to leverage the log file management implemented by the Platform Server (see `PS::LogDays`).

>[!NOTE]
>
>The new folder must be created before changing this setting. Make sure the access permissions are set so that Image Serving has the necessary create, read, and write privileges.

## IS:TraceClient - Image Server Debug Log Level {#section-3851f1f68e404430985c629ac80534db}

Log level can be 1, 2, 3, or 4 (Default is 2)

Level 1 logs events related to start-up, shut-down, and Platform Server connections.

Level 2 also logs connecting to and disconnecting from source images.

Level 3 adds logging of requests for pixel data and delivery of same to the Platform Server.

Level 4 records all messages received from the Platform Server.

Level 3 and 4 should be used for debug purposes only, as the log files can become very large.

## IS::TraceStatsInterval - Image Server Statistics Log Interval {#section-1d8df96d61044e33a5b2b2b0309c2d59}

The Image Server writes memory statistics to its trace log file at the interval specified by this setting. Valid range is 5 to 86,400 seconds. 
