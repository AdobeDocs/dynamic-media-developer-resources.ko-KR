---
description: FXG를 최적화할 수 있습니다.
seo-description: FXG를 최적화할 수 있습니다.
seo-title: enableVisibleAttributeOptimization
solution: Experience Manager
title: enableVisibleAttributeOptimization
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7f79aa12-6364-4b34-b547-88d4a778c015
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '100'
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

이 FXG를 전달할 때 FXG에서 가시성이 false로 설정된 요소를 제거합니다. 이렇게 하면 FXG의 처리 시간이 줄어듭니다. FXG의 다른 요소에 영향을 주지 않는 가시성이 있는 요소만 false로 제거하지만, 예를 들어 `Path`에 텍스트가 있고 `Path`의 가시성이 false로 설정되어 있는 경우, 이 경로에 텍스트를 그릴 필요가 있으므로 이 수정자가 활성화되어 있어도 FXG에서 제거되지 않습니다.

기본값은 1입니다.
