---
description: The IPS Web Service is supported by a set of WSDL (Web Services Description Language) documents that are accessed from any IPS installation on which the IPS Web Service component is installed. Each IPS API release includes a new WSDL file that references a versioned target XML namespace. Prior WSDL namespace versions are also supported to allow for backwards compatibility with existing applications.
solution: Experience Manager
title: IPS Web Service WSDL versions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# IPS Web Service WSDL versions{#ips-web-service-wsdl-versions}

The IPS Web Service is supported by a set of WSDL (Web Services Description Language) documents that are accessed from any IPS installation on which the IPS Web Service component is installed. Each IPS API release includes a new WSDL file that references a versioned target XML namespace. Prior WSDL namespace versions are also supported to allow for backwards compatibility with existing applications.

## WSDL access {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

Access the Scene7 WSDLs as shown below.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 

```

The default value for `<IPS_webapp>` is `scene7`.

**Service location**

The service URL is specified in the service section of the IPS Web Service WSDL document. The service URL is generally of the form:  

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 

```

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
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europe, Middle East, Asia </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japan/Asia Pacific </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## Supported WSDLs {#section-ebbba69880f94e9c823f1147974eb404}

Remember, you may need to modify your code if you want to use features in the latest version of the IPS API. The IPS API supports WSDLs for the following versions:  

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API release version </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API namespace </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pre-4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Existing applications that need to be modified to use new features must upgrade to the latest API version and may need to make changes to existing code. See the change log for details.

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**Bindings**

The IPS API Web Service supports a SOAP binding only.

**Supported transports**

The IPS API SOAP binding supports HTTP transport only. Make all SOAP requests using the HTTPS POST method.

**SOAP action header**

To process a request, set the SOAPAction HTTP header to the name of the requested operation. The operation name attribute in the WSDL binding section specifies the name.

**Message format**

The document/literal style is used for all input and output messages with types based on the XML Schema definition language ( [http://www.w3.org/TR/xmlschema-0/](http://www.w3.org/TR/xmlschema-0/)) and specified in the WSDL file. All types require qualified names using the target namespace value specified in the WSDL file.

**Request authentication**

The preferred method for passing authentication credentials in API requests is to use the `authHeader` element as defined in the IPS API WSDL.

```
<element name="authHeader"> 
    <complexType> 
       <sequence> 
            <element name="user" type="xsd:string"/> 
            <element name="password" type="xsd:string"/> 
            <element name="locale" type="xsd:string" minOccurs="0"/> 
            <element name="appName" type="xsd:string" minOccurs="0"/> 
            <element name="appVersion" type="xsd:string" minOccurs="0"/> 
            <element name="gzipResponse" type="xsd:boolean" minOccurs="0"/> 
            <element name="faultHttpStatusCode" type="xsd:int" minOccurs="0"/> 
       </sequence> 
    </complexType> 
 </element>
```

**Fields**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user </span> </p> </td> 
   <td colname="col2"> <p> Valid IPS user email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> password </span> </p> </td> 
   <td colname="col2"> <p>Password for user account. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> Optional locale for request. See <b>Locale</b> for details. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> Calling application name. This parameter is optional, but it is recommended that you include it in all requests. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> Calling application version. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> Optional flag to enable or disable gzip compression of response XML. By default, responses are gzip-compressed if the HTTP Accept-Encoding header indicates support for gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> Optional parameter to override the HTTP status code for fault responses. By default, fault responses return HTTP status code 500 (Internal Server Error). Some client platforms, including Adobe Flash, are unable to read the response body unless a status code of 200 (OK) is returned. </p> </td> 
  </tr> 
 </tbody> 
</table>

The `authHeader` element is always defined in the namespace `http://www.scene7.com/IpsApi/xsd`, regardless of API version.

The following is an example of using the `authHeader` element in a request SOAP header:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
      <user>user@scene7.com</user> 
      <password>mypassword</password> 
      <appName>MyApp</appName> 
      <appVersion>1.0</appVersion> 
   </authHeader> 
 </soap:Header>
```

**Other request authentication methods**

If for some reason it is not possible for your client application to pass the `authHeader` SOAP header, API requests can also specify credentials using HTTP Basic authentication (as specified in RFC 2617).

For HTTP Basic authentication, the HTTP header section of each SOAP POST request must include a header of the form:

`Authorization: Basic base64(<IPS_user_email>:<password>)`

Where `base64()` applies the standard Base64 encoding, `<IPS_user_email>` is the email address of a valid IPS user, and `<password>` is the user's password.

Send the Authorization header preemptively with the initial request. If no authentication credentials are included in the request, `IpsApiService` does not respond with a status code of `401 (Unauthorized)`. Instead, a status code of `500 (Internal Server Error)` is returned with a SOAP fault body stating that the request could not be authenticated.

Before IPS 3.8, authentication via SOAP header was implemented using the `AuthUser` and `AuthPassword` elements in the namespace `http://www.scene7.com/IpsApi`. For example:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

This style is still supported for backwards compatibility but has been deprecated in favor of the `authHeader` element.

**Request authorization**

After the caller's credentials are authenticated, the request is checked to ensure that the caller is authorized to perform the requested operation. Authorization is based on the user role of the caller and may also require checking the target company, target user, and other operation parameters. In addition, Image Portal users must belong to a Group with the required permissions to perform certain folder and asset operations. The Operations reference section details the authorization requirements for each operation.

**Sample SOAP request and response**

The following example shows a complete `addCompany` operation, including HTTP headers:

```
POST /scene7/services/IpsApiService HTTP/1.1 
User-Agent: Axis/2.0 
SOAPAction: addCompany 
Content-Type: text/xml; charset=UTF-8 
 
<?xml version='1.0' encoding='UTF-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soapenv:Header> 
      <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
        <user>user@scene7.com</user> 
        <password>mypassword</password> 
        <appName>MyApp</appName> 
        <appVersion>1.0</appVersion> 
      </authHeader> 
    </soapenv:Header> 
    <soapenv:Body> 
    <ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
      <ns1:companyName>Sample Company</ns1:companyName> 
      <ns1:expires>2008-07-31T12:00:00-06:00</ns1:expires> 
    </ns1:addCompanyParam> 
    </soapenv:Body> 
 </soapenv:Envelope>
```

And the corresponding response:

```
HTTP/1.1 200 OK 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 20:47:55 GMT 
 
<?xml version='1.0' encoding='utf-8'?><soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
     <ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
       <ns1:companyInfo> 
          <ns1:companyHandle>2</ns1:companyHandle> 
          <ns1:name>Sample Company</ns1:name> 
          <ns1:rootPath>SampleCompany/</ns1:rootPath> 
          <ns1:expires>2008-07-31T18:00:00.000Z</ns1:expires> 
       </ns1:companyInfo> 
     </ns1:addCompanyReturn> 
   </soapenv:Body> 
</soapenv:Envelope>
```

**SOAP faults**

When an operation encounters an exception condition, a SOAP fault is returned as the body of the SOAP message in place of the normal response. For example, if a non-admin user attempts to send the previous `addCompany` request, the following response is returned:

```
HTTP/1.1 500 Internal Server Error 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 16:36:20 GMT 
Connection: close 
 
<?xml version='1.0' encoding='utf-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
      <soapenv:Fault> 
         <faultcode>soapenv:Client</faultcode> 
         <faultstring>AuthorizationException</faultstring> 
         <detail> 
           <ns1:authorizationFault xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
               <code xmlns="http://www.scene7.com/IpsApi/xsd">20003</code> 
             <reason xmlns="http://www.scene7.com/IpsApi/xsd">User does not  
             have permission to access operation 'addCompany'</reason> 
           </ns1:authorizationFault> 
         </detail> 
      </soapenv:Fault> 
   </soapenv:Body> 
</soapenv:Envelope>
```

