---
description: Sets the password of a specific user or the default user to a specific value, depending on whether you specify a user handle.


solution: Experience Manager
title: setPassword

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# setPassword{#setpassword}

Sets the password of a specific user or the default user to a specific value, depending on whether you specify a user handle.

 Password expiration date is optional. If omitted, the password never expires. 

## Authorized User types {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*Only* the `IpsAdmin` user type is authorized to run setPassword calls against other users.

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `IpsUser` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser` 
* `ImagePortalUser`

## Parameters {#section-0531294341f7483d89dacaa393dd659a}

**Input (setPasswordParam)** 

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Required </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>User handle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> password </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col4"> <p>Password. </p> <p>The following requirements are enforced on the chosen password: </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">Passwords are case-sensitive. </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">The minimum password length is eight characters. </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">The password must contain one or more characters from the following character classes: 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">Lowercase English characters. For example, <span class="codeph"> a b c d e </span> and so forth </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">Uppercase English characters. For example, <span class="codeph"> A B C D E </span> and so forth. </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">Numbers. For example, <span class="codeph"> 1 2 3 4 5 </span> and so forth. </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">Special symbol characters. For example, you can use any of the following: <span class="codeph"> ` ~ ! @ # $ % ^ * ( ) _ + - = { } | [ ] &amp; \ : " ; ' &lt; &gt; ? , . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpires </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime </span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Determines password expiration date. <p>Note:  Provide the time zone with the request for this field. Time zones are adjusted to Central Time. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (setPasswordReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-23a6fbabdb3c4c3180076057e47ae567}

This code sample creates a user password. The password never expires because `passwordExpires` was omitted.

**Request** 

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**Response**

None. 
