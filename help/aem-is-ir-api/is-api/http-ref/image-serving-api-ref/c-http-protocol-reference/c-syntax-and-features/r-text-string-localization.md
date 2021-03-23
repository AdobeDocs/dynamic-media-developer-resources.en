---
description: Text string localization allows image catalogs to contain multiple locale-specific representations for the same string value.
solution: Experience Manager
title: Text string localization
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Text string localization{#text-string-localization}

Text string localization allows image catalogs to contain multiple locale-specific representations for the same string value.

 The server returns to the client the representation matching the locale specified with `locale=`, thereby avoiding client-side localization and allowing applications to switch locales simply by sending the appropriate `locale=` value with the IS text requests.

## Scope {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

Text string localization is applied to all string elements which include the localization token ` ^loc= *`locId`*^` in the following catalog fields: 

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Catalog field</b> </th> 
   <th class="entry"> <b>String element in field</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>Any sub-element containing a translatable string (delimited by any combination of separators ',' ';' ':' and/or the start/end of the field). </p> <p> A <span class="codeph"> 0xrrggbb </span> color value at the beginning of a localizable field is excluded from localization and passed through without modification. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>Any single- or double-quoted attribute value, except the values of the <span class="codeph"> coords= </span> and <span class="codeph"> shape= </span> attributes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>The value of any <span class="codeph"> target.*.label </span> and <span class="codeph"> target.*.userdata </span> property. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>The value of any property. </p> </td> 
  </tr> 
 </tbody> 
</table>

## String syntax {#section-d12320edf300409f8e17565b143acafc}

Localization-enabled *`string`* elements in the image catalog consist of one or more localized strings, each preceded by a localization token.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>Internal locale ID for the <span class="varname"> localizedString </span> following this <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>Localized string. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>String to be used for unknown locales. </p> </td> 
 </tr> 
</table>

*`locId`* must be ASCII and may not include '^'.

'^' may occur anywhere in sub-strings with or without HTTP-encoding. The server matches the entire *`localizationToken`* `^loc=locId^` pattern to separate substrings.

*`stringElements`* which do not include at least one *`localizationToken`* are not considered for localization.

## The translation map {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` defines the rules used by the server to determine which *`localizedStrings`* to return to the client. It consists of a list of input *`locales`* (matching the values specified with `locale=`), each with none or more internal locale ids ( *`locId`*). For example:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Empty *`locId`* values indicate that the *`defaultString`* should be returned, if available.

Refer to the description of `attribute::LocaleStrMap` for details.

## The translation process {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Given the example translation map above and the request `/is/image/myCat/myItem?req=&locale=nl`, the server first looks for " `nl`" in the locale map. The matched entry `nl,N` indicates that for each *`stringElement`*, the *`localizedString`* marked with `^loc=N^` should be returned. If this *`localizationToken`* is not present in the *`stringElement`*, an empty value is returned.

Let's say `catalog::UserData` for `myCat/myItem` contains the following (line breaks inserted for clarity):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

The server would return the following in response to our example request:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Unknown locales {#section-26dfeefbd60345de94bbfeaaf7741223}

In the above example, `attribute::LocaleStrMap` has an entry with an empty *`locale`* value. The server uses this entry to handle all `locale=` values which are not explicitly specified otherwise in the translation map.

The example translation map specifies that in such a case the *`defaultString`* should be returned if available. Thus, the following would be returned if this translation map were applied to the request `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Examples {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Language families**

Multiple *`locId`* values may be associated with each *`locale`* in the translation map. This allows supporting country-specific or region-specific variations (e.g US English vs UK English) for select *`stringElements`* while handling most contents with common base locales (e.g. International English).

For our example, we want to add support for US-specific English ( `*`locId`* EUS`) and UK-specific English ( `*`locId`* EUK`), to support the occasional alternative spelling. If EUK or EUS do not exist, we would fall back to E. Similarly, Austrian-specific German variants ( `DAT`) could be made available where needed while returning common German *`localizedStrings`* (marked with `D`) most of the time.

`attribute::LocaleStrMap` would look like this:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

The following table describes the output for some representative *`stringElement`* and *`locale`* combinations: 

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>locale</i> </th> 
   <th class="entry"> <p>Output string </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>all others </p> </td> 
   <td> <p>English </p> <p>German </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>all others </p> </td> 
   <td> <p>English </p> <p>UK-English </p> <p>German </p> <p>Austrian </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> Note that for this example the <span class="varname"> locId </span> DDE does not exist in <span class="codeph"> attribute::LocaleStrMap </span>, and thus the substring associated with this <span class="varname"> locId </span> is never returned. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>all others </p> </td> 
   <td> <p>English </p> <p>US-English </p> <p>German </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

