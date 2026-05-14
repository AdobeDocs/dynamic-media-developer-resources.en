---
description: Enables the optimization of FXG.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
TQID: 'https://experienceleague.adobe.com/QpFJklGLyM9-R9RfGfMQE0mypUKrs-L4g21yWtRyO10'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Enables the optimization of FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Removes the elements whose visibility is set as false in FXG while passing this FXG which in turn reduces the processing time of FXG. Though it removes only those elements with visibility as false that would not impact any other element in FXG. For example, if there is text on `Path` and visibility of `Path` is set as false, then it is not removed from FXG even with this modifier enabled because text needs to be drawn on this path.

Default is 1.
