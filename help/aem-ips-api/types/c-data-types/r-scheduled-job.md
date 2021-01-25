---
description: A job that is scheduled to run.
seo-description: A job that is scheduled to run.
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
topic: Dynamic Media Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
---

# ScheduledJob{#scheduledjob}

A job that is scheduled to run.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Company handle.  |
|  `*`jobHandle`*`  | `xsd:string`  | Scheduled job handle.  |
|  `*`name`*`  | `xsd:string`  | Job name.  |
|  `*`originalName`*`  | `xsd:string`  | Original name of the scheduled job.  |
|  `*`type`*`  | `xsd:string`  | Job type.  |
|  `*`submitUserEmail`*`  | `xsd:string`  | The email address of the user who scheduled the job.  |
|  `*`locale`*`  | `xsd:string`  |The locale to be used for job log details and email localization. Locales are specified as `<language_code>[- <country_code>]`, where the language code is a lower-case, two-letter code as specified by ISO-639, and the optional country code is an upper-case, two-letter code as specified by ISO-3166. For example, the locale string for English (United States) would be: `en-US`.  |
|  `*`description`*`  | `xsd:string`  |A description of the job as originally specified in `submitJob`.  |
|  `*`execSchedule`*`  | `xsd:string`  | When the job is scheduled to run.  |
|  `*`nextFireTime`*`  | `xsd:dateTime`  | The date, time, and time zone when the job will be fired.  |
|  `*`timeZone`*`  | `xsd:dateTime`  | The time zone of the scheduled job.  |
|  `*`triggerState`*`  | `xsd:int`  | Choice of job trigger state.  |
|  `*`imageServingPublishJob`*`  | `types:ImageServingPublishJob`  | Job details for an image serving publish job.  |
|  `*`imageServingRenderJob`*`  | `types:ImageServingRenderJob`  | Job details for an image rendering job.  |
|  `*`videoPublishJob`*`  | `types:VideoPublishJob`  |Job details for a video publish job. See [VideoPublishJob](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html).  |
|  `*`serverDirectoryPublishJob`*`  | `types:ServerDirectoryPublishJob`  | Job details for a server directory publish job.  |
|  `*`uploadDirectoryJob`*`  | `types:UploadDirectoryJob`  | Job details for an upload directory job.  |
|  `*`uploadUrlsJob`*`  | `types:UploadUrlsJob`  | Job details for an upload URLs job.  |
|  `*`optimizeImagesJob`*`  | `types:OptimizeImagesJob`  | |
|  `*`ripPdfsJob`*`  | `types:RipPdfsJob`  | |
|  `*`reprocessAssetsJob`*`  | `types:ReprocessAssetsJob`  | |
|  `*`exportJob`*`  | `types:ExportJob`  |Allow authorized export of previously uploaded files. See [Export Job](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html).  |

## Notes {#section-34ec157f281f412f9f0f6e861e6ed0cd}

When you specify a job type value in `submitJob`, the system returns a job based on that type. The following jobs can be returned:

* `imageServingPublishJob` 
* `imageRenderingPublishJob` 
* `videoPublishJob` 
* `serverDirectoryPublishJob` 
* `uploadDirectorhJob` 
* `uploadUrlsJob`

