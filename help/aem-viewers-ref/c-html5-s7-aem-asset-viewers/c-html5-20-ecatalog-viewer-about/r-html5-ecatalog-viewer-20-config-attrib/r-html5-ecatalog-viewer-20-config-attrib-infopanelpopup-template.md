---
title: InfoPanelPopup.template
description: InfoPanelPopup.template
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 20618017-2f73-4951-baa9-2063a0f4efcb
---
# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`template`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> template</span></span> </p> </td> 
   <td> <p>The content template that the data returned from the info server is merged into. </p> <p>The content template is an XML following this DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>The actual syntax for the content template is the following: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>That is, the template must start with the <span class="codeph"> &lt;info&gt;</span> element that may contain optional default <span class="codeph"> &lt;var&gt;</span> elements. The template content itself, <span class="codeph"> TEMPLATE_CONTENT</span> is HTML text. In addition, the content template may contain variable names enclosed in <span class="codeph"> $</span> characters that are replaced with the variable values that the info server returns or with default ones. </p> <p>Default variables that are defined in the template can be either global (if rollover attribute is not set) or specific to a certain rollover key (if rollover attribute is present). </p> <p>During template processing variables that are specific to roll over keys take precedence over global variables. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>When you configure Info Panel Popup, the HTML code, and JavaScript code passed to the Info Panel runs on the client's computer. Therefore, make sure that such HTML code and JavaScript code are secure.

## Properties {#section-6dd7785357d740d095fa9f7fd0f67da4}

Optional.

## Default {#section-cd5db06d08aa4de49e37d6c938b41570}

None.

## Example {#section-16d184665c484964af9a22f79ff3f840}

Assuming that the info server response returns the product name as variable `$1$` and product image URL is returned as variable `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
