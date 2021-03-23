---
description: The job log after the job has run.


solution: Experience Manager
title: JobLog

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# JobLog{#joblog}

The job log after the job has run.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Company handle.  |
|  `*`jobHandle`*`  | `xsd:string`  | Job handle.  |
|  `*`jobName`*`  | `xsd:string`  | Job name.  |
|  `*`originalJobName`*`  | `xsd:string`  |The original name submitted for the job with `submitJob`.  |
|  `*`submitUserEmail`*`  | `xsd:string`  | The email address of the user who submitted the job.  |
|  `*`logType`*`  | `xsd:string`  | Choice of job log types.  |
|  `*`jobSubType`*`  | `xsd:string`  | Additional job information.  |
|  `*`startDate`*`  | `xsd:dateTime`  | The start date, time, and time zone of the job.  |
|  `*`endDate`*`  | `xsd:dateTime`  | The end date, time, and time zone of the job.  |
|  `*`description`*`  | `xsd:string`  |A description of the job as originally specified in `submitJob`.  |
|  `*`fileSuccessCount`*`  | `xsd:int`  | Number of files successfully processed.  |
|  `*`fileErrorCount`*`  | `xsd:int`  | Number of files that caused an error.  |
|  `*`fileWarningCount`*`  | `xsd:int`  | Number of files that generated a warning.  |
|  `*`fileDuplicateCount`*`  | `xsd:int`  | Number of duplicate files.  |
|  `*`fileUpdateCount`*`  | `xsd:int`  | Number of files updated.  |
|  `*`totalFileCount`*`  | `xsd:int`  | Number of files processed by the logged job.  |
|  `*`transferSuccessCount`*`  | `xsd:int`  | Number of successful transfers.  |
|  `*`transferErrorCount`*`  | `xsd:int`  | Number of transfer errors.  |
|  `*`transferWarningCount`*`  | `xsd:int`  | Number of transfer warnings.  |
|  `*`fatalError`*`  | `xsd:boolean`  | Whether the job generated a fatal error.  |
|  `*`detailTotalRows`*`  | `xsd:int`  |The total number of rows matching the query, which may be larger than the size of `detailArray` due to page size limits.  |
|  `*`detailArray`*`  | `types:JobLogDetailArray`  | The array of details about the logged job.  |

