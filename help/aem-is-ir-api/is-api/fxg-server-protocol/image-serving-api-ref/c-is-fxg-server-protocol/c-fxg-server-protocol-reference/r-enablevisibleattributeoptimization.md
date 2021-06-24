---
description: FXG를 최적화할 수 있습니다.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

FXG를 최적화할 수 있습니다.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

이 FXG를 전달하는 동안 FXG에서 가시성이 false로 설정된 요소를 제거하여 FXG의 처리 시간을 줄입니다. FXG에서 다른 요소에 영향을 주지 않는 가시성이 있는 요소만 false로 제거하지만, 예를 들어 `Path`에 텍스트가 있고 `Path`의 가시성이 false로 설정된 경우, 이 수정자가 활성화된 경우에도 이 경로에서 텍스트를 그려야 하므로 FXG에서 제거되지 않습니다.

기본값은 1입니다.
