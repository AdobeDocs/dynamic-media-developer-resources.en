---
description: The Vignette Authoring Tool (part of the Dynamic Media Image Authoring package) provides mechanisms to control low-level aspects of the vignette render engine.
seo-description: The Vignette Authoring Tool (part of the Dynamic Media Image Authoring package) provides mechanisms to control low-level aspects of the vignette render engine.
seo-title: Advanced Render settings
solution: Experience Manager
title: Advanced Render settings
uuid: 18e7f3cf-4d30-445c-813c-546a91987b99
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Advanced Render settings{#advanced-render-settings}

The Vignette Authoring Tool (part of the Dynamic Media Image Authoring package) provides mechanisms to control low-level aspects of the vignette render engine.

>[!NOTE]
>
>Render Settings is an advanced feature of Image Rendering and Image Authoring. Contact Adobe Technical Support or your Adobe consulting representative for training, consultation, or both, on using Render Settings.

These settings are controlled interactively in Image Authoring. It is possible to apply the same settings in Image Rendering using the `rs=` command (or with the `catalog::RenderSettings` value). This mechanism is used to select different sharpening options for each material, and modify the behavior of the illumination rendering algorithms, such as varying the saturation of highlights or the contrast in shadows.

## Advanced Render Setting (rs=) values {#section-d9e7f341ebd44f07a4e90f1f5910726b}

<table id="table_1517FC39C7344EBB9F17BE20415DB057"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Code </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
   <th colname="col3" class="entry"> <p>Minimum value </p> </th> 
   <th colname="col4" class="entry"> <p>Maximum value </p> </th> 
   <th colname="col5" class="entry"> <p>Notes </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>A </p> </td> 
   <td colname="col2"> <p>Render Effects/Alternate Shader overrides the setting in the vignette. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>1 </p> </td> 
   <td colname="col5"> <p>A0=Render Effects </p> <p>A1=Alternate Shader </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>U </p> </td> 
   <td colname="col2"> <p>USM (UnSharp Mask). </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>2 </p> </td> 
   <td colname="col5"> <p>To use USM, U must be &gt; 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>W </p> </td> 
   <td colname="col2"> <p>USM amount (%). </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>500 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V </p> </td> 
   <td colname="col2"> <p>USM radius (pixels). </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>X </p> </td> 
   <td colname="col2"> <p>USM threshold (levels). </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q </p> </td> 
   <td colname="col2"> <p>Resizing mode. </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>5 </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_87184BB93E7F46D59BA1AAAFA8455512"> 
      <li id="li_E7711C3678ED4DE09E710F7C430CEF42">Nearest Neighbor </li> 
      <li id="li_CAE975B91C604DA0AA493F700AEBE199">Bi-Linear </li> 
      <li id="li_24E5A40B8A3F4C808A68686C27647CD5">Bi-Cubic </li> 
      <li id="li_42ACFCE65B4843ACAFA6A52255364642">Supersampling (default value) </li> 
      <li id="li_34EC85C4D15145DF80F7D3DB7B6244D3">Lanczos Window </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>R </p> </td> 
   <td colname="col2"> <p>Resampling mode. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>5 </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_FD4A9D73C32F47C3BF13776BB4D2818D"> 
      <li id="li_F08AD1D093D74059B60302374B472B52">Default </li> 
      <li id="li_FD4C859D975B44399475D4D93D6B05AB">Nearest Neighbor </li> 
      <li id="li_CA93566F5D4F4D3CAA1D0816562A3851">Bi-Linear </li> 
      <li id="li_D334ACF969E749A89A464B21C96CE8A6">Supersampling </li> 
      <li id="li_FAC72C36FF4A418F8A5B05F3B4E7C5D8">Adaptive </li> 
      <li id="li_6E9D81045A0C4804A4D35D9B239F6486">Poisson Sampler </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>Supersampling: Random. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>200 </p> </td> 
   <td colname="col5"> <p>Default is 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>Supersampling: Random rate. </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>20 </p> </td> 
   <td colname="col5"> <p>Default is 5. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>M </p> </td> 
   <td colname="col2"> <p>Adaptive Resizing: Depth. </p> </td> 
   <td colname="col3"> <p>4 </p> </td> 
   <td colname="col4"> <p>8 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>N </p> </td> 
   <td colname="col2"> <p>Adaptive Resizing: Width. </p> </td> 
   <td colname="col3"> <p>2 </p> </td> 
   <td colname="col4"> <p>10 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>P </p> </td> 
   <td colname="col2"> <p>Poisson: Samples/Pixel. </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>4 </p> </td> 
   <td colname="col5"> <p>Default is 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Y </p> </td> 
   <td colname="col2"> <p>Poisson: Use toggle. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>1 </p> </td> 
   <td colname="col5"> <p>Default is 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Render effects (older shader)</b> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>I </p> </td> 
   <td colname="col2"> <p>Highlights. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>J </p> </td> 
   <td colname="col2"> <p>Highlights saturation. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>50 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H </p> </td> 
   <td colname="col2"> <p>Shadows for bright materials. </p> </td> 
   <td colname="col3"> <p>50 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>K </p> </td> 
   <td colname="col2"> <p>Shadow saturation. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>400 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>Gloss-based extrapolation strength. </p> </td> 
   <td colname="col3"> <p>100 </p> </td> 
   <td colname="col4"> <p>600 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0 </p> </td> 
   <td colname="col2"> <p>Brightness compensation (checkbox) </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p>Default is on (blank) and deselected = F100G0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Alternate shader</b> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Z </p> </td> 
   <td colname="col2"> <p>Basic contrast. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p>Default is 50. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>a </p> </td> 
   <td colname="col2"> <p>Brightness compensation. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format different: a36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>b </p> </td> 
   <td colname="col2"> <p>Saturation adjustment. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format different: b36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>c </p> </td> 
   <td colname="col2"> <p>Shadows adjustment. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format different: c36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>d </p> </td> 
   <td colname="col2"> <p>Highlights adjustment. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format different: d36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>e </p> </td> 
   <td colname="col2"> <p>Specular highlights. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format different: e36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>xx </p> </td> 
   <td colname="col2"> <p>Shape. </p> </td> 
   <td colname="col3"> <p>-100 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p>See 'xx' in above values. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>k </p> </td> 
   <td colname="col2"> <p>Illumination adjustment. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format different: k64.138.175.60.xx.133.242 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>u &amp; s </p> </td> 
   <td colname="col2"> <p>Shadow hue shift. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format different: u8.1.2.3.4.5.6.7.8.s8.1.2.3.4.5.6.7.8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>v &amp; t </p> </td> 
   <td colname="col2"> <p>Highlight hue shift. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>Format different: v8.1.2.3.4.5.6.7.8.t8.1.2.3.4.5.6.7.8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>w </p> </td> 
   <td colname="col2"> <p>Saturation adjustment. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>g </p> </td> 
   <td colname="col2"> <p>Low saturation boost. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sample Advanced Render settings {#section-56528569eae44ecd997a289b211ff256}

<table id="table_062DCF66ACCC4A6997E3CA951C0A12B8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Setting composition </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>H60I30J10K200L400U1V10W100X0 </p> </td> 
   <td colname="col2"> <p>Default values in Image Authoring. 
     <ul id="ul_AA7CF1A3E6984B318265BBE8FFFBB4EE">
      <li> USM1
      <li id="li_8EC075956E2E4D5A91355122DC9BC938">H60 = Shadows for bright materials (50-100). </li> 
      <li id="li_F760B65E057146A7B56673D6B1A9A304">I30 = Highlights (0-100). </li> 
      <li id="li_376C275FDB3548958C09BD266C77318F">J10 = Highlights saturation (0-50). </li> 
      <li id="li_FE26429972F544869CDFE2DD61F39CC5">K200 = Shadow saturation (0-400). </li> 
      <li id="li_FB6BAA708427428AA4A3AC2E5D3B9932">L400 = Gloss-based extrapolation strength (100-600). </li> 
      <li id="li_6B2EEEE7F0D54E078462AAFC4E4FAB42">U1 = USM (Unsharp Mask) (0-2). </li> 
      <li id="li_7CD4E3662A6C48F9B5895D133D28BA2A">V10 = USM radius (1-100 pixels). </li> 
      <li id="li_949B6DB4959B46A892787CD5B3AD7485">W100 = USM amount (1%-500%). </li> 
      <li id="li_F39D3834D4A2478D993E5E9C9B434CFE">X0 = USM threshold (0-255 levels). </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H50I0J0K0L100U1V1W1 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_C6E6DD90ECAB4D2B9284A25A29923DC6"> 
      <li id="li_7B7A8C43BCEB4CB58C7074974CAB0419">USM1 </li> 
      <li id="li_A003B68023424DCABBF3A2CAF98C39A4">All maximum and brightness compensation is on. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0H50I0J0K0L100U1V1W1 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_AAEC098CED1C436E933B1C1B88DFB659"> 
      <li id="li_0CC34CDD796E4DFD802824FF21DB021B">USM1 </li> 
      <li id="li_E36886FB1D00444CBA19D7245E89B292">All maximum and brightness compensation is off. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0H100I100J50K400L600U2V100W500X255 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6BB668C6C055493DAAA38F4D3B9C20A7"> 
      <li id="li_D8BAFB41CF4C4B3FAD6F89AF5D7F223A">USM2 </li> 
      <li id="li_DA685F4DE4BA427BA7BE241A75C96152">All maximum and brightness compensation is off. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H80I70J40L300U1V8W80X5 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7C374842312E4AD0B62692BBCE6743A8"> 
      <li id="li_CC730580B54741FBBBFF507DE0FE1F15">H80 = USM amount </li> 
      <li id="li_C2801B2C093444AC9401793BC571EC27">I70 = Highlights </li> 
      <li id="li_518C6A690EC34614B0806A0C6BC535FF">J40 = Highlights saturation </li> 
      <li id="li_F280CF29D1E341D9AC9C0C16C2DEA1E6">L300 = Gloss-based extrapolation strength </li> 
      <li id="li_3F589F109AC94280911BD535C49E42E4">U1 = USM </li> 
      <li id="li_113FEC9B37D54511BAB3FEAC7C271858">V8 = USM radius </li> 
      <li id="li_E1BA7406A76B476EB1A89D6EDD87930C">W80 = Shadows for bright materials </li> 
      <li id="li_AAD479EF6A7F43B98A8C147FCD684ECA">X5 = USM threshold </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q5R3S11T103U1V6W120X5Z80b.188.88.75.37 </p> </td> 
   <td colname="col2"> <p>Alternate Shader with sharpen: </p> <p> 
     <ul id="ul_93AD53BB37EA47F6A3CEE424D3AAE18C"> 
      <li id="li_9EF1DF4167164721882E4842C2E0B20C">USM1 </li> 
      <li id="li_7B5D8B7BB5544E7FA4AD702EE281086B">USM amount (120) </li> 
      <li id="li_B3BE096BB0654A2DBADDD6832E499F2A">USM radius (0.6) </li> 
      <li id="li_793DAB145CE7469ABC1182BCBD324657">USM threshold (5) </li> 
      <li id="li_B1954FEBE2084726828D64E8165DA4DA">Resizing (Lanczos) </li> 
      <li id="li_E5ED76998C0543D8A3F9AD178CFD3C2C">Resample (Supersampling, random=half, rate=half) </li> 
      <li id="li_CCEE53544E7D48858398BF3168F1E87D">Contrast (stronger) </li> 
      <li id="li_EB0D25C095FB4D5798AC031AB759849B">Saturation Adjustment (first vertex in middle, second vertex along edge, third vertex middle point low) </li> 
      <li id="li_5C2304DA4A4D4799AE5DCCCB1E2ECBB3">Sharpen (3/4 way to the right) </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- RB: I don't know why this is in here; it was added by someone else: 
Alternate Shader Rendering (default on) checkbox provides a more precise Advanced Shader diffuse rendering pipeline. For a number of effects it also provides an alternate Advanced Shader rendering pipeline. Note that the underlying OpenGL hardware must provide support for the Advanced (Per-Pixel) GLSL Shaders for this option to be vailable; else this checkbox is automatically disabled. -->

<!-- RB: I don't know why this is in here; it was added by someone else:
It should probably also go into the different renders - Render Effects and Alternate Shader - or link to descriptions of each. -->
