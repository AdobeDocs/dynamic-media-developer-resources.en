---
description: Gets the job logs for an asset. Items returned in the array contain detailed information about each entry in the job log for that asset. The logMessage response field is localized based on the authHeader field.


solution: Experience Manager
title: getAssetJobLogs

feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
---

# getAssetJobLogs{#getassetjoblogs}

Gets the job logs for an asset. Items returned in the array contain detailed information about each entry in the job log for that asset. The logMessage response field is localized based on the authHeader field.

 Syntax 

## Authorized User Types {#section-72b98cdb0f6f47f5aabdc183a45ea577}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-9586617e124b4da4acb6b66b2a9adad8}

**Input (getAssetJobLogsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company to which the asset belongs.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | The handle to asset with the job logs to be retrieved.  |

**Output (getAssetJobLogsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`jobLogArray`*`  | `types:AssetJobLogArray`  | Yes  | Job log array.  |

## Examples {#section-f03d7f3ec5d043d38227f926fb7609f6}

This code sample retrieves the job logs of a specific asset. The response returns a job log array with detailed information about all of the jobs in which the asset was used.

**Request** 

```java
<getAssetJobLogsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetJobLogsParam>
```

**Response** 

```java
<getAssetJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <jobLogArray>
      <items>
         <jobHandle>j|6||Add_2007-10-24-16:11:07</jobHandle>
         <jobName>Add_2007-10-24-16:11:07</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS</logMessage>
         <logType>UploadSuccess</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2007-10-24T16:12:32.297-07:00</logDate>
      </items>
      <items>
         <jobHandle>j|6||submitServerUploadJob40_2008-06-11-11:38</jobHandle>
         <jobName>submitServerUploadJob40_2008-06-11-11:38</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS.</logMessage>
         <logType>FileUpdated</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2008-06-11T11:38:48.547-07:00</logDate>
      </items>
   </jobLogArray>
</getAssetJobLogsReturn>
```

