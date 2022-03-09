---
title: Uploading assets by way of HTTP POSTs to the UploadFile Servlet
description: Uploading assets into Dynamic Media Classic involves one or more HTTP POST requests that set up a job to coordinate all the log activity associated with the uploaded files.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
---
# Uploading assets by way of HTTP POSTs to the UploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Uploading assets into Dynamic Media Classic involves one or more HTTP POST requests that set up a job to coordinate all the log activity associated with the uploaded files.

Use the following URL to access the UploadFile Servlet:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>All POST requests for an upload job must originate from the same IP address.

**Access URLs for Dynamic Media regions**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geographic location </p> </th> 
   <th colname="col2" class="entry"> <p>Production URL </p> </th> 
   <th colname="col3" class="entry"> <p>Staging URL (use for pre-production development and testing) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>North America </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europe, Middle East, Asia </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japan/Asia Pacific </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## Workflow of the upload job {#section-873625b9512f477c992f5cdd77267094}

The upload job consists of one or more HTTP POSTs that use a common `jobHandle` to correlate processing into the same job. Each request is `multipart/form-data` encoded and consists of the following form parts:

>[!NOTE]
>
>All POST requests for an upload job must originate from the same IP address.

| HTTP POST form part | Description |
|---|---|
|`auth` |  Required. An XML authHeader document specifying authentication and client information. See **Request authentication** under [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
|`file params` |  Optional. You can include one or more files to upload with each POST request. Each file part can include a filename parameter in the Content-Disposition header that is used as the target filename in IPS if no `uploadPostParams/fileName` parameter is specified. |

| HTTP POST form part  | uploadPostParams element name  | Type  | Description  |
|---|---|---|---|
|`uploadParams` (Required. An XML `uploadParams` document specifying the upload parameters)  |  `companyHandle` | `xsd:string` | Required. Handle to the company to which the file is being upload. |
|`uploadParams` (Required. An XML `uploadParams` document specifying the upload parameters)|`jobName` | `xsd:string` | Either `jobName` or `jobHandle` is required. Name of the upload job. |
|`uploadParams` (Required. An XML `uploadParams` document specifying the upload parameters)|`jobHandle` | `xsd:string` | Either `jobName` or `jobHandle` is required. Handle to an upload job started in a previous request. |
|`uploadParams` (Required. An XML `uploadParams` document specifying the upload parameters)|`locale` | `xsd:string` | Optional. Language and country code for localization. |
|`uploadParams` (Required. An XML `uploadParams` document specifying the upload parameters)|`description` | `xsd:string` | Optional. Description of the job. |
|`uploadParams` (Required. An XML `uploadParams` document specifying the upload parameters)|`destFolder` | `xsd:string` | Optional. Target folder path to prefix to a filename property, particularly for browsers and other clients that may not support full paths in a filename. |
|`uploadParams` (Required. An XML `uploadParams` document specifying the upload parameters)|`fileName` | `xsd:string` | Optional. Name of the target file. Overrides the filename property. |
|`uploadParams` (Required. An XML `uploadParams` document specifying the upload parameters)|`endJob` | `xsd:boolean` | Optional. Default is false. |
|`uploadParams` (Required. An XML `uploadParams` document specifying the upload parameters)|`uploadParams` | `types:UploadPostJob` | Optional if this is a subsequent request for an existing active job. If there is an existing job, `uploadParams` is ignored and the existing job upload parameters are used. See [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

Within the `<uploadPostParams>` block is the `<uploadParams>` block that designates the processing of the included files.

See [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

While you might assume that the `uploadParams` parameter can change for individual files as a part of the same job, that is not the case. Use the same `uploadParams` parameters for the entire job.

The initial POST request for a new upload job should specify the `jobName` parameter, preferably using a unique job name to simplify subsequent job status polling and job log queries. Additional POST requests for the same upload job should specify the `jobHandle` parameter instead of `jobName`, using the `jobHandle` value returned from the initial request.

The final POST request for an upload job should set the `endJob` parameter to true so that no future files are POSTed for this job. In turn, this allows the job to complete immediately after all POSTed files are ingested. Otherwise, the job times out if no additional POST requests are received within 30 minutes.

## UploadPOST response {#section-421df5cc04d44e23a464059aad86d64e}

For a successful POST request, the response body is an XML `uploadPostReturn` document, as the XSD specifies in the following:

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

The `jobHandle` returned is passed in the `uploadPostParams`/ `jobHandle` parameter for any subsequent POST requests for the same job. You can also use it to poll job status with the `getActiveJobs` operation or to query the job logs with the `getJobLogDetails` operation.

If there is an error processing the POST request, the response body consists of one of the API fault types as described in [Faults](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Example POST request {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## Example POST response - success {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## Example POST response - error {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
