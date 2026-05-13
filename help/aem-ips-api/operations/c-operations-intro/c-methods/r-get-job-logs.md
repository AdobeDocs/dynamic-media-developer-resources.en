---
description: Gets specified job logs for the selected company. You can sort by characters, direction, start and end dates, and number of rows.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
TQID: 'https://experienceleague.adobe.com/lerbQ3ibPCI3zqkrmgPrwTAYp1w6dWxIWYRt2Ij51oA'
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
# getJobLogs{#getjoblogs}

Gets specified job logs for the selected company. You can sort by characters, direction, start and end dates, and number of rows.

 Syntax 

## Authorized User Types {#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-8cfdc7994da24678a45edcb37e9a2166}

**Input (getJobLogsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | No  | The company handle.  |
|  userHandle  | `xsd:string`  | No  | Gets logs for jobs submitted by a specific user.  |
|  sortBy  | `xsd:string`  | No  | Lets you select sort fields.  |
|  sortDirection  | `xsd:string`  | No  | Sort order (ascending or descending).  |
|  startDate  | `xsd:dateTime`  | No  | The date and time of the start of the job log. Provide the time zone with the request for this field.  |
|  endDate  | `xsd:dateTime`  | No  | The date and time of the end of the job log. Provide the time zone with the request for this field.  |
|  numRows  | `xsd:int`  | No  | Maximum number of rows to return.  |

**Output (getJobLogsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  jobLogArray  | `types: JobLogArray`  | Yes  | Array of job logs.  |

## Examples {#section-35871c94b4a44559912577efddbc46a6}

This code sample returns IPS job logs for a specific company. You can also use it to return job logs for a specific user or company and user.

**Request** 

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**Response** 

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```
