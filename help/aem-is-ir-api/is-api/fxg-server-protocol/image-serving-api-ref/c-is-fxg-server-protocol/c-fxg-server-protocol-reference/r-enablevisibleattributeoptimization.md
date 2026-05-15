---
description: FXG의 최적화를 활성화합니다.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
TQID: 'https://experienceleague.adobe.com/QpFJklGLyM9-R9RfGfMQE0mypUKrs-L4g21yWtRyO10'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 2%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

FXG의 최적화를 활성화합니다.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

이 FXG를 전달하는 동안 FXG에서 가시성이 false로 설정된 요소를 제거하여 FXG의 처리 시간을 줄입니다. FXG의 다른 요소에는 영향을 주지 않는 false로 표시되는 요소만 제거됩니다. 예를 들어 `Path`에 텍스트가 있고 `Path`의 가시성이 false로 설정된 경우 이 경로에 텍스트를 그려야 하므로 이 수정자를 활성화해도 FXG에서 제거되지 않습니다.

기본값은 1입니다.
