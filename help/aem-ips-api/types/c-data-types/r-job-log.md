---
description: The job log after the job has run.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
TQID: 'https://experienceleague.adobe.com/R3h5NRNxH00Qskdzvw6ul55STF234SudJbjLGYrd238'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# [!DNL JobLog]{#joblog}

The job log after the job has run.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  companyHandle  | `xsd:string`  | Company handle.  |
|  jobHandle  | `xsd:string`  | Job handle.  |
|  jobName  | `xsd:string`  | Job name.  |
|  originalJobName  | `xsd:string`  |The original name submitted for the job with `submitJob`.  |
|  submitUserEmail  | `xsd:string`  | The email address of the user who submitted the job.  |
|  logType  | `xsd:string`  | Choice of job log types.  |
|  jobSubType  | `xsd:string`  | Additional job information.  |
|  startDate  | `xsd:dateTime`  | The start date, time, and time zone of the job.  |
|  endDate  | `xsd:dateTime`  | The end date, time, and time zone of the job.  |
|  [!DNL description]  | `xsd:string`  |A description of the job as originally specified in `submitJob`.  |
|  fileSuccessCount  | `xsd:int`  | Number of files successfully processed.  |
|  fileErrorCount  | `xsd:int`  | Number of files that caused an error.  |
|  fileWarningCount  | `xsd:int`  | Number of files that generated a warning.  |
|  fileDuplicateCount  | `xsd:int`  | Number of duplicate files.  |
|  fileUpdateCount  | `xsd:int`  | Number of files updated.  |
|  totalFileCount  | `xsd:int`  | Number of files processed by the logged job.  |
|  transferSuccessCount  | `xsd:int`  | Number of successful transfers.  |
|  transferErrorCount  | `xsd:int`  | Number of transfer errors.  |
|  transferWarningCount  | `xsd:int`  | Number of transfer warnings.  |
|  fatalError  | `xsd:boolean`  | Whether the job generated a fatal error.  |
|  detailTotalRows  | `xsd:int`  |The total number of rows matching the query, which may be larger than the size of `detailArray` due to page size limits.  |
|  detailArray  | `types:JobLogDetailArray`  | The array of details about the logged job.  |

