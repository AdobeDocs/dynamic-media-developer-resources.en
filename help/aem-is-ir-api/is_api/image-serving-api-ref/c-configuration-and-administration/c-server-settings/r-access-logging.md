---
description: Use these server settings for logging access.
seo-description: Use these server settings for logging access.
seo-title: Access logging
solution: Experience Manager
title: Access logging
topic: Scene7 Image Serving - Image Rendering API
uuid: 3829df27-1daf-4046-973b-e488b32a764c
index: y
internal: n
snippet: y
---

# Access logging{#access-logging}

Use these server settings for logging access.

 Syntax 

## TC::directory - Log File Folder {#section-5d9e2168d4504bbe9868b7d6051c9d67}

The folder to which the Platform Server writes log files. This can be an absolute path or a path relative to *`install_folder`*. Default is [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>The new folder must be created before changing this setting. Make sure the folder has the correct read/write access privileges if Image Serving is installed to run under a user account other than root.

## TC::maxDays - Number of Days to Keep Log Files {#section-45cbecffc5694c87b7d5c176a44a4885}

The number of days log files should be preserved. New log files are created every day at midnight. At this time, the server will delete all files in the log file folder that are older than the specified number of days, including those written by the Image Server or Render Server. Default is 10.

## TC::prefix - Access Log File Name {#section-1003856323b844049632710a5a056aa7}

Name prefix for the file to which access log data is written. The date and the file suffix ( [!DNL  *`yyyy`*- *`mm`*- *`dd`*.log]) are appended to the specified string. The name of the access log file must be different from that of the trace log file. Default is " `access-`".

## TC::pattern - Access Log Pattern {#section-22775ea85cee444d8a7d7336a3b1feef}

Specifies the data pattern for Platform Server access log records. The pattern string specifies variables which are substituted with their corresponding values. All other characters in the pattern string are transferred literally to the log record.

To use the cache warm-up utility, spaces must be used as field separators. The Platform Server replaces all spaces and '%' characters in field values with `%20` and `%25`, respectively.

The following pattern variables are supported: 

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Pattern</b> </th> 
   <th class="entry"> <b>Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>Remote IP address. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>Local IP address. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>Response byte count excluding HTTP headers, or ' ' if zero. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>Response byte count excluding HTTP headers. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>Request processing time in milliseconds. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>thread id (for cross-referencing debug/error log entries). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>date and time, formatted as <span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> SSS </span> offset </span> </p> <p> ( <span class="varname"> SSS </span> are msec, <span class="varname"> offset </span> is the GMT time offset); the time value is captured when the response is sent to the client. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>Request method ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span>, and so forth). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>Request overlap (number of requests processed concurrently). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>Local port on which this request was received. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>Query string (prepended with a '?' if it exists). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>First line of request (request method, URI, HTTP version). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>Same as <span class="codeph"> %r </span>, but applies limited HTTP-encoding to the URI to avoid log parsing problems. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP response status code. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>User session ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>Date and time, in Common Log Format. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>Remote user that was authenticated (if any), else ''. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>URI path. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>Local server name. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>Request processing time in seconds. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r </span> </p> </td> 
   <td> <p>Platform Server cache key (cache file folder/name). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>Platform Server cache management keyword: <span class="codeph"> { REUSED | CREATED | UPDATED | REMOTE | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE | VALIDATED | IGNORED | UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>The response MIME type. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>The destination context if a context forward occurs. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p>The <span class="codeph"> etag </span> response header value (MD5 signature of the response data). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r </span> </p> </td> 
   <td> <p>Error message. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r </span> </p> </td> 
   <td> <p>Time taken to retrieve cache entry or data from Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r </span> </p> </td> 
   <td> <p>Time taken for request parsing and image catalog lookup. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>Indicates whether or not this request attempted any path-based access outside of the catalog system. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>IP address of the peer server in the cache cluster which delivered the cache entry or '-' if <span class="codeph"> CacheUse </span> is neither <span class="codeph"> REMOTE_CREATED </span> nor <span class="codeph"> REMOTE_UPDATED </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>Error category: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=no error. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=image(s) not found on the server. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS protocol usage error or a content error other than 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=other server error. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=request refused due to temporary server overload. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p>The upper-cased value of <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>The root id of the request's main catalog. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>The time it takes Platform Server to send response after writing data to the output stream. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p>Like <span class="codeph"> %B </span>, but includes values for 304 (not modified) responses. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r </span> </p> </td> 
   <td> <p>The final URL after all ruleset transformations. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>}i </span> </p> </td> 
   <td> <p>The value of the specified HTTP request header. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>The value of the specified HTTP response header. </p> </td> 
  </tr> 
 </tbody> 
</table>

Default is `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.` 
