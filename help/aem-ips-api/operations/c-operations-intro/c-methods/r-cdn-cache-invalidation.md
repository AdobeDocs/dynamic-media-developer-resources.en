---
description: Forwards the supplied list of URLs to the Dynamic Media CDN (Content Distribution Network) provider to invalidate their existing cache of HTTP responses.
solution: Experience Manager
title: cdnCacheInvalidation
topic: Dynamic Media Image Production System API
---

# cdnCacheInvalidation{#cdncacheinvalidation}

Forwards the supplied list of URLs to the Dynamic Media CDN (Content Distribution Network) provider to invalidate their existing cache of HTTP responses.

## cdnCacheInvalidation: About {#section-4f70d2bc79d64288b961836ab17e9690}

CDN cache invalidation forces all HTTP requests for these URLs to be revalidated against the current published data on the Dynamic Media network after this invalidation request is processed through the CDN network. Any URLs that are not connected to the Dynamic Media service URL structure and directly matching the Dynamic Media company root ID assigned when the company is created will result in an API fault for the entire request. Any invalid URLs that the CDN does not support that it considers invalid will also result in an API fault for the entire request.

**Frequency of Use: Rules**

The rules governing the frequency of the use of this feature are controlled by Dynamic Media's CDN partners. The CDN retains the discretion to degrade the responsiveness of these invalidations to maintain optimum performance of its service to its users. Should Dynamic Media be notified of overuse of this feature we will need to resort to disabling the feature on either a per company basis or entirely across the service.

**Confirmation Emails**

Confirmation emails from the Dynamic Media CDN partner can be sent to the list's creator or up to 5 other email addresses. The API sends the confirmation when the entire CDN network has been notified that the URLs referenced in the email have been cleared. A single call to `cdnCacheInvalidation` can send multiple emails if the number of URLs supplied exceed the number that Dynamic Media can deliver to the CDN partner on a single notification. Currently, that would be if the request exceeds 100 URLs, but is subject to change based at the request of the CDN partner.

**Supported Since**

6.0

## Authorized User Types {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin` 
* `IpsCompanyAdmin`

## Parameters {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** ( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Required</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> Yes </p> </td> 
   <td> <p> The handle to the company connected with the URLs to invalidate. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> types:UrlArray</span> </p> </td> 
   <td> <p> Yes </p> </td> 
   <td> <p> List of up to 1000 URLs to invalidate from the CDN cache. All URLS must contain the Dynamic Media company root ID to be invalidated. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Required</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col4"> <p>A handle referencing the purge request. </p> <p>The <span class="codeph"> cdnCacheInvalidation</span> API now invalidates the cache almost immediately (~5 seconds). As such, polling for invalidation status is generally no longer required. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col4"> <p>Estimated seconds to completion of the purge request. Clients should wait for this time before polling status. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-f414361a58e84dfcbbac30a358d02125}

This example requests four URLs to be invalidated in the CDN cache. The response contains summary counts of the success of the operations and a list of error details supplied directly from the CDN to assist the client in use of this feature.

`getCdnCacheInvalidationStatus` operation.

**Request**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**Response**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```

